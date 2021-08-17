<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `redmine`

-	[`redmine:4`](#redmine4)
-	[`redmine:4-alpine`](#redmine4-alpine)
-	[`redmine:4-passenger`](#redmine4-passenger)
-	[`redmine:4.0`](#redmine40)
-	[`redmine:4.0-alpine`](#redmine40-alpine)
-	[`redmine:4.0-passenger`](#redmine40-passenger)
-	[`redmine:4.0.9`](#redmine409)
-	[`redmine:4.0.9-alpine`](#redmine409-alpine)
-	[`redmine:4.0.9-passenger`](#redmine409-passenger)
-	[`redmine:4.1`](#redmine41)
-	[`redmine:4.1-alpine`](#redmine41-alpine)
-	[`redmine:4.1-passenger`](#redmine41-passenger)
-	[`redmine:4.1.4`](#redmine414)
-	[`redmine:4.1.4-alpine`](#redmine414-alpine)
-	[`redmine:4.1.4-passenger`](#redmine414-passenger)
-	[`redmine:4.2`](#redmine42)
-	[`redmine:4.2-alpine`](#redmine42-alpine)
-	[`redmine:4.2-passenger`](#redmine42-passenger)
-	[`redmine:4.2.2`](#redmine422)
-	[`redmine:4.2.2-alpine`](#redmine422-alpine)
-	[`redmine:4.2.2-passenger`](#redmine422-passenger)
-	[`redmine:alpine`](#redminealpine)
-	[`redmine:latest`](#redminelatest)
-	[`redmine:passenger`](#redminepassenger)

## `redmine:4`

```console
$ docker pull redmine@sha256:eee3e32af89aeb43c91af7b2a61a959c4fba3f6d6cdd9695f56be8c2cefc31b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4` - linux; amd64

```console
$ docker pull redmine@sha256:a40f8da31978334c3d594ec8a053130245877f460f45911fb36e17be8e6e07a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195494644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c25a3b03269000ce6a7aa543599b627f73fa5bcc07debf1eb1cd10129f908dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 17:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:28:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:28:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:28:25 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:03:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:04:03 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:04:03 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:04:03 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:04:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:26:03 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:26:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:26:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:26:48 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:26:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:26:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:26:49 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:26:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e582c090726ff249b7e30253c7f0c11aa2cd14282a8b6cd0e8055c8615e5586`  
		Last Modified: Thu, 22 Jul 2021 17:42:40 GMT  
		Size: 14.5 MB (14509812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f96a83aedee46aef2be1d4f73cc6990dc7e756981b022462100ac16fad345`  
		Last Modified: Thu, 22 Jul 2021 17:42:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9466f2ac94d013cc74523ee4ad44d9720c72baa51d8aecc2afcba41c3754be44`  
		Last Modified: Fri, 23 Jul 2021 11:10:32 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbad6372ccefa1ce14b5eefe2fe718c0cd234b40bf9a70e3d02e131a9dd65d26`  
		Last Modified: Fri, 23 Jul 2021 11:10:45 GMT  
		Size: 94.1 MB (94087869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b93724991108aa18238773a3122f3fcd80f69331610c0a7f00656f690ac7692`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19466676666dc7f1a145b5b2534855e6f32c152cd3da118bc5536badc24da33d`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97607437e7fff6da79d61cc4ee4518344c291c99e79a6b90c113170646e975a`  
		Last Modified: Mon, 02 Aug 2021 19:33:23 GMT  
		Size: 3.1 MB (3061918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67d0866b331d96beda7e546b964c7d5dc48b95b5ea08b4624257efde2481b4a`  
		Last Modified: Mon, 02 Aug 2021 19:33:27 GMT  
		Size: 44.1 MB (44122231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed36b971f221fb68203ab38c344723da172f129a111027998d95d695bdccfa`  
		Last Modified: Mon, 02 Aug 2021 19:33:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm variant v5

```console
$ docker pull redmine@sha256:2ba20de8f2d5813171b6b38d1e727aba839ab6cdd974c966ed2b8cd016b97c70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (196974835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2290c3ececd51c95738415fab07fc46dcc63d3a61e8099fb6c45e290ec3f0d91`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:39:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:39:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 14:39:29 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:48:33 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 14:48:33 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 14:48:34 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 14:52:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 14:52:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 14:52:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 14:52:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 14:52:55 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 14:52:55 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 01:25:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 01:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 01:26:16 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 01:26:17 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 01:26:17 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 01:26:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 20:58:44 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 20:58:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 20:58:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 21:04:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 21:04:31 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 21:04:31 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 21:04:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 21:04:32 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 21:04:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9237058b7c5120d5c6315b5d17a8c1d783be09a228b83772111ce9436c29d078`  
		Last Modified: Thu, 22 Jul 2021 15:15:34 GMT  
		Size: 10.3 MB (10345807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144b4344f580222d2fbc2f0d80fc139ab1a1ddb9a245b6073c41fdca9a93c23e`  
		Last Modified: Thu, 22 Jul 2021 15:15:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8ddbd20410764a5a44de2520de7417bddfcc0fdf2f4fa1b1d4e9ac785ce253`  
		Last Modified: Thu, 22 Jul 2021 15:17:00 GMT  
		Size: 13.9 MB (13871315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1fe10899466e387c0fc9cc130a0a900ffeb91af92c09301e387e444836d74f`  
		Last Modified: Thu, 22 Jul 2021 15:16:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b419523e1af1c8a3f9891c74f5e29e5697be8bf7bf57f23880ac551c460f07`  
		Last Modified: Fri, 23 Jul 2021 01:48:00 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d44a2001e78eed6fc3a85dbe0059a0bfae376949cda406c9304941ed617a23`  
		Last Modified: Fri, 23 Jul 2021 01:49:01 GMT  
		Size: 89.6 MB (89576912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2901c80e9a45cf66afe7fb2306719b195ec9c983783f4058ef68246bb10b95`  
		Last Modified: Fri, 23 Jul 2021 01:47:58 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b0cf9a21c70c0994e217daf5f71efd9d2f8ce8f36e062be7c831492162e99a`  
		Last Modified: Fri, 23 Jul 2021 01:47:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342031318accab10946b43b34804e02f1e0c107a6af3af5a4ebb766152ee509`  
		Last Modified: Mon, 02 Aug 2021 21:11:42 GMT  
		Size: 3.1 MB (3061919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648b6a3dac4889e5f68f30776a664fe9d62256592f37d6d2912163da56f265fa`  
		Last Modified: Mon, 02 Aug 2021 21:12:04 GMT  
		Size: 55.2 MB (55235555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5a29c2452fcab6625565bca85ff5fccfbee37e09b6f1e8455655c2735c166a`  
		Last Modified: Mon, 02 Aug 2021 21:11:38 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm variant v7

```console
$ docker pull redmine@sha256:cac694ac7078f02298b587000698d84cb3bb69637d30c724bd0bcac087c22f41
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190115136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3187fd285a60bd484a8586f3ee1dc8896c0c94e433a102025bf0dae4c344c1b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:15:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 02:15:46 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 02:25:03 GMT
ENV RUBY_MAJOR=2.7
# Fri, 23 Jul 2021 02:25:04 GMT
ENV RUBY_VERSION=2.7.4
# Fri, 23 Jul 2021 02:25:04 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Fri, 23 Jul 2021 02:29:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 02:29:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 02:29:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 02:29:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 02:29:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 02:29:10 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 21:18:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 21:19:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 21:19:37 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 21:19:37 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 21:19:38 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 21:19:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 03 Aug 2021 00:00:45 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 03 Aug 2021 00:00:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 03 Aug 2021 00:00:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 03 Aug 2021 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 03 Aug 2021 00:06:06 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 03 Aug 2021 00:06:07 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 03 Aug 2021 00:06:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Aug 2021 00:06:08 GMT
EXPOSE 3000
# Tue, 03 Aug 2021 00:06:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b8c791d70de7f22816846fbb07e0a1d7d419841c7e539a7cf57ef05fd50c5`  
		Last Modified: Fri, 23 Jul 2021 03:05:10 GMT  
		Size: 9.9 MB (9872218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb12a7edb0af862efa24dc389d7901cd2a894f2e106a1cef931ba0a6d675e2c0`  
		Last Modified: Fri, 23 Jul 2021 03:05:04 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b75d257bf75804e51385b730af2aaba386a501ef50517b8379966d4372c8597`  
		Last Modified: Fri, 23 Jul 2021 03:06:48 GMT  
		Size: 13.8 MB (13766962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc7c7e0536ed6ba4a99c1b8960d7c1d7365c8bc52d230b8af44d07d085916f`  
		Last Modified: Fri, 23 Jul 2021 03:06:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9cbdbb67af5c0b986c2fd6f93a2bacf3c795b046bfdf19e8f483dbc780c643`  
		Last Modified: Fri, 23 Jul 2021 21:39:57 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823bb8e3702405c250a7cc3dadba844fef162cbd0f5b9fb70a107f618dffeddf`  
		Last Modified: Fri, 23 Jul 2021 21:40:51 GMT  
		Size: 85.6 MB (85590187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930c9cc4f262f629914e37abf7b88697bc949d34260a237f8d740ea30ddf5902`  
		Last Modified: Fri, 23 Jul 2021 21:39:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e7aa3a63516ee59c6e77fd1a74b1ce0b303c09b2a97dd0ca3b0af594021030`  
		Last Modified: Fri, 23 Jul 2021 21:39:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2c8055fd9194f59346984cbb7941b37a40023edc25ab3dec3e42e9b8c01287`  
		Last Modified: Tue, 03 Aug 2021 00:12:46 GMT  
		Size: 3.1 MB (3061917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836246f3dcf57e23a39d002b3b9d9a09fedb40b5b6accc7268b28ae167eca128`  
		Last Modified: Tue, 03 Aug 2021 00:13:05 GMT  
		Size: 55.1 MB (55073644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63001a72a77f002e6a9f105ba97f4e5cb147287597ca1e71c8670c6b0e768390`  
		Last Modified: Tue, 03 Aug 2021 00:12:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:168d7ed49573c2aaecf2d0d8adcc21280d9e2c18dc1ddb19848393c9847211e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203243298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a980ba1133cf226e557df7c34d75d5c5e7bfb359db4c611a013f2dd737ac6dc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:11:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_MAJOR=2.7
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 17 Aug 2021 04:20:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:20:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:20:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:20:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:20:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:20:13 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 14:17:02 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 14:17:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:17:25 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 14:17:26 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 14:17:26 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 14:17:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 14:17:27 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 17 Aug 2021 14:17:27 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 17 Aug 2021 14:17:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 14:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:19:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 14:19:47 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 14:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:19:48 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:19:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ab80b058f00336b15786a8d20ce50706c5277560dc1ddb487b7e5c9d24b10`  
		Last Modified: Tue, 17 Aug 2021 04:34:12 GMT  
		Size: 11.3 MB (11263042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6eb72cd750a3e09673b73506f2a2ce24b3006d1773293eb65b72c9a2cdf7190`  
		Last Modified: Tue, 17 Aug 2021 04:34:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2cb28558c1dd6c31a020484f10c613185335d6d30e7c7a81d3e6ffd0f374f0`  
		Last Modified: Tue, 17 Aug 2021 04:35:35 GMT  
		Size: 14.4 MB (14356587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49391d2e67bfbf4fd993b49c9be1225f0a09d4177c605548f82d49cbcfe78b99`  
		Last Modified: Tue, 17 Aug 2021 04:35:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9307e85455464623a9445ee9314b11fd777c561cefed9b38e6f9067bd30653a`  
		Last Modified: Tue, 17 Aug 2021 14:26:18 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba598bababc240a9c29cf82ac1a0b01837945e37b3cb2b17a3a55ba776227b76`  
		Last Modified: Tue, 17 Aug 2021 14:26:34 GMT  
		Size: 92.6 MB (92611086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc88258ae8d8cf36219a3b41b130d1e21bf4c2dfb6e1cf9c3f6b3ae2395817`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c9b592ea00c036970d3b4b7baf687de5e9394670884daa30890ab191cfe5bb`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e8230053e3f65d96319f5f2351fc906de79749654a83811bf21ea7b34f3bee`  
		Last Modified: Tue, 17 Aug 2021 14:26:17 GMT  
		Size: 3.1 MB (3061920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe117b5c157b62194a629b77cf9c9b15c6821516a74c96470c098adba14546ba`  
		Last Modified: Tue, 17 Aug 2021 14:26:22 GMT  
		Size: 56.0 MB (56031346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff9fc675e51cbab5a7a0574bbd10f6ebdc614381aa4a451a98f5884e386b455`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; 386

```console
$ docker pull redmine@sha256:0b76e0e34b7153ffc2a922fe7cc584cdf37e53c0bf95d204bb3ff857e242f139
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202124661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d0b99035f254ab4f5e3822b673034b671859094e70176d730c1807bed1c7d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:39:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 15:39:00 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 15:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:49:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:49:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:49:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:49:39 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 00:10:49 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 00:11:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:11:45 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 00:11:45 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 00:11:46 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 00:11:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:53:31 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 23:53:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 23:53:36 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:54:26 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:54:26 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:54:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:54:27 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:54:27 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071d04ca5200ad3b98494cfde36960022dbd29c9afc33d685ac499fae8a05d63`  
		Last Modified: Thu, 22 Jul 2021 16:06:57 GMT  
		Size: 17.2 MB (17227285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d9d06c9e919afbd9358b702cad5bc0f28b8150722ffedb25ece16dc1f19b2`  
		Last Modified: Thu, 22 Jul 2021 16:06:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9e06bdf88f28c2f5d5893c862c6da8a6a73eb098cb2cd8eec57656d9a79b69`  
		Last Modified: Thu, 22 Jul 2021 16:08:14 GMT  
		Size: 14.0 MB (13992268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f84633b2fe0d1dff5a1fd6ab3a5506af8978d94ded4f5a0f2727ce06805d4`  
		Last Modified: Thu, 22 Jul 2021 16:08:11 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ef59b51318d382563cb5fdab4577df04d06c56bd8885926c9a9374a31ed7c`  
		Last Modified: Fri, 23 Jul 2021 00:22:32 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2922ffac0f77cf1fd832a20d48b586a6621e1d75610c055227f6d76e34928b16`  
		Last Modified: Fri, 23 Jul 2021 00:23:09 GMT  
		Size: 95.7 MB (95703233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb8c5967872202784509fa53a811f849c714ef794dd53a40047d0c81585ce4`  
		Last Modified: Fri, 23 Jul 2021 00:22:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2c1ffe6294aae5e8df812aee47c20e59fe0f4ec3593946e4ed069116ebb9f1`  
		Last Modified: Fri, 23 Jul 2021 00:22:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2101d5d051bcf08ee904abd42115ca10712771f5cf1c4e0b423529da86e741a6`  
		Last Modified: Mon, 02 Aug 2021 23:56:03 GMT  
		Size: 3.1 MB (3061914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fcbda204aa9670b17dc8d7e97735f16ce74df3a60c6d2d9569f7318a335249`  
		Last Modified: Mon, 02 Aug 2021 23:56:09 GMT  
		Size: 44.3 MB (44338267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3a655d5b411d7076572c42fcece59f2189f79f1c6bfa2759554c0fe12a0ec3`  
		Last Modified: Mon, 02 Aug 2021 23:56:01 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; ppc64le

```console
$ docker pull redmine@sha256:ecdb00827fcf83f2f12c122af3ffc2420a6faa270cd7b048c9756f927f7c77fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219650618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57391c1536ff89c22d27544dc68890a924a8d455796c92bdc28721108b71a53c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 00:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 00:33:06 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 00:52:18 GMT
ENV RUBY_MAJOR=2.7
# Fri, 23 Jul 2021 00:52:28 GMT
ENV RUBY_VERSION=2.7.4
# Fri, 23 Jul 2021 00:52:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Fri, 23 Jul 2021 01:01:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 01:01:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 01:01:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 01:01:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 01:01:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 01:01:58 GMT
CMD ["irb"]
# Sat, 24 Jul 2021 02:42:41 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sat, 24 Jul 2021 02:46:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Jul 2021 02:46:14 GMT
ENV RAILS_ENV=production
# Sat, 24 Jul 2021 02:46:17 GMT
WORKDIR /usr/src/redmine
# Sat, 24 Jul 2021 02:46:19 GMT
ENV HOME=/home/redmine
# Sat, 24 Jul 2021 02:46:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:16:59 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 23:17:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 23:17:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:23:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:23:26 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:23:29 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:23:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:23:37 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:23:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f17b372a9c9122b881c2d22680e91d78ef4c329094595c61f5acb2523f41b7`  
		Last Modified: Fri, 23 Jul 2021 01:35:00 GMT  
		Size: 12.7 MB (12704330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064c16cae6894266abd8c9d33cfb671a4ebb2705d8b8bb7495bafc50c3dcd344`  
		Last Modified: Fri, 23 Jul 2021 01:34:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76d2032e7e646d23109ea1a55abb581c169350b85836914155a6837d64eb757`  
		Last Modified: Fri, 23 Jul 2021 01:36:48 GMT  
		Size: 15.0 MB (14997545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996a3088f8cd5e20b9f19c3aebdd4a6228a85b6c0a83f9dde8e2a5ec82976d3`  
		Last Modified: Fri, 23 Jul 2021 01:36:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acdc172d0fc27092df5794b7a17e2c42e7f2497e85086076f490e273db428fe`  
		Last Modified: Sat, 24 Jul 2021 03:36:05 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fe4ded3f0db610cc9dca87e98b2305c850cbaf595886ccb44e3492ad727b18`  
		Last Modified: Sat, 24 Jul 2021 03:36:28 GMT  
		Size: 101.3 MB (101327533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14617640fcda340a6bc04fd1c65d4183ad0dd01a4e3b44fb313d164071471e95`  
		Last Modified: Sat, 24 Jul 2021 03:36:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1b361a5633d0ca044cc644bddc99329645edadfff1cbb48e966deb9b0d079a`  
		Last Modified: Sat, 24 Jul 2021 03:36:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bfbd857622d0239bfa521d75318f40925e9e4608a62a4be7abc2bc89801ec3`  
		Last Modified: Mon, 02 Aug 2021 23:30:32 GMT  
		Size: 3.1 MB (3061921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e4b836dd92fc0980e6e61a697cc881ceb76ca811af742788283ab3211698e1`  
		Last Modified: Mon, 02 Aug 2021 23:30:38 GMT  
		Size: 57.0 MB (57001331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2976222796409af9d080f03664b07bc2a177c8b37d29e7937c0620ba5f908d03`  
		Last Modified: Mon, 02 Aug 2021 23:30:31 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; s390x

```console
$ docker pull redmine@sha256:33d5a2369e443a1bb092e9da696586fae6988113fc4ef99bf98b5af5e03135f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202554693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f13509159fb8e3ef52d7620d4ef325ebe2d7a388fec2faf172536b64ee9ae9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:21:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:21:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:37:51 GMT
ENV RUBY_MAJOR=2.7
# Tue, 17 Aug 2021 04:37:51 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 17 Aug 2021 04:37:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 17 Aug 2021 04:40:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:40:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:40:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:40:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:40:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:40:24 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 13:32:53 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 13:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 13:33:28 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 13:33:28 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 13:33:28 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 13:33:29 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 13:33:29 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 17 Aug 2021 13:33:29 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 17 Aug 2021 13:33:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 13:35:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 13:35:38 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 13:35:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 13:35:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 13:35:39 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 13:35:39 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c03f413a15f7a98caaa2b027613636c576e3d98d8e1a98805c5978f2cc985f`  
		Last Modified: Tue, 17 Aug 2021 05:03:55 GMT  
		Size: 10.8 MB (10814401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ded0951dc51ddc1b38edf558277fec87d4169c1607312f67af2c4ffb9c4f19`  
		Last Modified: Tue, 17 Aug 2021 05:03:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d49ef1e1c8f0247bfa63924e738fc94dc0c4a81ec0e4b2b73df09f08d080005`  
		Last Modified: Tue, 17 Aug 2021 05:04:49 GMT  
		Size: 14.7 MB (14697415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54919ecbd2a42d851761e24bb9a1e9e71346c6ecd753a4c6b7868679823367b`  
		Last Modified: Tue, 17 Aug 2021 05:04:47 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159f1e20f87d626bb303eea037968c316700fdd1fd9fa734e8ebacf14608ab2`  
		Last Modified: Tue, 17 Aug 2021 13:42:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223675cd45b3e6a43e45f6ad1a699c278dc5effe72583bec3657746c84a2a692`  
		Last Modified: Tue, 17 Aug 2021 13:42:24 GMT  
		Size: 91.8 MB (91792621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f55e74adea5c6a7d4c0be869fe00b2451a51e188e2c0e1466d72eaad06cc9d`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cd2e454b71a3aea72543018a9596e611b94ee88301b3d5971854daab02981`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b885ccd7ef756fbf397809a3541c6cadba886972a35c3f9d9d00cc920b16ef2`  
		Last Modified: Tue, 17 Aug 2021 13:42:11 GMT  
		Size: 3.1 MB (3061920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde4808141553382cd3c73078af6ba86889e806ed72c6251287678fbce48b5ea`  
		Last Modified: Tue, 17 Aug 2021 13:42:15 GMT  
		Size: 56.4 MB (56423232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed18e7c147f9b19d7cb774a6462749d36a61882e80d34fff6912e4ed7990252d`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4-alpine`

```console
$ docker pull redmine@sha256:34362d64f5cac220ecf3058a2982583ec0e2cba35273960105a4cff3dc0c4a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:429416f2012459eaa042fe2879ae170f0d1ee68b283059b2e4f855edcaae0101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150082289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a3f4194f1bef28b7e8c9cb584331cfe9876976fd1c68e194837191b82282e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 08 Jul 2021 21:57:27 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 08 Jul 2021 21:57:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 08 Jul 2021 21:57:30 GMT
ENV LANG=C.UTF-8
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_MAJOR=2.7
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 08 Jul 2021 22:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 22:18:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 22:18:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 22:18:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 22:18:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 22:18:51 GMT
CMD ["irb"]
# Wed, 14 Jul 2021 20:22:24 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 14 Jul 2021 20:22:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 14 Jul 2021 20:22:33 GMT
ENV RAILS_ENV=production
# Wed, 14 Jul 2021 20:22:33 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jul 2021 20:22:33 GMT
ENV HOME=/home/redmine
# Wed, 14 Jul 2021 20:22:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:27:15 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:27:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:27:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:27:19 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 02 Aug 2021 19:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Mon, 02 Aug 2021 19:29:21 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:29:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Mon, 02 Aug 2021 19:29:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:29:22 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:29:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5b0ea69e9ed42c49b5af449b703a12a4d2f2e28d87905af6fcd903fdae5689`  
		Last Modified: Thu, 08 Jul 2021 22:38:46 GMT  
		Size: 3.6 MB (3581658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad656ed833315b61ea674706f32c2d18d7412c7120926442af57b9131ee72ee`  
		Last Modified: Thu, 08 Jul 2021 22:38:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626f6830afc6fb7a05a8f18f2b98e4ea4db3d2dd50803e5cd2c627fe25150dc8`  
		Last Modified: Thu, 08 Jul 2021 22:40:13 GMT  
		Size: 14.4 MB (14373123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5375389679c9573d241b22905aee17b20981e2628989561698087f107fcfed4a`  
		Last Modified: Thu, 08 Jul 2021 22:40:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76a82132aeb154f32b80803eecedc3e27e062a35ae1e05284dc2d7e6c7f4f59`  
		Last Modified: Wed, 14 Jul 2021 20:35:42 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb4af997128346f54fa569d3a04180c718e02a90e90eff7161241d54deef92`  
		Last Modified: Wed, 14 Jul 2021 20:35:52 GMT  
		Size: 69.5 MB (69526214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da2816c58ef08b826f823d7b6a4126bb63594ed1109880b795c28cc4d3f032`  
		Last Modified: Wed, 14 Jul 2021 20:35:39 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f34be07349b94807cc58a0e31cecec279d0591b9a6f1f65f1dbe94a4713462`  
		Last Modified: Wed, 14 Jul 2021 20:35:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98c03ed41f8aa891bcd79e61fbb88cda198d71f5a8de4f510950e7f58aa1a15`  
		Last Modified: Mon, 02 Aug 2021 19:34:04 GMT  
		Size: 3.1 MB (3062843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08d14dd9ea01201645da35bc3855c4b0a6270b9d4ae9510f9da35fb4150e833`  
		Last Modified: Mon, 02 Aug 2021 19:34:08 GMT  
		Size: 56.7 MB (56722754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bee94fd486f4fb693e4765ade966dd49ee96cd0aff32109f156b9a2511d1af3`  
		Last Modified: Mon, 02 Aug 2021 19:34:03 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:1227b146ef6133442f3c82299c894fd310739b1042176653e2126cf65a6bb369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:8f065daab31dbf85b85fa0bd93241a0225439d387e574f3b3c3ed2bac86bacc5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221545515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5b06ed983bc1e6cfc65432f997639be41bac864baaa904857feedfda309362`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 17:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:28:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:28:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:28:25 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:03:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:04:03 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:04:03 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:04:03 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:04:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:26:03 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:26:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:26:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:26:48 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:26:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:26:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:26:49 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:26:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Mon, 02 Aug 2021 19:26:54 GMT
ENV PASSENGER_VERSION=6.0.10
# Mon, 02 Aug 2021 19:27:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:27:11 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Mon, 02 Aug 2021 19:27:11 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Mon, 02 Aug 2021 19:27:11 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e582c090726ff249b7e30253c7f0c11aa2cd14282a8b6cd0e8055c8615e5586`  
		Last Modified: Thu, 22 Jul 2021 17:42:40 GMT  
		Size: 14.5 MB (14509812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f96a83aedee46aef2be1d4f73cc6990dc7e756981b022462100ac16fad345`  
		Last Modified: Thu, 22 Jul 2021 17:42:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9466f2ac94d013cc74523ee4ad44d9720c72baa51d8aecc2afcba41c3754be44`  
		Last Modified: Fri, 23 Jul 2021 11:10:32 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbad6372ccefa1ce14b5eefe2fe718c0cd234b40bf9a70e3d02e131a9dd65d26`  
		Last Modified: Fri, 23 Jul 2021 11:10:45 GMT  
		Size: 94.1 MB (94087869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b93724991108aa18238773a3122f3fcd80f69331610c0a7f00656f690ac7692`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19466676666dc7f1a145b5b2534855e6f32c152cd3da118bc5536badc24da33d`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97607437e7fff6da79d61cc4ee4518344c291c99e79a6b90c113170646e975a`  
		Last Modified: Mon, 02 Aug 2021 19:33:23 GMT  
		Size: 3.1 MB (3061918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67d0866b331d96beda7e546b964c7d5dc48b95b5ea08b4624257efde2481b4a`  
		Last Modified: Mon, 02 Aug 2021 19:33:27 GMT  
		Size: 44.1 MB (44122231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed36b971f221fb68203ab38c344723da172f129a111027998d95d695bdccfa`  
		Last Modified: Mon, 02 Aug 2021 19:33:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913b642de7599d445e0069c22e66310828fb96025c0b69e5be168036e5cae921`  
		Last Modified: Mon, 02 Aug 2021 19:33:47 GMT  
		Size: 21.1 MB (21131586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c214594b43db5e8aa08dd61b352a254deb095023ee416412ce655e42e783c5`  
		Last Modified: Mon, 02 Aug 2021 19:33:45 GMT  
		Size: 4.9 MB (4919285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0`

```console
$ docker pull redmine@sha256:666cf5c71c9adad56dd82e1d7cd22e551cd8685f9525ef6329cde48daaf2ed7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.0` - linux; amd64

```console
$ docker pull redmine@sha256:a30cd3dc5580f5966689be984309a4c58b44a1ecb3ce8a989f0712765b575b6a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205072160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd81a2ff1ed6cd5076a6a870886dec018329cd0f3bdf1047393351eed3a2b4f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 17:31:25 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 17:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:34:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:34:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:34:07 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:05:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:07:36 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:07:36 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:07:37 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:07:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 11:07:38 GMT
ENV REDMINE_VERSION=4.0.9
# Fri, 23 Jul 2021 11:07:38 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Fri, 23 Jul 2021 11:07:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 11:09:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 11:09:35 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 11:09:35 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 11:09:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 11:09:35 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 11:09:36 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b7373cf9d9195064da3c92860c7157644c595720fffd5bb48615ac96985d5`  
		Last Modified: Thu, 22 Jul 2021 17:43:38 GMT  
		Size: 21.5 MB (21468044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb83e25b0fb68c5c98194adb0ad3740bc7d2242801c213e7d7949281f901679`  
		Last Modified: Thu, 22 Jul 2021 17:43:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61371aadcf232eb667c47dbba436a5611088d97ba4c8a9bd0c271f36882b027d`  
		Last Modified: Fri, 23 Jul 2021 11:11:30 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527440fec380cb5ffab3044cdb10895391dd8c0967dbf50c94f5a6ac54cbe48`  
		Last Modified: Fri, 23 Jul 2021 11:12:23 GMT  
		Size: 81.2 MB (81200505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ead518ac18671d74e03ee9c8d93c71f9ced66c21ba86bcc2c503a8e5c8326b`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f008d376270911f79e7e6c177b16b77b13d0309adcd8dd7266e1bf0b2b4dd9`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9566b0985629bf3ebfee385cb50b88bb50798e5ae4b5c4dbb87298c9baedf66e`  
		Last Modified: Fri, 23 Jul 2021 11:12:09 GMT  
		Size: 2.5 MB (2542546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe2b1704c38fcd44f73cfa4cd5ed3ee7c7c9182e905d3bda2bad7457e7478f2`  
		Last Modified: Fri, 23 Jul 2021 11:12:15 GMT  
		Size: 60.1 MB (60148250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0011d8346df5b8d0b6540960e13a4a200f5fd7cd2283b3d0c7e0e3d61856f2c5`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm variant v5

```console
$ docker pull redmine@sha256:f68b890b9070068d1d1e4d2e129b6a2588f712889ef062ee4ba10ed3208024de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194719441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb736ee279c270380b4ea5b0c9aeef3d9e76b9e17b589c178f12c5e569445a2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:39:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:39:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 14:39:29 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 15:01:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:02:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:02:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:02:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:02:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:02:04 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 01:32:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 01:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 01:40:50 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 01:40:51 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 01:40:51 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 01:40:53 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 01:40:53 GMT
ENV REDMINE_VERSION=4.0.9
# Fri, 23 Jul 2021 01:40:53 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Fri, 23 Jul 2021 01:40:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 01:47:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 01:47:02 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 01:47:02 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 01:47:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 01:47:03 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 01:47:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9237058b7c5120d5c6315b5d17a8c1d783be09a228b83772111ce9436c29d078`  
		Last Modified: Thu, 22 Jul 2021 15:15:34 GMT  
		Size: 10.3 MB (10345807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144b4344f580222d2fbc2f0d80fc139ab1a1ddb9a245b6073c41fdca9a93c23e`  
		Last Modified: Thu, 22 Jul 2021 15:15:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae149ea188f1e064a0256560e0273ae4b331a42ab93326fd9a79753cfb63299d`  
		Last Modified: Thu, 22 Jul 2021 15:18:00 GMT  
		Size: 20.7 MB (20733368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5d2d97d7d53265f79bb7d6b5cfc05f237e3d237d9cf22475536aa4fd57ccde`  
		Last Modified: Thu, 22 Jul 2021 15:17:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822c77937c7bc9bc3d506cf3a12ef2ada0bdbc4c0db3af2efaecc31c4191df4a`  
		Last Modified: Fri, 23 Jul 2021 01:49:24 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf88d0b525291c8ed7e29e9e8ba21a25a8c186e2b45bbe036f6b45b60dbb725`  
		Last Modified: Fri, 23 Jul 2021 01:51:32 GMT  
		Size: 77.0 MB (76965230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259fc97807986ce68b1adaf43768244b0f7feb0b45a3693494d303a9bde78206`  
		Last Modified: Fri, 23 Jul 2021 01:50:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da90621c3344a001d962d4e9ee37ee08502d9a1d4c1a26e40082177f7d78eb9`  
		Last Modified: Fri, 23 Jul 2021 01:50:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6d126519049a526572ad6fbdff768305806b6cf0b42a0707007187491835a6`  
		Last Modified: Fri, 23 Jul 2021 01:50:43 GMT  
		Size: 2.5 MB (2542540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8457820c2404a0f956447bb7bde617741101e1b6ac11c79c7dc9e4ba284f06fb`  
		Last Modified: Fri, 23 Jul 2021 01:51:09 GMT  
		Size: 59.2 MB (59249171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae53e60f882218b768c0d7ea4a5a40fbe5512f79710f794079f92caa7a225d1`  
		Last Modified: Fri, 23 Jul 2021 01:50:40 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm variant v7

```console
$ docker pull redmine@sha256:adaecf942bcbf470ce5a40970bf2c079bcdcc70921efddada7897d7966c86313
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188053580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afae75ed20002c892916b188691ea63f8643a55ed5c8b26670d0ad3c396ed670`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:15:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 02:15:46 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 02:46:35 GMT
ENV RUBY_MAJOR=2.6
# Fri, 23 Jul 2021 02:46:35 GMT
ENV RUBY_VERSION=2.6.8
# Fri, 23 Jul 2021 02:46:36 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Fri, 23 Jul 2021 02:50:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 02:50:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 02:50:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 02:50:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 02:50:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 02:50:43 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 21:25:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 21:33:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 21:33:10 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 21:33:11 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 21:33:11 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 21:33:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 21:33:13 GMT
ENV REDMINE_VERSION=4.0.9
# Fri, 23 Jul 2021 21:33:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Fri, 23 Jul 2021 21:33:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 21:38:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 21:38:54 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 21:38:55 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 21:38:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 21:38:56 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 21:38:56 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b8c791d70de7f22816846fbb07e0a1d7d419841c7e539a7cf57ef05fd50c5`  
		Last Modified: Fri, 23 Jul 2021 03:05:10 GMT  
		Size: 9.9 MB (9872218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb12a7edb0af862efa24dc389d7901cd2a894f2e106a1cef931ba0a6d675e2c0`  
		Last Modified: Fri, 23 Jul 2021 03:05:04 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0837e4e34dc8fe0ec9567b99bb7b1397a813fca3b43abfbbd75ee231a946a979`  
		Last Modified: Fri, 23 Jul 2021 03:07:54 GMT  
		Size: 20.6 MB (20643760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c76309d8689f06c398ddc0f6b5ec99a408c65c613d73d63fb9f5101ebe3e2a1`  
		Last Modified: Fri, 23 Jul 2021 03:07:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c349a607ae692434577c905a1f4029d996cee89a0c9f214fa866ac935ceddf23`  
		Last Modified: Fri, 23 Jul 2021 21:41:16 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8cee36193dcad9a6170ac7b62624990e45bd8e40f280263cbc385102b815b5`  
		Last Modified: Fri, 23 Jul 2021 21:43:15 GMT  
		Size: 73.3 MB (73264161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51cab5b19ebed7ef72637004e6d5caa4c8e6339b68a5858b092f7969de48022`  
		Last Modified: Fri, 23 Jul 2021 21:42:27 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aa70a44bb3a34cdec8010dc14c194820f60d59bb588e122bb488dc1c65dc40`  
		Last Modified: Fri, 23 Jul 2021 21:42:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f27c773a3f3c9a852c5331d84ab63be28de904da75fa384a2b36a9ebc45b27`  
		Last Modified: Fri, 23 Jul 2021 21:42:31 GMT  
		Size: 2.5 MB (2542541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ac45246d6c17b1fb3dd54ad65b762e50f7ca0eb448a4137ada4f6896ef5925`  
		Last Modified: Fri, 23 Jul 2021 21:42:55 GMT  
		Size: 59.0 MB (58980689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a33b1a2d4b8fa224e96757684c0e214ff8c5922ab1ca4606c39b3ee25dcadfd`  
		Last Modified: Fri, 23 Jul 2021 21:42:27 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b88759af15842d0592a9ea5f67a803fd6ac33252a035ab554e88098f02574b52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 MB (200850483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43460e0a84b844270c94cae84bf674b95dd7fc307754fe931011e927e98abd47`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:11:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:25:18 GMT
ENV RUBY_MAJOR=2.6
# Tue, 17 Aug 2021 04:25:19 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 17 Aug 2021 04:25:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 17 Aug 2021 04:27:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:27:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:27:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:27:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:27:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:27:26 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 14:19:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 14:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:23:16 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 14:23:16 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 14:23:16 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 14:23:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 14:23:17 GMT
ENV REDMINE_VERSION=4.0.9
# Tue, 17 Aug 2021 14:23:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Tue, 17 Aug 2021 14:23:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 14:25:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:25:43 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 14:25:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 14:25:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:25:44 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:25:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ab80b058f00336b15786a8d20ce50706c5277560dc1ddb487b7e5c9d24b10`  
		Last Modified: Tue, 17 Aug 2021 04:34:12 GMT  
		Size: 11.3 MB (11263042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6eb72cd750a3e09673b73506f2a2ce24b3006d1773293eb65b72c9a2cdf7190`  
		Last Modified: Tue, 17 Aug 2021 04:34:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a741dfbe27573196b9f78f97eb7f35b06eaff990866fb7f894987974bd3f6d`  
		Last Modified: Tue, 17 Aug 2021 04:36:41 GMT  
		Size: 21.3 MB (21309045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6991754b0a79718bf8ab6c058b0ca4e091450b59072ac29e34401525b4337cc2`  
		Last Modified: Tue, 17 Aug 2021 04:36:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b2d6fcce3e7c045cbcf366963f15eecf60f206a0f9affdb4be5f3e1cdb8e58`  
		Last Modified: Tue, 17 Aug 2021 14:26:56 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39391463d0169869babe67051e72a4badb5e6538463aa13476d59709b2d1627a`  
		Last Modified: Tue, 17 Aug 2021 14:27:39 GMT  
		Size: 79.7 MB (79749184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bd4702d9b260665631a6e852231aba7fd3ba3322e443a969edb1d5f08f7196`  
		Last Modified: Tue, 17 Aug 2021 14:27:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93416b8e64e921655341d941d209345e030b91a533d8ffb233ece46312f04886`  
		Last Modified: Tue, 17 Aug 2021 14:27:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a29700d7f8864656fe98ec815952adea82a0cc692c4d47e68902625234b455f`  
		Last Modified: Tue, 17 Aug 2021 14:27:25 GMT  
		Size: 2.5 MB (2542545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb789346c1b22068ac9ec84aa33e715bb1529ef95da7ab381f8775aadeb83ff`  
		Last Modified: Tue, 17 Aug 2021 14:27:32 GMT  
		Size: 60.1 MB (60067351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd11b2bf406e2bdcdb6a7e80ab2722c7b56c44677f10548b9d342d2c88669302`  
		Last Modified: Tue, 17 Aug 2021 14:27:24 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; 386

```console
$ docker pull redmine@sha256:9b4b725043561fc6f093b1805ecf81bd81c278ff9900fe39a00e413d9864647c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210332451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21c08cabd048f1e2a1a723cb64800b532c989486494956a12e85e74c7cbd805`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:39:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 15:39:00 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:53:08 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 15:56:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:56:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:56:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:56:29 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 00:13:48 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 00:17:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:17:17 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 00:17:18 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 00:17:18 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 00:17:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 00:17:20 GMT
ENV REDMINE_VERSION=4.0.9
# Fri, 23 Jul 2021 00:17:21 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Fri, 23 Jul 2021 00:17:27 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 00:21:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 00:21:42 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 00:21:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 00:21:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 00:21:44 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 00:21:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071d04ca5200ad3b98494cfde36960022dbd29c9afc33d685ac499fae8a05d63`  
		Last Modified: Thu, 22 Jul 2021 16:06:57 GMT  
		Size: 17.2 MB (17227285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d9d06c9e919afbd9358b702cad5bc0f28b8150722ffedb25ece16dc1f19b2`  
		Last Modified: Thu, 22 Jul 2021 16:06:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3172650cf56a46da1b8438a86468d4053edf77c17eaad06d10b7c7a4f89d13ff`  
		Last Modified: Thu, 22 Jul 2021 16:09:12 GMT  
		Size: 20.9 MB (20910118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686761ac4b88297af44e82ba027c5c73411fe3e728b11bbdc631ea19cae4207`  
		Last Modified: Thu, 22 Jul 2021 16:09:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd85881cfa469c977c54673a6f7a5069bd5524e91c3dcc68765e8c34126cabe2`  
		Last Modified: Fri, 23 Jul 2021 00:23:41 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50e9554d325af14ff7a934082d622c3943218047ed2aa4294b0c7535581244b`  
		Last Modified: Fri, 23 Jul 2021 00:25:08 GMT  
		Size: 82.6 MB (82599806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a2d230fb36dab9b19e500fa31f006d0eeee505ceff2925ba4be6e11f79e7cb`  
		Last Modified: Fri, 23 Jul 2021 00:24:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab5662ff0e835add5c4df375cbd7a031f48ab605541cefdee4c0d951b6a724`  
		Last Modified: Fri, 23 Jul 2021 00:24:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fb67e4236a41bcff9cbb8e3a50fb0448092b2e9c48698898fd97c9be5596d6`  
		Last Modified: Fri, 23 Jul 2021 00:24:35 GMT  
		Size: 2.5 MB (2542547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce6344df4fd2a77ff42e131656f0ecabf7e82245e9baa99c29bbd0d0f746fbf`  
		Last Modified: Fri, 23 Jul 2021 00:24:54 GMT  
		Size: 59.3 MB (59251004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9705ef65a1f1f76bc1e8bc800dc07a0a770e8e1bf07b138f90cf1d3126ba5f38`  
		Last Modified: Fri, 23 Jul 2021 00:24:33 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; ppc64le

```console
$ docker pull redmine@sha256:f66f4634bf1585887b6cadeb8646989343e1ee4c44a136cd20edbe611d29e44d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216453624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9be8237ffe8a0fb25d3069a58c72db83381976bcc3b21b0c9815de1b8edca92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 00:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 00:33:06 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 01:11:31 GMT
ENV RUBY_MAJOR=2.6
# Fri, 23 Jul 2021 01:11:38 GMT
ENV RUBY_VERSION=2.6.8
# Fri, 23 Jul 2021 01:11:44 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Fri, 23 Jul 2021 01:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 01:26:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 01:26:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 01:26:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 01:26:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 01:26:59 GMT
CMD ["irb"]
# Sat, 24 Jul 2021 02:51:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sat, 24 Jul 2021 03:14:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Jul 2021 03:14:23 GMT
ENV RAILS_ENV=production
# Sat, 24 Jul 2021 03:14:25 GMT
WORKDIR /usr/src/redmine
# Sat, 24 Jul 2021 03:14:30 GMT
ENV HOME=/home/redmine
# Sat, 24 Jul 2021 03:14:38 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 24 Jul 2021 03:14:46 GMT
ENV REDMINE_VERSION=4.0.9
# Sat, 24 Jul 2021 03:14:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Sat, 24 Jul 2021 03:15:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 24 Jul 2021 03:35:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 24 Jul 2021 03:35:13 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 24 Jul 2021 03:35:17 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Sat, 24 Jul 2021 03:35:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 24 Jul 2021 03:35:27 GMT
EXPOSE 3000
# Sat, 24 Jul 2021 03:35:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f17b372a9c9122b881c2d22680e91d78ef4c329094595c61f5acb2523f41b7`  
		Last Modified: Fri, 23 Jul 2021 01:35:00 GMT  
		Size: 12.7 MB (12704330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064c16cae6894266abd8c9d33cfb671a4ebb2705d8b8bb7495bafc50c3dcd344`  
		Last Modified: Fri, 23 Jul 2021 01:34:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33960675014a7e56a0cf9f85e256ec6cce1c710723a7cd8f64935709d00e323d`  
		Last Modified: Fri, 23 Jul 2021 01:38:17 GMT  
		Size: 22.0 MB (21985713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047ee7c416fdfdb76a18bc7d50d5c00c1568b5e197242760391ce18bec14da13`  
		Last Modified: Fri, 23 Jul 2021 01:38:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c93f3da9b7a0eaf5df16b7b32a686296eaa146856420c2ce2d9ee2ad916121`  
		Last Modified: Sat, 24 Jul 2021 03:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf10994c116f970b482c990a6b89a17d4292257aa8d4c8f112785b16d9683b77`  
		Last Modified: Sat, 24 Jul 2021 03:37:45 GMT  
		Size: 87.9 MB (87901004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbc18e39a895f554cc9e72fb3f4f8fd6e3f14b8ba82bd4e555e33eab6e1e53c`  
		Last Modified: Sat, 24 Jul 2021 03:37:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e987abb4c826ab5b57ae49bcd75a9f15613c83d87e0677a62c4a11a1e60997`  
		Last Modified: Sat, 24 Jul 2021 03:37:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70618bee2d6cbdd87a9143949d8b3b252e21aa336af80a651853bfeac299ccb1`  
		Last Modified: Sat, 24 Jul 2021 03:37:26 GMT  
		Size: 2.5 MB (2542542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a66220dec1e7b2bd2bdba148f204920c16e19c11be7ac1000b3a337d3b3f0b`  
		Last Modified: Sat, 24 Jul 2021 03:37:35 GMT  
		Size: 60.8 MB (60762081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2192580103ba2e9b41655dfdbd0ed3800350febf95cbdba890bb38b2f9d12bc0`  
		Last Modified: Sat, 24 Jul 2021 03:37:25 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; s390x

```console
$ docker pull redmine@sha256:d328d900e9b6cb797ed448f67b29841ed5cf8a4c3832bba7fc865e60bd8eaacb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200270811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1f10c0616a1c38940f42bed4e642ccdd9226b8d89fc62b6e3e4dabcc41355e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:21:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:21:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:54:27 GMT
ENV RUBY_MAJOR=2.6
# Tue, 17 Aug 2021 04:54:28 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 17 Aug 2021 04:54:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 17 Aug 2021 04:57:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:57:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:57:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:57:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:57:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:57:43 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 13:35:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 13:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 13:39:00 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 13:39:01 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 13:39:01 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 13:39:02 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 13:39:03 GMT
ENV REDMINE_VERSION=4.0.9
# Tue, 17 Aug 2021 13:39:03 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Tue, 17 Aug 2021 13:39:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 13:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 13:41:36 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 13:41:36 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 13:41:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 13:41:36 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 13:41:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c03f413a15f7a98caaa2b027613636c576e3d98d8e1a98805c5978f2cc985f`  
		Last Modified: Tue, 17 Aug 2021 05:03:55 GMT  
		Size: 10.8 MB (10814401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ded0951dc51ddc1b38edf558277fec87d4169c1607312f67af2c4ffb9c4f19`  
		Last Modified: Tue, 17 Aug 2021 05:03:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b5f065983b815df03f5d378b737ce8b8950a6f775907f64c8d9413edfec507`  
		Last Modified: Tue, 17 Aug 2021 05:05:31 GMT  
		Size: 21.6 MB (21620194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c23b68c30a72cdc95043eff33b8ac51682c16759a2f483c8f4255db0f287c2`  
		Last Modified: Tue, 17 Aug 2021 05:05:28 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04534d357d558a08a4aea1da302e17954529ebf3804b4a0fe94cff2edac70b48`  
		Last Modified: Tue, 17 Aug 2021 13:42:39 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218be0290ec79b3f04e7f77dfe8f8ac8cbd9201826ad01308fcbadb25a5e6a77`  
		Last Modified: Tue, 17 Aug 2021 13:43:11 GMT  
		Size: 78.9 MB (78942684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2fac95700e00653babfdc8d8adf7f68e3bad29e80fa48749640f683e194389`  
		Last Modified: Tue, 17 Aug 2021 13:43:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ced46f2f9e40ad3ad2fbf664f2e2e2602d4d28bfe90a309a0f825cf0fca8b5`  
		Last Modified: Tue, 17 Aug 2021 13:43:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f2b73b065f8dcb4e9e6dffcbe73867f941480ca0a5d80811e345039ff4105e`  
		Last Modified: Tue, 17 Aug 2021 13:43:00 GMT  
		Size: 2.5 MB (2542549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28def5e72cbe09aa3df74f8671867014e00dbab04acaaf0216d648662c3ced87`  
		Last Modified: Tue, 17 Aug 2021 13:43:06 GMT  
		Size: 60.6 MB (60585884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902db45741704beb098e03501c7e36acd54a48c9891229a213037876e70978d7`  
		Last Modified: Tue, 17 Aug 2021 13:42:59 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0-alpine`

```console
$ docker pull redmine@sha256:9b8ec4df56622e6060cfc701a5059050c3b734da828cc8f154367d016ac22227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:baed7be679b02ee2f252035dbc06e0fed257f026688a9fe3da3832b0bf54ae51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153900570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69f8d92df2e7210bf95dfe2b409c178cacd6767792bbca288c47ff774f5e817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 08 Jul 2021 21:57:27 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 08 Jul 2021 21:57:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 08 Jul 2021 21:57:30 GMT
ENV LANG=C.UTF-8
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_MAJOR=2.6
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 08 Jul 2021 22:35:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 22:35:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 22:35:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 22:35:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 22:35:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 22:35:59 GMT
CMD ["irb"]
# Wed, 14 Jul 2021 20:26:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 14 Jul 2021 20:32:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Wed, 14 Jul 2021 20:32:28 GMT
ENV RAILS_ENV=production
# Wed, 14 Jul 2021 20:32:28 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jul 2021 20:32:29 GMT
ENV HOME=/home/redmine
# Wed, 14 Jul 2021 20:32:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 14 Jul 2021 20:32:30 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 14 Jul 2021 20:32:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 14 Jul 2021 20:32:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 14 Jul 2021 20:32:34 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 14 Jul 2021 20:34:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 14 Jul 2021 20:34:03 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 14 Jul 2021 20:34:04 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Wed, 14 Jul 2021 20:34:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jul 2021 20:34:04 GMT
EXPOSE 3000
# Wed, 14 Jul 2021 20:34:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5b0ea69e9ed42c49b5af449b703a12a4d2f2e28d87905af6fcd903fdae5689`  
		Last Modified: Thu, 08 Jul 2021 22:38:46 GMT  
		Size: 3.6 MB (3581658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad656ed833315b61ea674706f32c2d18d7412c7120926442af57b9131ee72ee`  
		Last Modified: Thu, 08 Jul 2021 22:38:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9d07bc1851494b8935d8593efecfea98e2c4a4ff1c3eaf2e5319eb31cb3a2`  
		Last Modified: Thu, 08 Jul 2021 22:41:47 GMT  
		Size: 19.9 MB (19889336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d50c8fd3318db7f0dbb1d50a8aa4e571ae4926440e66c07be861dd4685211d`  
		Last Modified: Thu, 08 Jul 2021 22:41:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e030b8560a875bcd9c87e7dd1c8faf94a9d48cf039ee0bf125017750cc802b`  
		Last Modified: Wed, 14 Jul 2021 20:37:07 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f9541899ba9d0a6bde1aaa23a83e1e1cd6a17fc0adecb390591f66b0ccb93b`  
		Last Modified: Wed, 14 Jul 2021 20:38:23 GMT  
		Size: 66.2 MB (66172712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bc115e3ba6c2cb414f0bb5c4df5c0dad6b57442cf9044bbe1fc33e266821b4`  
		Last Modified: Wed, 14 Jul 2021 20:38:08 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0bf51497625cb7774642f214c3424e7a0e97dff3e9c1c7e96c279d965e3981`  
		Last Modified: Wed, 14 Jul 2021 20:38:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d58772bc79f2753b31d538e035d07bd09bb2731fc4843259e09b0c4be77e2f9`  
		Last Modified: Wed, 14 Jul 2021 20:38:10 GMT  
		Size: 2.5 MB (2543757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f9be46406ca851c437e457fa10b35fea3c15bda96b4f315f9514efea879beb`  
		Last Modified: Wed, 14 Jul 2021 20:38:15 GMT  
		Size: 58.9 MB (58897408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad779a0b33ba3ea1e31e4a1ee1c8bab4546aadacd48d0fb32d05adc26c02906`  
		Last Modified: Wed, 14 Jul 2021 20:38:08 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0-passenger`

```console
$ docker pull redmine@sha256:319dd08d03106ba06b96a6c2c211c7bdbdf6671de495c0b1a1e270098bf3cb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:0d1a0ccbcaa59efb65e98fbf387d0cf046cb38a46c274cb0e25ca9e2aa13d165
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231318767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c59b0c8114ee55abb9152e916fd05b8ced427af548ff6d169917a286874784`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 17:31:25 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 17:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:34:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:34:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:34:07 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:05:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:07:36 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:07:36 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:07:37 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:07:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 11:07:38 GMT
ENV REDMINE_VERSION=4.0.9
# Fri, 23 Jul 2021 11:07:38 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Fri, 23 Jul 2021 11:07:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 11:09:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 11:09:35 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 11:09:35 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 11:09:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 11:09:35 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 11:09:36 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 23 Jul 2021 11:09:39 GMT
ENV PASSENGER_VERSION=6.0.10
# Fri, 23 Jul 2021 11:09:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 11:09:57 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Fri, 23 Jul 2021 11:09:57 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Fri, 23 Jul 2021 11:09:58 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b7373cf9d9195064da3c92860c7157644c595720fffd5bb48615ac96985d5`  
		Last Modified: Thu, 22 Jul 2021 17:43:38 GMT  
		Size: 21.5 MB (21468044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb83e25b0fb68c5c98194adb0ad3740bc7d2242801c213e7d7949281f901679`  
		Last Modified: Thu, 22 Jul 2021 17:43:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61371aadcf232eb667c47dbba436a5611088d97ba4c8a9bd0c271f36882b027d`  
		Last Modified: Fri, 23 Jul 2021 11:11:30 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527440fec380cb5ffab3044cdb10895391dd8c0967dbf50c94f5a6ac54cbe48`  
		Last Modified: Fri, 23 Jul 2021 11:12:23 GMT  
		Size: 81.2 MB (81200505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ead518ac18671d74e03ee9c8d93c71f9ced66c21ba86bcc2c503a8e5c8326b`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f008d376270911f79e7e6c177b16b77b13d0309adcd8dd7266e1bf0b2b4dd9`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9566b0985629bf3ebfee385cb50b88bb50798e5ae4b5c4dbb87298c9baedf66e`  
		Last Modified: Fri, 23 Jul 2021 11:12:09 GMT  
		Size: 2.5 MB (2542546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe2b1704c38fcd44f73cfa4cd5ed3ee7c7c9182e905d3bda2bad7457e7478f2`  
		Last Modified: Fri, 23 Jul 2021 11:12:15 GMT  
		Size: 60.1 MB (60148250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0011d8346df5b8d0b6540960e13a4a200f5fd7cd2283b3d0c7e0e3d61856f2c5`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4115f43d92079ea0e1fd41e8d42467fc73d3b96a655e7eeaf1ceed99049832cf`  
		Last Modified: Fri, 23 Jul 2021 11:12:37 GMT  
		Size: 21.3 MB (21327322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923adc728211126334159e16d7a0931ea37967801e506f3f0eb071d26ced3762`  
		Last Modified: Fri, 23 Jul 2021 11:12:35 GMT  
		Size: 4.9 MB (4919285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.9`

```console
$ docker pull redmine@sha256:666cf5c71c9adad56dd82e1d7cd22e551cd8685f9525ef6329cde48daaf2ed7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.0.9` - linux; amd64

```console
$ docker pull redmine@sha256:a30cd3dc5580f5966689be984309a4c58b44a1ecb3ce8a989f0712765b575b6a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205072160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd81a2ff1ed6cd5076a6a870886dec018329cd0f3bdf1047393351eed3a2b4f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 17:31:25 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 17:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:34:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:34:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:34:07 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:05:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:07:36 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:07:36 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:07:37 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:07:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 11:07:38 GMT
ENV REDMINE_VERSION=4.0.9
# Fri, 23 Jul 2021 11:07:38 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Fri, 23 Jul 2021 11:07:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 11:09:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 11:09:35 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 11:09:35 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 11:09:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 11:09:35 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 11:09:36 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b7373cf9d9195064da3c92860c7157644c595720fffd5bb48615ac96985d5`  
		Last Modified: Thu, 22 Jul 2021 17:43:38 GMT  
		Size: 21.5 MB (21468044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb83e25b0fb68c5c98194adb0ad3740bc7d2242801c213e7d7949281f901679`  
		Last Modified: Thu, 22 Jul 2021 17:43:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61371aadcf232eb667c47dbba436a5611088d97ba4c8a9bd0c271f36882b027d`  
		Last Modified: Fri, 23 Jul 2021 11:11:30 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527440fec380cb5ffab3044cdb10895391dd8c0967dbf50c94f5a6ac54cbe48`  
		Last Modified: Fri, 23 Jul 2021 11:12:23 GMT  
		Size: 81.2 MB (81200505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ead518ac18671d74e03ee9c8d93c71f9ced66c21ba86bcc2c503a8e5c8326b`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f008d376270911f79e7e6c177b16b77b13d0309adcd8dd7266e1bf0b2b4dd9`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9566b0985629bf3ebfee385cb50b88bb50798e5ae4b5c4dbb87298c9baedf66e`  
		Last Modified: Fri, 23 Jul 2021 11:12:09 GMT  
		Size: 2.5 MB (2542546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe2b1704c38fcd44f73cfa4cd5ed3ee7c7c9182e905d3bda2bad7457e7478f2`  
		Last Modified: Fri, 23 Jul 2021 11:12:15 GMT  
		Size: 60.1 MB (60148250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0011d8346df5b8d0b6540960e13a4a200f5fd7cd2283b3d0c7e0e3d61856f2c5`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; arm variant v5

```console
$ docker pull redmine@sha256:f68b890b9070068d1d1e4d2e129b6a2588f712889ef062ee4ba10ed3208024de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194719441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb736ee279c270380b4ea5b0c9aeef3d9e76b9e17b589c178f12c5e569445a2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:39:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:39:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 14:39:29 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 15:01:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:02:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:02:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:02:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:02:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:02:04 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 01:32:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 01:40:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 01:40:50 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 01:40:51 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 01:40:51 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 01:40:53 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 01:40:53 GMT
ENV REDMINE_VERSION=4.0.9
# Fri, 23 Jul 2021 01:40:53 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Fri, 23 Jul 2021 01:40:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 01:47:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 01:47:02 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 01:47:02 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 01:47:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 01:47:03 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 01:47:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9237058b7c5120d5c6315b5d17a8c1d783be09a228b83772111ce9436c29d078`  
		Last Modified: Thu, 22 Jul 2021 15:15:34 GMT  
		Size: 10.3 MB (10345807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144b4344f580222d2fbc2f0d80fc139ab1a1ddb9a245b6073c41fdca9a93c23e`  
		Last Modified: Thu, 22 Jul 2021 15:15:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae149ea188f1e064a0256560e0273ae4b331a42ab93326fd9a79753cfb63299d`  
		Last Modified: Thu, 22 Jul 2021 15:18:00 GMT  
		Size: 20.7 MB (20733368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5d2d97d7d53265f79bb7d6b5cfc05f237e3d237d9cf22475536aa4fd57ccde`  
		Last Modified: Thu, 22 Jul 2021 15:17:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822c77937c7bc9bc3d506cf3a12ef2ada0bdbc4c0db3af2efaecc31c4191df4a`  
		Last Modified: Fri, 23 Jul 2021 01:49:24 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf88d0b525291c8ed7e29e9e8ba21a25a8c186e2b45bbe036f6b45b60dbb725`  
		Last Modified: Fri, 23 Jul 2021 01:51:32 GMT  
		Size: 77.0 MB (76965230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259fc97807986ce68b1adaf43768244b0f7feb0b45a3693494d303a9bde78206`  
		Last Modified: Fri, 23 Jul 2021 01:50:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da90621c3344a001d962d4e9ee37ee08502d9a1d4c1a26e40082177f7d78eb9`  
		Last Modified: Fri, 23 Jul 2021 01:50:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6d126519049a526572ad6fbdff768305806b6cf0b42a0707007187491835a6`  
		Last Modified: Fri, 23 Jul 2021 01:50:43 GMT  
		Size: 2.5 MB (2542540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8457820c2404a0f956447bb7bde617741101e1b6ac11c79c7dc9e4ba284f06fb`  
		Last Modified: Fri, 23 Jul 2021 01:51:09 GMT  
		Size: 59.2 MB (59249171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae53e60f882218b768c0d7ea4a5a40fbe5512f79710f794079f92caa7a225d1`  
		Last Modified: Fri, 23 Jul 2021 01:50:40 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; arm variant v7

```console
$ docker pull redmine@sha256:adaecf942bcbf470ce5a40970bf2c079bcdcc70921efddada7897d7966c86313
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188053580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afae75ed20002c892916b188691ea63f8643a55ed5c8b26670d0ad3c396ed670`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:15:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 02:15:46 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 02:46:35 GMT
ENV RUBY_MAJOR=2.6
# Fri, 23 Jul 2021 02:46:35 GMT
ENV RUBY_VERSION=2.6.8
# Fri, 23 Jul 2021 02:46:36 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Fri, 23 Jul 2021 02:50:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 02:50:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 02:50:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 02:50:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 02:50:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 02:50:43 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 21:25:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 21:33:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 21:33:10 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 21:33:11 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 21:33:11 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 21:33:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 21:33:13 GMT
ENV REDMINE_VERSION=4.0.9
# Fri, 23 Jul 2021 21:33:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Fri, 23 Jul 2021 21:33:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 21:38:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 21:38:54 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 21:38:55 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 21:38:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 21:38:56 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 21:38:56 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b8c791d70de7f22816846fbb07e0a1d7d419841c7e539a7cf57ef05fd50c5`  
		Last Modified: Fri, 23 Jul 2021 03:05:10 GMT  
		Size: 9.9 MB (9872218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb12a7edb0af862efa24dc389d7901cd2a894f2e106a1cef931ba0a6d675e2c0`  
		Last Modified: Fri, 23 Jul 2021 03:05:04 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0837e4e34dc8fe0ec9567b99bb7b1397a813fca3b43abfbbd75ee231a946a979`  
		Last Modified: Fri, 23 Jul 2021 03:07:54 GMT  
		Size: 20.6 MB (20643760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c76309d8689f06c398ddc0f6b5ec99a408c65c613d73d63fb9f5101ebe3e2a1`  
		Last Modified: Fri, 23 Jul 2021 03:07:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c349a607ae692434577c905a1f4029d996cee89a0c9f214fa866ac935ceddf23`  
		Last Modified: Fri, 23 Jul 2021 21:41:16 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8cee36193dcad9a6170ac7b62624990e45bd8e40f280263cbc385102b815b5`  
		Last Modified: Fri, 23 Jul 2021 21:43:15 GMT  
		Size: 73.3 MB (73264161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51cab5b19ebed7ef72637004e6d5caa4c8e6339b68a5858b092f7969de48022`  
		Last Modified: Fri, 23 Jul 2021 21:42:27 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aa70a44bb3a34cdec8010dc14c194820f60d59bb588e122bb488dc1c65dc40`  
		Last Modified: Fri, 23 Jul 2021 21:42:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f27c773a3f3c9a852c5331d84ab63be28de904da75fa384a2b36a9ebc45b27`  
		Last Modified: Fri, 23 Jul 2021 21:42:31 GMT  
		Size: 2.5 MB (2542541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ac45246d6c17b1fb3dd54ad65b762e50f7ca0eb448a4137ada4f6896ef5925`  
		Last Modified: Fri, 23 Jul 2021 21:42:55 GMT  
		Size: 59.0 MB (58980689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a33b1a2d4b8fa224e96757684c0e214ff8c5922ab1ca4606c39b3ee25dcadfd`  
		Last Modified: Fri, 23 Jul 2021 21:42:27 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b88759af15842d0592a9ea5f67a803fd6ac33252a035ab554e88098f02574b52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 MB (200850483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43460e0a84b844270c94cae84bf674b95dd7fc307754fe931011e927e98abd47`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:11:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:25:18 GMT
ENV RUBY_MAJOR=2.6
# Tue, 17 Aug 2021 04:25:19 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 17 Aug 2021 04:25:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 17 Aug 2021 04:27:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:27:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:27:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:27:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:27:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:27:26 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 14:19:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 14:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:23:16 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 14:23:16 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 14:23:16 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 14:23:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 14:23:17 GMT
ENV REDMINE_VERSION=4.0.9
# Tue, 17 Aug 2021 14:23:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Tue, 17 Aug 2021 14:23:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 14:25:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:25:43 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 14:25:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 14:25:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:25:44 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:25:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ab80b058f00336b15786a8d20ce50706c5277560dc1ddb487b7e5c9d24b10`  
		Last Modified: Tue, 17 Aug 2021 04:34:12 GMT  
		Size: 11.3 MB (11263042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6eb72cd750a3e09673b73506f2a2ce24b3006d1773293eb65b72c9a2cdf7190`  
		Last Modified: Tue, 17 Aug 2021 04:34:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a741dfbe27573196b9f78f97eb7f35b06eaff990866fb7f894987974bd3f6d`  
		Last Modified: Tue, 17 Aug 2021 04:36:41 GMT  
		Size: 21.3 MB (21309045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6991754b0a79718bf8ab6c058b0ca4e091450b59072ac29e34401525b4337cc2`  
		Last Modified: Tue, 17 Aug 2021 04:36:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b2d6fcce3e7c045cbcf366963f15eecf60f206a0f9affdb4be5f3e1cdb8e58`  
		Last Modified: Tue, 17 Aug 2021 14:26:56 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39391463d0169869babe67051e72a4badb5e6538463aa13476d59709b2d1627a`  
		Last Modified: Tue, 17 Aug 2021 14:27:39 GMT  
		Size: 79.7 MB (79749184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bd4702d9b260665631a6e852231aba7fd3ba3322e443a969edb1d5f08f7196`  
		Last Modified: Tue, 17 Aug 2021 14:27:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93416b8e64e921655341d941d209345e030b91a533d8ffb233ece46312f04886`  
		Last Modified: Tue, 17 Aug 2021 14:27:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a29700d7f8864656fe98ec815952adea82a0cc692c4d47e68902625234b455f`  
		Last Modified: Tue, 17 Aug 2021 14:27:25 GMT  
		Size: 2.5 MB (2542545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb789346c1b22068ac9ec84aa33e715bb1529ef95da7ab381f8775aadeb83ff`  
		Last Modified: Tue, 17 Aug 2021 14:27:32 GMT  
		Size: 60.1 MB (60067351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd11b2bf406e2bdcdb6a7e80ab2722c7b56c44677f10548b9d342d2c88669302`  
		Last Modified: Tue, 17 Aug 2021 14:27:24 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; 386

```console
$ docker pull redmine@sha256:9b4b725043561fc6f093b1805ecf81bd81c278ff9900fe39a00e413d9864647c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210332451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21c08cabd048f1e2a1a723cb64800b532c989486494956a12e85e74c7cbd805`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:39:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 15:39:00 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:53:08 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 15:56:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:56:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:56:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:56:29 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 00:13:48 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 00:17:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:17:17 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 00:17:18 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 00:17:18 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 00:17:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 00:17:20 GMT
ENV REDMINE_VERSION=4.0.9
# Fri, 23 Jul 2021 00:17:21 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Fri, 23 Jul 2021 00:17:27 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 00:21:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 00:21:42 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 00:21:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 00:21:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 00:21:44 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 00:21:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071d04ca5200ad3b98494cfde36960022dbd29c9afc33d685ac499fae8a05d63`  
		Last Modified: Thu, 22 Jul 2021 16:06:57 GMT  
		Size: 17.2 MB (17227285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d9d06c9e919afbd9358b702cad5bc0f28b8150722ffedb25ece16dc1f19b2`  
		Last Modified: Thu, 22 Jul 2021 16:06:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3172650cf56a46da1b8438a86468d4053edf77c17eaad06d10b7c7a4f89d13ff`  
		Last Modified: Thu, 22 Jul 2021 16:09:12 GMT  
		Size: 20.9 MB (20910118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686761ac4b88297af44e82ba027c5c73411fe3e728b11bbdc631ea19cae4207`  
		Last Modified: Thu, 22 Jul 2021 16:09:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd85881cfa469c977c54673a6f7a5069bd5524e91c3dcc68765e8c34126cabe2`  
		Last Modified: Fri, 23 Jul 2021 00:23:41 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50e9554d325af14ff7a934082d622c3943218047ed2aa4294b0c7535581244b`  
		Last Modified: Fri, 23 Jul 2021 00:25:08 GMT  
		Size: 82.6 MB (82599806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a2d230fb36dab9b19e500fa31f006d0eeee505ceff2925ba4be6e11f79e7cb`  
		Last Modified: Fri, 23 Jul 2021 00:24:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab5662ff0e835add5c4df375cbd7a031f48ab605541cefdee4c0d951b6a724`  
		Last Modified: Fri, 23 Jul 2021 00:24:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fb67e4236a41bcff9cbb8e3a50fb0448092b2e9c48698898fd97c9be5596d6`  
		Last Modified: Fri, 23 Jul 2021 00:24:35 GMT  
		Size: 2.5 MB (2542547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce6344df4fd2a77ff42e131656f0ecabf7e82245e9baa99c29bbd0d0f746fbf`  
		Last Modified: Fri, 23 Jul 2021 00:24:54 GMT  
		Size: 59.3 MB (59251004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9705ef65a1f1f76bc1e8bc800dc07a0a770e8e1bf07b138f90cf1d3126ba5f38`  
		Last Modified: Fri, 23 Jul 2021 00:24:33 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; ppc64le

```console
$ docker pull redmine@sha256:f66f4634bf1585887b6cadeb8646989343e1ee4c44a136cd20edbe611d29e44d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216453624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9be8237ffe8a0fb25d3069a58c72db83381976bcc3b21b0c9815de1b8edca92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 00:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 00:33:06 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 01:11:31 GMT
ENV RUBY_MAJOR=2.6
# Fri, 23 Jul 2021 01:11:38 GMT
ENV RUBY_VERSION=2.6.8
# Fri, 23 Jul 2021 01:11:44 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Fri, 23 Jul 2021 01:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 01:26:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 01:26:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 01:26:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 01:26:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 01:26:59 GMT
CMD ["irb"]
# Sat, 24 Jul 2021 02:51:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sat, 24 Jul 2021 03:14:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Jul 2021 03:14:23 GMT
ENV RAILS_ENV=production
# Sat, 24 Jul 2021 03:14:25 GMT
WORKDIR /usr/src/redmine
# Sat, 24 Jul 2021 03:14:30 GMT
ENV HOME=/home/redmine
# Sat, 24 Jul 2021 03:14:38 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 24 Jul 2021 03:14:46 GMT
ENV REDMINE_VERSION=4.0.9
# Sat, 24 Jul 2021 03:14:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Sat, 24 Jul 2021 03:15:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 24 Jul 2021 03:35:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 24 Jul 2021 03:35:13 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 24 Jul 2021 03:35:17 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Sat, 24 Jul 2021 03:35:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 24 Jul 2021 03:35:27 GMT
EXPOSE 3000
# Sat, 24 Jul 2021 03:35:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f17b372a9c9122b881c2d22680e91d78ef4c329094595c61f5acb2523f41b7`  
		Last Modified: Fri, 23 Jul 2021 01:35:00 GMT  
		Size: 12.7 MB (12704330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064c16cae6894266abd8c9d33cfb671a4ebb2705d8b8bb7495bafc50c3dcd344`  
		Last Modified: Fri, 23 Jul 2021 01:34:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33960675014a7e56a0cf9f85e256ec6cce1c710723a7cd8f64935709d00e323d`  
		Last Modified: Fri, 23 Jul 2021 01:38:17 GMT  
		Size: 22.0 MB (21985713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047ee7c416fdfdb76a18bc7d50d5c00c1568b5e197242760391ce18bec14da13`  
		Last Modified: Fri, 23 Jul 2021 01:38:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c93f3da9b7a0eaf5df16b7b32a686296eaa146856420c2ce2d9ee2ad916121`  
		Last Modified: Sat, 24 Jul 2021 03:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf10994c116f970b482c990a6b89a17d4292257aa8d4c8f112785b16d9683b77`  
		Last Modified: Sat, 24 Jul 2021 03:37:45 GMT  
		Size: 87.9 MB (87901004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbc18e39a895f554cc9e72fb3f4f8fd6e3f14b8ba82bd4e555e33eab6e1e53c`  
		Last Modified: Sat, 24 Jul 2021 03:37:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e987abb4c826ab5b57ae49bcd75a9f15613c83d87e0677a62c4a11a1e60997`  
		Last Modified: Sat, 24 Jul 2021 03:37:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70618bee2d6cbdd87a9143949d8b3b252e21aa336af80a651853bfeac299ccb1`  
		Last Modified: Sat, 24 Jul 2021 03:37:26 GMT  
		Size: 2.5 MB (2542542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a66220dec1e7b2bd2bdba148f204920c16e19c11be7ac1000b3a337d3b3f0b`  
		Last Modified: Sat, 24 Jul 2021 03:37:35 GMT  
		Size: 60.8 MB (60762081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2192580103ba2e9b41655dfdbd0ed3800350febf95cbdba890bb38b2f9d12bc0`  
		Last Modified: Sat, 24 Jul 2021 03:37:25 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; s390x

```console
$ docker pull redmine@sha256:d328d900e9b6cb797ed448f67b29841ed5cf8a4c3832bba7fc865e60bd8eaacb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200270811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1f10c0616a1c38940f42bed4e642ccdd9226b8d89fc62b6e3e4dabcc41355e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:21:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:21:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:54:27 GMT
ENV RUBY_MAJOR=2.6
# Tue, 17 Aug 2021 04:54:28 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 17 Aug 2021 04:54:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 17 Aug 2021 04:57:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:57:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:57:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:57:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:57:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:57:43 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 13:35:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 13:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 13:39:00 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 13:39:01 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 13:39:01 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 13:39:02 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 13:39:03 GMT
ENV REDMINE_VERSION=4.0.9
# Tue, 17 Aug 2021 13:39:03 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Tue, 17 Aug 2021 13:39:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 13:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 13:41:36 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 13:41:36 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 13:41:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 13:41:36 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 13:41:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c03f413a15f7a98caaa2b027613636c576e3d98d8e1a98805c5978f2cc985f`  
		Last Modified: Tue, 17 Aug 2021 05:03:55 GMT  
		Size: 10.8 MB (10814401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ded0951dc51ddc1b38edf558277fec87d4169c1607312f67af2c4ffb9c4f19`  
		Last Modified: Tue, 17 Aug 2021 05:03:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b5f065983b815df03f5d378b737ce8b8950a6f775907f64c8d9413edfec507`  
		Last Modified: Tue, 17 Aug 2021 05:05:31 GMT  
		Size: 21.6 MB (21620194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c23b68c30a72cdc95043eff33b8ac51682c16759a2f483c8f4255db0f287c2`  
		Last Modified: Tue, 17 Aug 2021 05:05:28 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04534d357d558a08a4aea1da302e17954529ebf3804b4a0fe94cff2edac70b48`  
		Last Modified: Tue, 17 Aug 2021 13:42:39 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218be0290ec79b3f04e7f77dfe8f8ac8cbd9201826ad01308fcbadb25a5e6a77`  
		Last Modified: Tue, 17 Aug 2021 13:43:11 GMT  
		Size: 78.9 MB (78942684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2fac95700e00653babfdc8d8adf7f68e3bad29e80fa48749640f683e194389`  
		Last Modified: Tue, 17 Aug 2021 13:43:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ced46f2f9e40ad3ad2fbf664f2e2e2602d4d28bfe90a309a0f825cf0fca8b5`  
		Last Modified: Tue, 17 Aug 2021 13:43:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f2b73b065f8dcb4e9e6dffcbe73867f941480ca0a5d80811e345039ff4105e`  
		Last Modified: Tue, 17 Aug 2021 13:43:00 GMT  
		Size: 2.5 MB (2542549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28def5e72cbe09aa3df74f8671867014e00dbab04acaaf0216d648662c3ced87`  
		Last Modified: Tue, 17 Aug 2021 13:43:06 GMT  
		Size: 60.6 MB (60585884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902db45741704beb098e03501c7e36acd54a48c9891229a213037876e70978d7`  
		Last Modified: Tue, 17 Aug 2021 13:42:59 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.9-alpine`

```console
$ docker pull redmine@sha256:9b8ec4df56622e6060cfc701a5059050c3b734da828cc8f154367d016ac22227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0.9-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:baed7be679b02ee2f252035dbc06e0fed257f026688a9fe3da3832b0bf54ae51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153900570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69f8d92df2e7210bf95dfe2b409c178cacd6767792bbca288c47ff774f5e817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 08 Jul 2021 21:57:27 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 08 Jul 2021 21:57:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 08 Jul 2021 21:57:30 GMT
ENV LANG=C.UTF-8
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_MAJOR=2.6
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 08 Jul 2021 22:35:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 22:35:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 22:35:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 22:35:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 22:35:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 22:35:59 GMT
CMD ["irb"]
# Wed, 14 Jul 2021 20:26:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 14 Jul 2021 20:32:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Wed, 14 Jul 2021 20:32:28 GMT
ENV RAILS_ENV=production
# Wed, 14 Jul 2021 20:32:28 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jul 2021 20:32:29 GMT
ENV HOME=/home/redmine
# Wed, 14 Jul 2021 20:32:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 14 Jul 2021 20:32:30 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 14 Jul 2021 20:32:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 14 Jul 2021 20:32:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 14 Jul 2021 20:32:34 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 14 Jul 2021 20:34:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 14 Jul 2021 20:34:03 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 14 Jul 2021 20:34:04 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Wed, 14 Jul 2021 20:34:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jul 2021 20:34:04 GMT
EXPOSE 3000
# Wed, 14 Jul 2021 20:34:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5b0ea69e9ed42c49b5af449b703a12a4d2f2e28d87905af6fcd903fdae5689`  
		Last Modified: Thu, 08 Jul 2021 22:38:46 GMT  
		Size: 3.6 MB (3581658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad656ed833315b61ea674706f32c2d18d7412c7120926442af57b9131ee72ee`  
		Last Modified: Thu, 08 Jul 2021 22:38:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9d07bc1851494b8935d8593efecfea98e2c4a4ff1c3eaf2e5319eb31cb3a2`  
		Last Modified: Thu, 08 Jul 2021 22:41:47 GMT  
		Size: 19.9 MB (19889336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d50c8fd3318db7f0dbb1d50a8aa4e571ae4926440e66c07be861dd4685211d`  
		Last Modified: Thu, 08 Jul 2021 22:41:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e030b8560a875bcd9c87e7dd1c8faf94a9d48cf039ee0bf125017750cc802b`  
		Last Modified: Wed, 14 Jul 2021 20:37:07 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f9541899ba9d0a6bde1aaa23a83e1e1cd6a17fc0adecb390591f66b0ccb93b`  
		Last Modified: Wed, 14 Jul 2021 20:38:23 GMT  
		Size: 66.2 MB (66172712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bc115e3ba6c2cb414f0bb5c4df5c0dad6b57442cf9044bbe1fc33e266821b4`  
		Last Modified: Wed, 14 Jul 2021 20:38:08 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0bf51497625cb7774642f214c3424e7a0e97dff3e9c1c7e96c279d965e3981`  
		Last Modified: Wed, 14 Jul 2021 20:38:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d58772bc79f2753b31d538e035d07bd09bb2731fc4843259e09b0c4be77e2f9`  
		Last Modified: Wed, 14 Jul 2021 20:38:10 GMT  
		Size: 2.5 MB (2543757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f9be46406ca851c437e457fa10b35fea3c15bda96b4f315f9514efea879beb`  
		Last Modified: Wed, 14 Jul 2021 20:38:15 GMT  
		Size: 58.9 MB (58897408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad779a0b33ba3ea1e31e4a1ee1c8bab4546aadacd48d0fb32d05adc26c02906`  
		Last Modified: Wed, 14 Jul 2021 20:38:08 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.9-passenger`

```console
$ docker pull redmine@sha256:319dd08d03106ba06b96a6c2c211c7bdbdf6671de495c0b1a1e270098bf3cb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0.9-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:0d1a0ccbcaa59efb65e98fbf387d0cf046cb38a46c274cb0e25ca9e2aa13d165
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231318767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c59b0c8114ee55abb9152e916fd05b8ced427af548ff6d169917a286874784`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 17:31:25 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 17:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:34:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:34:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:34:07 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:05:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:07:36 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:07:36 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:07:37 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:07:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 23 Jul 2021 11:07:38 GMT
ENV REDMINE_VERSION=4.0.9
# Fri, 23 Jul 2021 11:07:38 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Fri, 23 Jul 2021 11:07:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 23 Jul 2021 11:09:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 11:09:35 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 23 Jul 2021 11:09:35 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 23 Jul 2021 11:09:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Jul 2021 11:09:35 GMT
EXPOSE 3000
# Fri, 23 Jul 2021 11:09:36 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 23 Jul 2021 11:09:39 GMT
ENV PASSENGER_VERSION=6.0.10
# Fri, 23 Jul 2021 11:09:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 23 Jul 2021 11:09:57 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Fri, 23 Jul 2021 11:09:57 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Fri, 23 Jul 2021 11:09:58 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b7373cf9d9195064da3c92860c7157644c595720fffd5bb48615ac96985d5`  
		Last Modified: Thu, 22 Jul 2021 17:43:38 GMT  
		Size: 21.5 MB (21468044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb83e25b0fb68c5c98194adb0ad3740bc7d2242801c213e7d7949281f901679`  
		Last Modified: Thu, 22 Jul 2021 17:43:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61371aadcf232eb667c47dbba436a5611088d97ba4c8a9bd0c271f36882b027d`  
		Last Modified: Fri, 23 Jul 2021 11:11:30 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527440fec380cb5ffab3044cdb10895391dd8c0967dbf50c94f5a6ac54cbe48`  
		Last Modified: Fri, 23 Jul 2021 11:12:23 GMT  
		Size: 81.2 MB (81200505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ead518ac18671d74e03ee9c8d93c71f9ced66c21ba86bcc2c503a8e5c8326b`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f008d376270911f79e7e6c177b16b77b13d0309adcd8dd7266e1bf0b2b4dd9`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9566b0985629bf3ebfee385cb50b88bb50798e5ae4b5c4dbb87298c9baedf66e`  
		Last Modified: Fri, 23 Jul 2021 11:12:09 GMT  
		Size: 2.5 MB (2542546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe2b1704c38fcd44f73cfa4cd5ed3ee7c7c9182e905d3bda2bad7457e7478f2`  
		Last Modified: Fri, 23 Jul 2021 11:12:15 GMT  
		Size: 60.1 MB (60148250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0011d8346df5b8d0b6540960e13a4a200f5fd7cd2283b3d0c7e0e3d61856f2c5`  
		Last Modified: Fri, 23 Jul 2021 11:12:08 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4115f43d92079ea0e1fd41e8d42467fc73d3b96a655e7eeaf1ceed99049832cf`  
		Last Modified: Fri, 23 Jul 2021 11:12:37 GMT  
		Size: 21.3 MB (21327322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923adc728211126334159e16d7a0931ea37967801e506f3f0eb071d26ced3762`  
		Last Modified: Fri, 23 Jul 2021 11:12:35 GMT  
		Size: 4.9 MB (4919285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1`

```console
$ docker pull redmine@sha256:a29907f5967562cf8b1c9111dbf4a19e2b25a135ab7b211794876ea75d595903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.1` - linux; amd64

```console
$ docker pull redmine@sha256:d9cce15565736aab1f4db6c7ca03a60a7421a2562941e1dbf7d045cfede3f10f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206651136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd1bbd7d315847a1fea45b79faf80abd0b4310e95d3652b088f6acf6caca394`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 17:31:25 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 17:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:34:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:34:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:34:07 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:05:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:05:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:05:50 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:05:50 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:05:50 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:05:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:29:26 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 19:29:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 19:29:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:30:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:30:08 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:30:09 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:30:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:30:09 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:30:09 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b7373cf9d9195064da3c92860c7157644c595720fffd5bb48615ac96985d5`  
		Last Modified: Thu, 22 Jul 2021 17:43:38 GMT  
		Size: 21.5 MB (21468044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb83e25b0fb68c5c98194adb0ad3740bc7d2242801c213e7d7949281f901679`  
		Last Modified: Thu, 22 Jul 2021 17:43:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61371aadcf232eb667c47dbba436a5611088d97ba4c8a9bd0c271f36882b027d`  
		Last Modified: Fri, 23 Jul 2021 11:11:30 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfd1dde1f32f7f8409959b4663cf89b722a2f427f544c5acf3c4dca5ba89961`  
		Last Modified: Fri, 23 Jul 2021 11:11:43 GMT  
		Size: 94.1 MB (94088300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216270a0114d5886d784b5a4bd95e0270c48d34e26e20ced7ee30251aecc0235`  
		Last Modified: Fri, 23 Jul 2021 11:11:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0835bd828414f95e3e7358066f88a9b754de0e89b47c431fd9eb5f61f4143`  
		Last Modified: Fri, 23 Jul 2021 11:11:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b607a9ed17bf183fba2f9dccf4bb87e2761cc9bec5cfb9b0075a65a6bcb3fbfa`  
		Last Modified: Mon, 02 Aug 2021 19:34:26 GMT  
		Size: 2.7 MB (2749052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0160648d960a2454964d3b9064d49d65a50bb41c534dbc2981c1d75ffb53f1f3`  
		Last Modified: Mon, 02 Aug 2021 19:34:31 GMT  
		Size: 48.6 MB (48632927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2ce4148d6e5ad123e1ed4f5fab2dc2ad17c411e17d178811ac1d5e9607ea69`  
		Last Modified: Mon, 02 Aug 2021 19:34:27 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm variant v5

```console
$ docker pull redmine@sha256:4bdd1675075975131a250540a53f8880f1e0fae8b29cfbc67ddab10f6586177b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210666390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcbb5833331e6445ac71ddc434c6a915315e32f215e0d6bc5929c81cd521053`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:39:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:39:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 14:39:29 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 15:01:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:02:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:02:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:02:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:02:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:02:04 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 01:32:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 01:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 01:33:37 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 01:33:37 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 01:33:38 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 01:33:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 21:04:50 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 21:04:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 21:04:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 21:10:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 21:10:36 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 21:10:37 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 21:10:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 21:10:38 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 21:10:38 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9237058b7c5120d5c6315b5d17a8c1d783be09a228b83772111ce9436c29d078`  
		Last Modified: Thu, 22 Jul 2021 15:15:34 GMT  
		Size: 10.3 MB (10345807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144b4344f580222d2fbc2f0d80fc139ab1a1ddb9a245b6073c41fdca9a93c23e`  
		Last Modified: Thu, 22 Jul 2021 15:15:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae149ea188f1e064a0256560e0273ae4b331a42ab93326fd9a79753cfb63299d`  
		Last Modified: Thu, 22 Jul 2021 15:18:00 GMT  
		Size: 20.7 MB (20733368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5d2d97d7d53265f79bb7d6b5cfc05f237e3d237d9cf22475536aa4fd57ccde`  
		Last Modified: Thu, 22 Jul 2021 15:17:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822c77937c7bc9bc3d506cf3a12ef2ada0bdbc4c0db3af2efaecc31c4191df4a`  
		Last Modified: Fri, 23 Jul 2021 01:49:24 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c50724a36d3c9a8b9ceae430de242d7f6969dbef3ac25c5fde473a8b062cd3`  
		Last Modified: Fri, 23 Jul 2021 01:50:25 GMT  
		Size: 89.6 MB (89576586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64ad6c53bf00acadba6df300f7a60ca8ae5ddc2336b37cd556bbcc18d26566c`  
		Last Modified: Fri, 23 Jul 2021 01:49:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f057554e99e7143804c2bfa6e4ad7c04cbf19075e611550a34de736734ec41c3`  
		Last Modified: Fri, 23 Jul 2021 01:49:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f864c8ca3715d87914498c4905365f0ed5cbf5e0cb26b9c639534a5511833b`  
		Last Modified: Mon, 02 Aug 2021 21:12:29 GMT  
		Size: 2.7 MB (2749054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4019d3cb4be9309f4cb0baa969bf37dfa6c525ade166c631d7b406cd8a3e59e4`  
		Last Modified: Mon, 02 Aug 2021 21:12:55 GMT  
		Size: 62.4 MB (62378250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564d2b0e0b86ccd1d38a66825b3d86b65542b19b9b749dd197dcf78fa771f039`  
		Last Modified: Mon, 02 Aug 2021 21:12:26 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm variant v7

```console
$ docker pull redmine@sha256:be260e0859e1639be25cf06cbe19352b4fb385c4942632e35f1558ddda888805
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203843857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f5b264322abd1cb8a7edae6550cf4a9952aa25db98c9a76125dd5ca9d1a94a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:15:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 02:15:46 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 02:46:35 GMT
ENV RUBY_MAJOR=2.6
# Fri, 23 Jul 2021 02:46:35 GMT
ENV RUBY_VERSION=2.6.8
# Fri, 23 Jul 2021 02:46:36 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Fri, 23 Jul 2021 02:50:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 02:50:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 02:50:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 02:50:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 02:50:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 02:50:43 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 21:25:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 21:26:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 21:26:28 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 21:26:29 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 21:26:29 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 21:26:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 03 Aug 2021 00:06:22 GMT
ENV REDMINE_VERSION=4.1.4
# Tue, 03 Aug 2021 00:06:23 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Tue, 03 Aug 2021 00:06:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 03 Aug 2021 00:11:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 03 Aug 2021 00:11:46 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 03 Aug 2021 00:11:47 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 03 Aug 2021 00:11:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Aug 2021 00:11:48 GMT
EXPOSE 3000
# Tue, 03 Aug 2021 00:11:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b8c791d70de7f22816846fbb07e0a1d7d419841c7e539a7cf57ef05fd50c5`  
		Last Modified: Fri, 23 Jul 2021 03:05:10 GMT  
		Size: 9.9 MB (9872218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb12a7edb0af862efa24dc389d7901cd2a894f2e106a1cef931ba0a6d675e2c0`  
		Last Modified: Fri, 23 Jul 2021 03:05:04 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0837e4e34dc8fe0ec9567b99bb7b1397a813fca3b43abfbbd75ee231a946a979`  
		Last Modified: Fri, 23 Jul 2021 03:07:54 GMT  
		Size: 20.6 MB (20643760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c76309d8689f06c398ddc0f6b5ec99a408c65c613d73d63fb9f5101ebe3e2a1`  
		Last Modified: Fri, 23 Jul 2021 03:07:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c349a607ae692434577c905a1f4029d996cee89a0c9f214fa866ac935ceddf23`  
		Last Modified: Fri, 23 Jul 2021 21:41:16 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2880a64f27ab57a09b4f72db20fc36a50bf3b6a6f3475f8661e8184e4b8acb99`  
		Last Modified: Fri, 23 Jul 2021 21:42:11 GMT  
		Size: 85.6 MB (85590430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455a681e485f6469d2ea0559f66edfbdf6ea359e79d4a5db42bf76287a0de434`  
		Last Modified: Fri, 23 Jul 2021 21:41:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac534a0a817b7f2f9c1f1e31c139ea1f9375a72e0f485b0383bc4fc4d59fd2a`  
		Last Modified: Fri, 23 Jul 2021 21:41:14 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c129690336fa4b91fdd3354d450f70c1d503241b4f996e45a06f6cc7c5c33c8e`  
		Last Modified: Tue, 03 Aug 2021 00:13:31 GMT  
		Size: 2.7 MB (2749050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fe83cafb9bc610bb800a4c85956caaac9219e0f8a9d3c4c4951568fbaf45a4`  
		Last Modified: Tue, 03 Aug 2021 00:13:56 GMT  
		Size: 62.2 MB (62238188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8821dd99090d5f0c3476a0eabbcb4ec9b51cd0954272e8f5443c04ab694180f`  
		Last Modified: Tue, 03 Aug 2021 00:13:27 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:4d2eef074194f45decdf5b1b4a3166169b18038058b325f0d0862dbf58e89de1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217544129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43f88150f3bd00e9b27ca2fb50ae014489a41818c5674b2166dabae0c267a69`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:11:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:25:18 GMT
ENV RUBY_MAJOR=2.6
# Tue, 17 Aug 2021 04:25:19 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 17 Aug 2021 04:25:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 17 Aug 2021 04:27:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:27:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:27:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:27:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:27:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:27:26 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 14:19:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 14:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:20:21 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 14:20:21 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 14:20:21 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 14:20:22 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 14:20:22 GMT
ENV REDMINE_VERSION=4.1.4
# Tue, 17 Aug 2021 14:20:22 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Tue, 17 Aug 2021 14:20:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 14:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:22:50 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 14:22:50 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 14:22:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:22:50 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:22:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ab80b058f00336b15786a8d20ce50706c5277560dc1ddb487b7e5c9d24b10`  
		Last Modified: Tue, 17 Aug 2021 04:34:12 GMT  
		Size: 11.3 MB (11263042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6eb72cd750a3e09673b73506f2a2ce24b3006d1773293eb65b72c9a2cdf7190`  
		Last Modified: Tue, 17 Aug 2021 04:34:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a741dfbe27573196b9f78f97eb7f35b06eaff990866fb7f894987974bd3f6d`  
		Last Modified: Tue, 17 Aug 2021 04:36:41 GMT  
		Size: 21.3 MB (21309045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6991754b0a79718bf8ab6c058b0ca4e091450b59072ac29e34401525b4337cc2`  
		Last Modified: Tue, 17 Aug 2021 04:36:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b2d6fcce3e7c045cbcf366963f15eecf60f206a0f9affdb4be5f3e1cdb8e58`  
		Last Modified: Tue, 17 Aug 2021 14:26:56 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fb70beab3eb9f346f19baeada6ab2ab16b85603c8269cd25ef07d34d7d3bbd`  
		Last Modified: Tue, 17 Aug 2021 14:27:12 GMT  
		Size: 92.6 MB (92610850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88949e39e9bf16adf106d42b5c92a9aa9f223ed09de640620dab986a37998467`  
		Last Modified: Tue, 17 Aug 2021 14:26:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8b01342158e6f70c8d6a1fb0a08d898843a76e9eaac116f8be7bf1cd5dc0ab`  
		Last Modified: Tue, 17 Aug 2021 14:26:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a92eed4532a610d931b5637079bd2beaf67787995446f363d81a4e9afb7304c`  
		Last Modified: Tue, 17 Aug 2021 14:26:55 GMT  
		Size: 2.7 MB (2749057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4658a1e88f9cf77366e04fc9ccacb6815390e8e23e32ba77a0e63a1307a797d5`  
		Last Modified: Tue, 17 Aug 2021 14:27:02 GMT  
		Size: 63.7 MB (63692816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd3201c15e0230dd813392cedf5401f39cafe6d75e2649301390105577ef545`  
		Last Modified: Tue, 17 Aug 2021 14:26:54 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; 386

```console
$ docker pull redmine@sha256:34c1de73f944be0d2b1aad3429ab5446bd8eb5f8fa9a6d9c6a2834e32009f2f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (213005139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31e81ffbd0f74a0e05d1b81a16f5590b48a3fea8852ccffb8e39da33177b98e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:39:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 15:39:00 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:53:08 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 15:56:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:56:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:56:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:56:29 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 00:13:48 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 00:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:14:41 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 00:14:42 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 00:14:42 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 00:14:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:54:34 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 23:54:34 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 23:54:38 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:55:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:55:25 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:55:26 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:55:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:55:26 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:55:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071d04ca5200ad3b98494cfde36960022dbd29c9afc33d685ac499fae8a05d63`  
		Last Modified: Thu, 22 Jul 2021 16:06:57 GMT  
		Size: 17.2 MB (17227285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d9d06c9e919afbd9358b702cad5bc0f28b8150722ffedb25ece16dc1f19b2`  
		Last Modified: Thu, 22 Jul 2021 16:06:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3172650cf56a46da1b8438a86468d4053edf77c17eaad06d10b7c7a4f89d13ff`  
		Last Modified: Thu, 22 Jul 2021 16:09:12 GMT  
		Size: 20.9 MB (20910118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686761ac4b88297af44e82ba027c5c73411fe3e728b11bbdc631ea19cae4207`  
		Last Modified: Thu, 22 Jul 2021 16:09:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd85881cfa469c977c54673a6f7a5069bd5524e91c3dcc68765e8c34126cabe2`  
		Last Modified: Fri, 23 Jul 2021 00:23:41 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceccbef720a55f3b84f4c45e8ebfdec613398d896ceb5e3e5eb289b29c9fc015`  
		Last Modified: Fri, 23 Jul 2021 00:24:18 GMT  
		Size: 95.7 MB (95703189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2780ce2bed1fed359a6ca6b2570df212412bf9869a7e43011fd9b1e2b174944`  
		Last Modified: Fri, 23 Jul 2021 00:23:39 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f156819ab7d2b648146a7ca9ccee6d402b080b6d4f0d598d5844ff1dcd229e09`  
		Last Modified: Fri, 23 Jul 2021 00:23:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68c428871e997596ca3bf8c8c41a6dd81f73aa3ceacccd5dd3dac68fe3bf2d2`  
		Last Modified: Mon, 02 Aug 2021 23:56:30 GMT  
		Size: 2.7 MB (2749061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672dc0c872867a2d4f39e506bc7a1ebf5d775df842e1756c4c2e90e83c7110d`  
		Last Modified: Mon, 02 Aug 2021 23:56:36 GMT  
		Size: 48.6 MB (48613795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811de41f951559285a2f0118abc2c4bfa0cfc320e2607a3b79eea7b056af6df`  
		Last Modified: Mon, 02 Aug 2021 23:56:29 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; ppc64le

```console
$ docker pull redmine@sha256:6efef148967595e8835c7ce456bbd96854bc5b5bde0f00aa661936d90794159d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234101779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537c3d32f7d409d0c29fbdb569f953787339bc40657e734c3348a1fb9679b5f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 00:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 00:33:06 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 01:11:31 GMT
ENV RUBY_MAJOR=2.6
# Fri, 23 Jul 2021 01:11:38 GMT
ENV RUBY_VERSION=2.6.8
# Fri, 23 Jul 2021 01:11:44 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Fri, 23 Jul 2021 01:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 01:26:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 01:26:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 01:26:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 01:26:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 01:26:59 GMT
CMD ["irb"]
# Sat, 24 Jul 2021 02:51:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sat, 24 Jul 2021 02:58:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Jul 2021 02:58:12 GMT
ENV RAILS_ENV=production
# Sat, 24 Jul 2021 02:58:18 GMT
WORKDIR /usr/src/redmine
# Sat, 24 Jul 2021 02:58:23 GMT
ENV HOME=/home/redmine
# Sat, 24 Jul 2021 02:58:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:23:57 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 23:24:02 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 23:24:16 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:29:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:29:34 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:29:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:29:42 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:29:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f17b372a9c9122b881c2d22680e91d78ef4c329094595c61f5acb2523f41b7`  
		Last Modified: Fri, 23 Jul 2021 01:35:00 GMT  
		Size: 12.7 MB (12704330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064c16cae6894266abd8c9d33cfb671a4ebb2705d8b8bb7495bafc50c3dcd344`  
		Last Modified: Fri, 23 Jul 2021 01:34:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33960675014a7e56a0cf9f85e256ec6cce1c710723a7cd8f64935709d00e323d`  
		Last Modified: Fri, 23 Jul 2021 01:38:17 GMT  
		Size: 22.0 MB (21985713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047ee7c416fdfdb76a18bc7d50d5c00c1568b5e197242760391ce18bec14da13`  
		Last Modified: Fri, 23 Jul 2021 01:38:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c93f3da9b7a0eaf5df16b7b32a686296eaa146856420c2ce2d9ee2ad916121`  
		Last Modified: Sat, 24 Jul 2021 03:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77867ad228284b5163a25c4a76739b9c38ecbf8984bbc696c8e354141fe6b00`  
		Last Modified: Sat, 24 Jul 2021 03:37:11 GMT  
		Size: 101.3 MB (101328215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1ee06db11cacc9daf59c75cefc28c1d232ac1e928afa7a6f43d367e10bd1f1`  
		Last Modified: Sat, 24 Jul 2021 03:36:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f85237d5d99063036b3bb2790b12d7cbce41850c87c2bfbff1db63e7f5c0aa`  
		Last Modified: Sat, 24 Jul 2021 03:36:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b41fd52ae5e75f49d10d154992d46e779d973647edbfc7cc463b8c08b43cf95`  
		Last Modified: Mon, 02 Aug 2021 23:30:58 GMT  
		Size: 2.7 MB (2749055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9579a8a24f91bac1182097cd9218c6eb23b0e16728c8a7fb9a8386b58daf180`  
		Last Modified: Mon, 02 Aug 2021 23:31:07 GMT  
		Size: 64.8 MB (64776514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fea5dde6960e18005f909bc4dcaff30bd2eff3054518e9b24d2fc72f25038e`  
		Last Modified: Mon, 02 Aug 2021 23:30:57 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; s390x

```console
$ docker pull redmine@sha256:5c79bd1a8590ca5bf82ec50e92e21512b07940797a1463edc9ddcf5fa9b56609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216904122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d385d903de9e3d8df431fcda401c63ff60e7c93ecd4adc587a0f18c0cec4b352`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:21:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:21:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:54:27 GMT
ENV RUBY_MAJOR=2.6
# Tue, 17 Aug 2021 04:54:28 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 17 Aug 2021 04:54:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 17 Aug 2021 04:57:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:57:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:57:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:57:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:57:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:57:43 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 13:35:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 13:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 13:36:30 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 13:36:31 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 13:36:31 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 13:36:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 13:36:32 GMT
ENV REDMINE_VERSION=4.1.4
# Tue, 17 Aug 2021 13:36:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Tue, 17 Aug 2021 13:36:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 13:38:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 13:38:20 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 13:38:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 13:38:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 13:38:20 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 13:38:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c03f413a15f7a98caaa2b027613636c576e3d98d8e1a98805c5978f2cc985f`  
		Last Modified: Tue, 17 Aug 2021 05:03:55 GMT  
		Size: 10.8 MB (10814401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ded0951dc51ddc1b38edf558277fec87d4169c1607312f67af2c4ffb9c4f19`  
		Last Modified: Tue, 17 Aug 2021 05:03:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b5f065983b815df03f5d378b737ce8b8950a6f775907f64c8d9413edfec507`  
		Last Modified: Tue, 17 Aug 2021 05:05:31 GMT  
		Size: 21.6 MB (21620194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c23b68c30a72cdc95043eff33b8ac51682c16759a2f483c8f4255db0f287c2`  
		Last Modified: Tue, 17 Aug 2021 05:05:28 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04534d357d558a08a4aea1da302e17954529ebf3804b4a0fe94cff2edac70b48`  
		Last Modified: Tue, 17 Aug 2021 13:42:39 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f89f5346ffb70bc7a8b15f07817f963fb0d00122dacff743cb5c1af76d9479`  
		Last Modified: Tue, 17 Aug 2021 13:42:51 GMT  
		Size: 91.8 MB (91789175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad842e06b48edaf468d80d1505a6ee1be7be796415dc006ca2d231db55e6b6a6`  
		Last Modified: Tue, 17 Aug 2021 13:42:37 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b320e5d26dc0c91fa46241087be2cc7e455bf87e055af14800bf2489c38c2452`  
		Last Modified: Tue, 17 Aug 2021 13:42:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636b36120f102a30afdee3f007c4c76c804f392476d0db0dfec249f4c7b8a7f`  
		Last Modified: Tue, 17 Aug 2021 13:42:37 GMT  
		Size: 2.7 MB (2749060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55ccb25470f9adf5b849f9a3d8fdd2393db99a602df8f5a9df60ddf284f94dd`  
		Last Modified: Tue, 17 Aug 2021 13:42:43 GMT  
		Size: 64.2 MB (64166193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126aa5be9c0306e584899b0604d54804c8fb7792dedca7cfce8c6a063d0cab14`  
		Last Modified: Tue, 17 Aug 2021 13:42:37 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1-alpine`

```console
$ docker pull redmine@sha256:75724ab6c055e0fb9d5c001b3e2ea96933739a169effd4d9dff712e0beec5c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:704c3fa30632908b58ecbb9d7dfddcbbd1729a16f5d17ce4f7fc3be03b731265
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161073890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c81718646cb9796cc83de16cb4c5cb35512859b54704d82c2d2c2aad4028d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 08 Jul 2021 21:57:27 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 08 Jul 2021 21:57:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 08 Jul 2021 21:57:30 GMT
ENV LANG=C.UTF-8
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_MAJOR=2.6
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 08 Jul 2021 22:35:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 22:35:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 22:35:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 22:35:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 22:35:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 22:35:59 GMT
CMD ["irb"]
# Wed, 14 Jul 2021 20:26:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 14 Jul 2021 20:26:45 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 14 Jul 2021 20:26:46 GMT
ENV RAILS_ENV=production
# Wed, 14 Jul 2021 20:26:46 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jul 2021 20:26:46 GMT
ENV HOME=/home/redmine
# Wed, 14 Jul 2021 20:26:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:30:38 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 19:30:38 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 19:30:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:30:41 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 02 Aug 2021 19:32:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Mon, 02 Aug 2021 19:32:43 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:32:43 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Mon, 02 Aug 2021 19:32:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:32:43 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:32:43 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5b0ea69e9ed42c49b5af449b703a12a4d2f2e28d87905af6fcd903fdae5689`  
		Last Modified: Thu, 08 Jul 2021 22:38:46 GMT  
		Size: 3.6 MB (3581658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad656ed833315b61ea674706f32c2d18d7412c7120926442af57b9131ee72ee`  
		Last Modified: Thu, 08 Jul 2021 22:38:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9d07bc1851494b8935d8593efecfea98e2c4a4ff1c3eaf2e5319eb31cb3a2`  
		Last Modified: Thu, 08 Jul 2021 22:41:47 GMT  
		Size: 19.9 MB (19889336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d50c8fd3318db7f0dbb1d50a8aa4e571ae4926440e66c07be861dd4685211d`  
		Last Modified: Thu, 08 Jul 2021 22:41:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e030b8560a875bcd9c87e7dd1c8faf94a9d48cf039ee0bf125017750cc802b`  
		Last Modified: Wed, 14 Jul 2021 20:37:07 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c0006aa2ad99f9ffc9d729323dc4d6fe56017cf11735d341570e65864f6425`  
		Last Modified: Wed, 14 Jul 2021 20:37:17 GMT  
		Size: 69.5 MB (69526405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde1c41e26debfed4512ebfbeb0a14368410a36df9e8a30216966c830eee17ad`  
		Last Modified: Wed, 14 Jul 2021 20:37:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968695fc5116055ee483a173dbd08fdd5e9aba5dea28a955cdc730ae9f0bba52`  
		Last Modified: Wed, 14 Jul 2021 20:37:04 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c82c1c8b2f323e74c94315a3f2612cfb3ccc41eb9f247db68ff0821e0e089ba`  
		Last Modified: Mon, 02 Aug 2021 19:34:56 GMT  
		Size: 2.7 MB (2749721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7662a67f83cd246151d8c35ba66c66751655e34aad0846285c1dfb5a0c63284a`  
		Last Modified: Mon, 02 Aug 2021 19:35:01 GMT  
		Size: 62.5 MB (62511071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8798eb314975e00365c070021fed0c5fcb4587d78e6a72432cef4f1f7974426a`  
		Last Modified: Mon, 02 Aug 2021 19:34:55 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1-passenger`

```console
$ docker pull redmine@sha256:5c6e20997f65ca9b448dd204a9876048d651859b7b1c5fb6b43e03fc76c96ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:2c81b66540bf9965be665f52cf1b0d64f64a56dbe812dab5f4232ef6e3aaa44b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232893079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025667f7cf28b19b6bc5b9f9b223e794ec8a85794144ca94fb067769b629d7e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 17:31:25 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 17:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:34:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:34:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:34:07 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:05:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:05:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:05:50 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:05:50 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:05:50 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:05:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:29:26 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 19:29:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 19:29:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:30:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:30:08 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:30:09 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:30:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:30:09 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:30:09 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Mon, 02 Aug 2021 19:30:16 GMT
ENV PASSENGER_VERSION=6.0.10
# Mon, 02 Aug 2021 19:30:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:30:34 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Mon, 02 Aug 2021 19:30:34 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Mon, 02 Aug 2021 19:30:34 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b7373cf9d9195064da3c92860c7157644c595720fffd5bb48615ac96985d5`  
		Last Modified: Thu, 22 Jul 2021 17:43:38 GMT  
		Size: 21.5 MB (21468044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb83e25b0fb68c5c98194adb0ad3740bc7d2242801c213e7d7949281f901679`  
		Last Modified: Thu, 22 Jul 2021 17:43:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61371aadcf232eb667c47dbba436a5611088d97ba4c8a9bd0c271f36882b027d`  
		Last Modified: Fri, 23 Jul 2021 11:11:30 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfd1dde1f32f7f8409959b4663cf89b722a2f427f544c5acf3c4dca5ba89961`  
		Last Modified: Fri, 23 Jul 2021 11:11:43 GMT  
		Size: 94.1 MB (94088300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216270a0114d5886d784b5a4bd95e0270c48d34e26e20ced7ee30251aecc0235`  
		Last Modified: Fri, 23 Jul 2021 11:11:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0835bd828414f95e3e7358066f88a9b754de0e89b47c431fd9eb5f61f4143`  
		Last Modified: Fri, 23 Jul 2021 11:11:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b607a9ed17bf183fba2f9dccf4bb87e2761cc9bec5cfb9b0075a65a6bcb3fbfa`  
		Last Modified: Mon, 02 Aug 2021 19:34:26 GMT  
		Size: 2.7 MB (2749052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0160648d960a2454964d3b9064d49d65a50bb41c534dbc2981c1d75ffb53f1f3`  
		Last Modified: Mon, 02 Aug 2021 19:34:31 GMT  
		Size: 48.6 MB (48632927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2ce4148d6e5ad123e1ed4f5fab2dc2ad17c411e17d178811ac1d5e9607ea69`  
		Last Modified: Mon, 02 Aug 2021 19:34:27 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1626dac6c4d9ff800fe35da237dabc193dbdc7f07135c5322d702b87da59fd3f`  
		Last Modified: Mon, 02 Aug 2021 19:34:45 GMT  
		Size: 21.3 MB (21322664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbf672985eb895d1057965b1448ea42f3c48ad6d94dbc25c415d08aaf6958e1`  
		Last Modified: Mon, 02 Aug 2021 19:34:43 GMT  
		Size: 4.9 MB (4919279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.4`

```console
$ docker pull redmine@sha256:a29907f5967562cf8b1c9111dbf4a19e2b25a135ab7b211794876ea75d595903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.1.4` - linux; amd64

```console
$ docker pull redmine@sha256:d9cce15565736aab1f4db6c7ca03a60a7421a2562941e1dbf7d045cfede3f10f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206651136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd1bbd7d315847a1fea45b79faf80abd0b4310e95d3652b088f6acf6caca394`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 17:31:25 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 17:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:34:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:34:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:34:07 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:05:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:05:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:05:50 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:05:50 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:05:50 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:05:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:29:26 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 19:29:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 19:29:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:30:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:30:08 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:30:09 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:30:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:30:09 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:30:09 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b7373cf9d9195064da3c92860c7157644c595720fffd5bb48615ac96985d5`  
		Last Modified: Thu, 22 Jul 2021 17:43:38 GMT  
		Size: 21.5 MB (21468044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb83e25b0fb68c5c98194adb0ad3740bc7d2242801c213e7d7949281f901679`  
		Last Modified: Thu, 22 Jul 2021 17:43:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61371aadcf232eb667c47dbba436a5611088d97ba4c8a9bd0c271f36882b027d`  
		Last Modified: Fri, 23 Jul 2021 11:11:30 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfd1dde1f32f7f8409959b4663cf89b722a2f427f544c5acf3c4dca5ba89961`  
		Last Modified: Fri, 23 Jul 2021 11:11:43 GMT  
		Size: 94.1 MB (94088300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216270a0114d5886d784b5a4bd95e0270c48d34e26e20ced7ee30251aecc0235`  
		Last Modified: Fri, 23 Jul 2021 11:11:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0835bd828414f95e3e7358066f88a9b754de0e89b47c431fd9eb5f61f4143`  
		Last Modified: Fri, 23 Jul 2021 11:11:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b607a9ed17bf183fba2f9dccf4bb87e2761cc9bec5cfb9b0075a65a6bcb3fbfa`  
		Last Modified: Mon, 02 Aug 2021 19:34:26 GMT  
		Size: 2.7 MB (2749052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0160648d960a2454964d3b9064d49d65a50bb41c534dbc2981c1d75ffb53f1f3`  
		Last Modified: Mon, 02 Aug 2021 19:34:31 GMT  
		Size: 48.6 MB (48632927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2ce4148d6e5ad123e1ed4f5fab2dc2ad17c411e17d178811ac1d5e9607ea69`  
		Last Modified: Mon, 02 Aug 2021 19:34:27 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.4` - linux; arm variant v5

```console
$ docker pull redmine@sha256:4bdd1675075975131a250540a53f8880f1e0fae8b29cfbc67ddab10f6586177b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210666390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcbb5833331e6445ac71ddc434c6a915315e32f215e0d6bc5929c81cd521053`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:39:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:39:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 14:39:29 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 14:57:30 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 15:01:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:02:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:02:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:02:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:02:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:02:04 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 01:32:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 01:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 01:33:37 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 01:33:37 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 01:33:38 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 01:33:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 21:04:50 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 21:04:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 21:04:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 21:10:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 21:10:36 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 21:10:37 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 21:10:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 21:10:38 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 21:10:38 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9237058b7c5120d5c6315b5d17a8c1d783be09a228b83772111ce9436c29d078`  
		Last Modified: Thu, 22 Jul 2021 15:15:34 GMT  
		Size: 10.3 MB (10345807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144b4344f580222d2fbc2f0d80fc139ab1a1ddb9a245b6073c41fdca9a93c23e`  
		Last Modified: Thu, 22 Jul 2021 15:15:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae149ea188f1e064a0256560e0273ae4b331a42ab93326fd9a79753cfb63299d`  
		Last Modified: Thu, 22 Jul 2021 15:18:00 GMT  
		Size: 20.7 MB (20733368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5d2d97d7d53265f79bb7d6b5cfc05f237e3d237d9cf22475536aa4fd57ccde`  
		Last Modified: Thu, 22 Jul 2021 15:17:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822c77937c7bc9bc3d506cf3a12ef2ada0bdbc4c0db3af2efaecc31c4191df4a`  
		Last Modified: Fri, 23 Jul 2021 01:49:24 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c50724a36d3c9a8b9ceae430de242d7f6969dbef3ac25c5fde473a8b062cd3`  
		Last Modified: Fri, 23 Jul 2021 01:50:25 GMT  
		Size: 89.6 MB (89576586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64ad6c53bf00acadba6df300f7a60ca8ae5ddc2336b37cd556bbcc18d26566c`  
		Last Modified: Fri, 23 Jul 2021 01:49:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f057554e99e7143804c2bfa6e4ad7c04cbf19075e611550a34de736734ec41c3`  
		Last Modified: Fri, 23 Jul 2021 01:49:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f864c8ca3715d87914498c4905365f0ed5cbf5e0cb26b9c639534a5511833b`  
		Last Modified: Mon, 02 Aug 2021 21:12:29 GMT  
		Size: 2.7 MB (2749054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4019d3cb4be9309f4cb0baa969bf37dfa6c525ade166c631d7b406cd8a3e59e4`  
		Last Modified: Mon, 02 Aug 2021 21:12:55 GMT  
		Size: 62.4 MB (62378250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564d2b0e0b86ccd1d38a66825b3d86b65542b19b9b749dd197dcf78fa771f039`  
		Last Modified: Mon, 02 Aug 2021 21:12:26 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.4` - linux; arm variant v7

```console
$ docker pull redmine@sha256:be260e0859e1639be25cf06cbe19352b4fb385c4942632e35f1558ddda888805
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203843857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f5b264322abd1cb8a7edae6550cf4a9952aa25db98c9a76125dd5ca9d1a94a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:15:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 02:15:46 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 02:46:35 GMT
ENV RUBY_MAJOR=2.6
# Fri, 23 Jul 2021 02:46:35 GMT
ENV RUBY_VERSION=2.6.8
# Fri, 23 Jul 2021 02:46:36 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Fri, 23 Jul 2021 02:50:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 02:50:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 02:50:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 02:50:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 02:50:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 02:50:43 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 21:25:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 21:26:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 21:26:28 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 21:26:29 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 21:26:29 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 21:26:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 03 Aug 2021 00:06:22 GMT
ENV REDMINE_VERSION=4.1.4
# Tue, 03 Aug 2021 00:06:23 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Tue, 03 Aug 2021 00:06:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 03 Aug 2021 00:11:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 03 Aug 2021 00:11:46 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 03 Aug 2021 00:11:47 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 03 Aug 2021 00:11:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Aug 2021 00:11:48 GMT
EXPOSE 3000
# Tue, 03 Aug 2021 00:11:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b8c791d70de7f22816846fbb07e0a1d7d419841c7e539a7cf57ef05fd50c5`  
		Last Modified: Fri, 23 Jul 2021 03:05:10 GMT  
		Size: 9.9 MB (9872218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb12a7edb0af862efa24dc389d7901cd2a894f2e106a1cef931ba0a6d675e2c0`  
		Last Modified: Fri, 23 Jul 2021 03:05:04 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0837e4e34dc8fe0ec9567b99bb7b1397a813fca3b43abfbbd75ee231a946a979`  
		Last Modified: Fri, 23 Jul 2021 03:07:54 GMT  
		Size: 20.6 MB (20643760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c76309d8689f06c398ddc0f6b5ec99a408c65c613d73d63fb9f5101ebe3e2a1`  
		Last Modified: Fri, 23 Jul 2021 03:07:49 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c349a607ae692434577c905a1f4029d996cee89a0c9f214fa866ac935ceddf23`  
		Last Modified: Fri, 23 Jul 2021 21:41:16 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2880a64f27ab57a09b4f72db20fc36a50bf3b6a6f3475f8661e8184e4b8acb99`  
		Last Modified: Fri, 23 Jul 2021 21:42:11 GMT  
		Size: 85.6 MB (85590430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455a681e485f6469d2ea0559f66edfbdf6ea359e79d4a5db42bf76287a0de434`  
		Last Modified: Fri, 23 Jul 2021 21:41:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac534a0a817b7f2f9c1f1e31c139ea1f9375a72e0f485b0383bc4fc4d59fd2a`  
		Last Modified: Fri, 23 Jul 2021 21:41:14 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c129690336fa4b91fdd3354d450f70c1d503241b4f996e45a06f6cc7c5c33c8e`  
		Last Modified: Tue, 03 Aug 2021 00:13:31 GMT  
		Size: 2.7 MB (2749050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fe83cafb9bc610bb800a4c85956caaac9219e0f8a9d3c4c4951568fbaf45a4`  
		Last Modified: Tue, 03 Aug 2021 00:13:56 GMT  
		Size: 62.2 MB (62238188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8821dd99090d5f0c3476a0eabbcb4ec9b51cd0954272e8f5443c04ab694180f`  
		Last Modified: Tue, 03 Aug 2021 00:13:27 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.4` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:4d2eef074194f45decdf5b1b4a3166169b18038058b325f0d0862dbf58e89de1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217544129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43f88150f3bd00e9b27ca2fb50ae014489a41818c5674b2166dabae0c267a69`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:11:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:25:18 GMT
ENV RUBY_MAJOR=2.6
# Tue, 17 Aug 2021 04:25:19 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 17 Aug 2021 04:25:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 17 Aug 2021 04:27:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:27:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:27:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:27:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:27:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:27:26 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 14:19:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 14:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:20:21 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 14:20:21 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 14:20:21 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 14:20:22 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 14:20:22 GMT
ENV REDMINE_VERSION=4.1.4
# Tue, 17 Aug 2021 14:20:22 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Tue, 17 Aug 2021 14:20:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 14:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:22:50 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 14:22:50 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 14:22:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:22:50 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:22:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ab80b058f00336b15786a8d20ce50706c5277560dc1ddb487b7e5c9d24b10`  
		Last Modified: Tue, 17 Aug 2021 04:34:12 GMT  
		Size: 11.3 MB (11263042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6eb72cd750a3e09673b73506f2a2ce24b3006d1773293eb65b72c9a2cdf7190`  
		Last Modified: Tue, 17 Aug 2021 04:34:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a741dfbe27573196b9f78f97eb7f35b06eaff990866fb7f894987974bd3f6d`  
		Last Modified: Tue, 17 Aug 2021 04:36:41 GMT  
		Size: 21.3 MB (21309045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6991754b0a79718bf8ab6c058b0ca4e091450b59072ac29e34401525b4337cc2`  
		Last Modified: Tue, 17 Aug 2021 04:36:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b2d6fcce3e7c045cbcf366963f15eecf60f206a0f9affdb4be5f3e1cdb8e58`  
		Last Modified: Tue, 17 Aug 2021 14:26:56 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fb70beab3eb9f346f19baeada6ab2ab16b85603c8269cd25ef07d34d7d3bbd`  
		Last Modified: Tue, 17 Aug 2021 14:27:12 GMT  
		Size: 92.6 MB (92610850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88949e39e9bf16adf106d42b5c92a9aa9f223ed09de640620dab986a37998467`  
		Last Modified: Tue, 17 Aug 2021 14:26:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8b01342158e6f70c8d6a1fb0a08d898843a76e9eaac116f8be7bf1cd5dc0ab`  
		Last Modified: Tue, 17 Aug 2021 14:26:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a92eed4532a610d931b5637079bd2beaf67787995446f363d81a4e9afb7304c`  
		Last Modified: Tue, 17 Aug 2021 14:26:55 GMT  
		Size: 2.7 MB (2749057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4658a1e88f9cf77366e04fc9ccacb6815390e8e23e32ba77a0e63a1307a797d5`  
		Last Modified: Tue, 17 Aug 2021 14:27:02 GMT  
		Size: 63.7 MB (63692816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd3201c15e0230dd813392cedf5401f39cafe6d75e2649301390105577ef545`  
		Last Modified: Tue, 17 Aug 2021 14:26:54 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.4` - linux; 386

```console
$ docker pull redmine@sha256:34c1de73f944be0d2b1aad3429ab5446bd8eb5f8fa9a6d9c6a2834e32009f2f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (213005139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31e81ffbd0f74a0e05d1b81a16f5590b48a3fea8852ccffb8e39da33177b98e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:39:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 15:39:00 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:53:08 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 15:53:09 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 15:56:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:56:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:56:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:56:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:56:29 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 00:13:48 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 00:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:14:41 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 00:14:42 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 00:14:42 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 00:14:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:54:34 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 23:54:34 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 23:54:38 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:55:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:55:25 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:55:26 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:55:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:55:26 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:55:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071d04ca5200ad3b98494cfde36960022dbd29c9afc33d685ac499fae8a05d63`  
		Last Modified: Thu, 22 Jul 2021 16:06:57 GMT  
		Size: 17.2 MB (17227285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d9d06c9e919afbd9358b702cad5bc0f28b8150722ffedb25ece16dc1f19b2`  
		Last Modified: Thu, 22 Jul 2021 16:06:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3172650cf56a46da1b8438a86468d4053edf77c17eaad06d10b7c7a4f89d13ff`  
		Last Modified: Thu, 22 Jul 2021 16:09:12 GMT  
		Size: 20.9 MB (20910118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2686761ac4b88297af44e82ba027c5c73411fe3e728b11bbdc631ea19cae4207`  
		Last Modified: Thu, 22 Jul 2021 16:09:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd85881cfa469c977c54673a6f7a5069bd5524e91c3dcc68765e8c34126cabe2`  
		Last Modified: Fri, 23 Jul 2021 00:23:41 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceccbef720a55f3b84f4c45e8ebfdec613398d896ceb5e3e5eb289b29c9fc015`  
		Last Modified: Fri, 23 Jul 2021 00:24:18 GMT  
		Size: 95.7 MB (95703189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2780ce2bed1fed359a6ca6b2570df212412bf9869a7e43011fd9b1e2b174944`  
		Last Modified: Fri, 23 Jul 2021 00:23:39 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f156819ab7d2b648146a7ca9ccee6d402b080b6d4f0d598d5844ff1dcd229e09`  
		Last Modified: Fri, 23 Jul 2021 00:23:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68c428871e997596ca3bf8c8c41a6dd81f73aa3ceacccd5dd3dac68fe3bf2d2`  
		Last Modified: Mon, 02 Aug 2021 23:56:30 GMT  
		Size: 2.7 MB (2749061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672dc0c872867a2d4f39e506bc7a1ebf5d775df842e1756c4c2e90e83c7110d`  
		Last Modified: Mon, 02 Aug 2021 23:56:36 GMT  
		Size: 48.6 MB (48613795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811de41f951559285a2f0118abc2c4bfa0cfc320e2607a3b79eea7b056af6df`  
		Last Modified: Mon, 02 Aug 2021 23:56:29 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.4` - linux; ppc64le

```console
$ docker pull redmine@sha256:6efef148967595e8835c7ce456bbd96854bc5b5bde0f00aa661936d90794159d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234101779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537c3d32f7d409d0c29fbdb569f953787339bc40657e734c3348a1fb9679b5f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 00:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 00:33:06 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 01:11:31 GMT
ENV RUBY_MAJOR=2.6
# Fri, 23 Jul 2021 01:11:38 GMT
ENV RUBY_VERSION=2.6.8
# Fri, 23 Jul 2021 01:11:44 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Fri, 23 Jul 2021 01:26:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 01:26:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 01:26:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 01:26:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 01:26:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 01:26:59 GMT
CMD ["irb"]
# Sat, 24 Jul 2021 02:51:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sat, 24 Jul 2021 02:58:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Jul 2021 02:58:12 GMT
ENV RAILS_ENV=production
# Sat, 24 Jul 2021 02:58:18 GMT
WORKDIR /usr/src/redmine
# Sat, 24 Jul 2021 02:58:23 GMT
ENV HOME=/home/redmine
# Sat, 24 Jul 2021 02:58:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:23:57 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 23:24:02 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 23:24:16 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:29:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:29:34 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:29:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:29:42 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:29:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f17b372a9c9122b881c2d22680e91d78ef4c329094595c61f5acb2523f41b7`  
		Last Modified: Fri, 23 Jul 2021 01:35:00 GMT  
		Size: 12.7 MB (12704330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064c16cae6894266abd8c9d33cfb671a4ebb2705d8b8bb7495bafc50c3dcd344`  
		Last Modified: Fri, 23 Jul 2021 01:34:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33960675014a7e56a0cf9f85e256ec6cce1c710723a7cd8f64935709d00e323d`  
		Last Modified: Fri, 23 Jul 2021 01:38:17 GMT  
		Size: 22.0 MB (21985713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047ee7c416fdfdb76a18bc7d50d5c00c1568b5e197242760391ce18bec14da13`  
		Last Modified: Fri, 23 Jul 2021 01:38:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c93f3da9b7a0eaf5df16b7b32a686296eaa146856420c2ce2d9ee2ad916121`  
		Last Modified: Sat, 24 Jul 2021 03:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77867ad228284b5163a25c4a76739b9c38ecbf8984bbc696c8e354141fe6b00`  
		Last Modified: Sat, 24 Jul 2021 03:37:11 GMT  
		Size: 101.3 MB (101328215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1ee06db11cacc9daf59c75cefc28c1d232ac1e928afa7a6f43d367e10bd1f1`  
		Last Modified: Sat, 24 Jul 2021 03:36:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f85237d5d99063036b3bb2790b12d7cbce41850c87c2bfbff1db63e7f5c0aa`  
		Last Modified: Sat, 24 Jul 2021 03:36:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b41fd52ae5e75f49d10d154992d46e779d973647edbfc7cc463b8c08b43cf95`  
		Last Modified: Mon, 02 Aug 2021 23:30:58 GMT  
		Size: 2.7 MB (2749055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9579a8a24f91bac1182097cd9218c6eb23b0e16728c8a7fb9a8386b58daf180`  
		Last Modified: Mon, 02 Aug 2021 23:31:07 GMT  
		Size: 64.8 MB (64776514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fea5dde6960e18005f909bc4dcaff30bd2eff3054518e9b24d2fc72f25038e`  
		Last Modified: Mon, 02 Aug 2021 23:30:57 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.4` - linux; s390x

```console
$ docker pull redmine@sha256:5c79bd1a8590ca5bf82ec50e92e21512b07940797a1463edc9ddcf5fa9b56609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216904122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d385d903de9e3d8df431fcda401c63ff60e7c93ecd4adc587a0f18c0cec4b352`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:21:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:21:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:54:27 GMT
ENV RUBY_MAJOR=2.6
# Tue, 17 Aug 2021 04:54:28 GMT
ENV RUBY_VERSION=2.6.8
# Tue, 17 Aug 2021 04:54:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Tue, 17 Aug 2021 04:57:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:57:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:57:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:57:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:57:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:57:43 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 13:35:57 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 13:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 13:36:30 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 13:36:31 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 13:36:31 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 13:36:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 13:36:32 GMT
ENV REDMINE_VERSION=4.1.4
# Tue, 17 Aug 2021 13:36:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Tue, 17 Aug 2021 13:36:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 13:38:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 13:38:20 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 13:38:20 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 13:38:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 13:38:20 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 13:38:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c03f413a15f7a98caaa2b027613636c576e3d98d8e1a98805c5978f2cc985f`  
		Last Modified: Tue, 17 Aug 2021 05:03:55 GMT  
		Size: 10.8 MB (10814401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ded0951dc51ddc1b38edf558277fec87d4169c1607312f67af2c4ffb9c4f19`  
		Last Modified: Tue, 17 Aug 2021 05:03:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b5f065983b815df03f5d378b737ce8b8950a6f775907f64c8d9413edfec507`  
		Last Modified: Tue, 17 Aug 2021 05:05:31 GMT  
		Size: 21.6 MB (21620194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c23b68c30a72cdc95043eff33b8ac51682c16759a2f483c8f4255db0f287c2`  
		Last Modified: Tue, 17 Aug 2021 05:05:28 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04534d357d558a08a4aea1da302e17954529ebf3804b4a0fe94cff2edac70b48`  
		Last Modified: Tue, 17 Aug 2021 13:42:39 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f89f5346ffb70bc7a8b15f07817f963fb0d00122dacff743cb5c1af76d9479`  
		Last Modified: Tue, 17 Aug 2021 13:42:51 GMT  
		Size: 91.8 MB (91789175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad842e06b48edaf468d80d1505a6ee1be7be796415dc006ca2d231db55e6b6a6`  
		Last Modified: Tue, 17 Aug 2021 13:42:37 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b320e5d26dc0c91fa46241087be2cc7e455bf87e055af14800bf2489c38c2452`  
		Last Modified: Tue, 17 Aug 2021 13:42:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6636b36120f102a30afdee3f007c4c76c804f392476d0db0dfec249f4c7b8a7f`  
		Last Modified: Tue, 17 Aug 2021 13:42:37 GMT  
		Size: 2.7 MB (2749060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55ccb25470f9adf5b849f9a3d8fdd2393db99a602df8f5a9df60ddf284f94dd`  
		Last Modified: Tue, 17 Aug 2021 13:42:43 GMT  
		Size: 64.2 MB (64166193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126aa5be9c0306e584899b0604d54804c8fb7792dedca7cfce8c6a063d0cab14`  
		Last Modified: Tue, 17 Aug 2021 13:42:37 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.4-alpine`

```console
$ docker pull redmine@sha256:75724ab6c055e0fb9d5c001b3e2ea96933739a169effd4d9dff712e0beec5c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1.4-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:704c3fa30632908b58ecbb9d7dfddcbbd1729a16f5d17ce4f7fc3be03b731265
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161073890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c81718646cb9796cc83de16cb4c5cb35512859b54704d82c2d2c2aad4028d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 08 Jul 2021 21:57:27 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 08 Jul 2021 21:57:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 08 Jul 2021 21:57:30 GMT
ENV LANG=C.UTF-8
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_MAJOR=2.6
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 08 Jul 2021 22:33:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 08 Jul 2021 22:35:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 22:35:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 22:35:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 22:35:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 22:35:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 22:35:59 GMT
CMD ["irb"]
# Wed, 14 Jul 2021 20:26:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 14 Jul 2021 20:26:45 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 14 Jul 2021 20:26:46 GMT
ENV RAILS_ENV=production
# Wed, 14 Jul 2021 20:26:46 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jul 2021 20:26:46 GMT
ENV HOME=/home/redmine
# Wed, 14 Jul 2021 20:26:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:30:38 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 19:30:38 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 19:30:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:30:41 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 02 Aug 2021 19:32:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Mon, 02 Aug 2021 19:32:43 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:32:43 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Mon, 02 Aug 2021 19:32:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:32:43 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:32:43 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5b0ea69e9ed42c49b5af449b703a12a4d2f2e28d87905af6fcd903fdae5689`  
		Last Modified: Thu, 08 Jul 2021 22:38:46 GMT  
		Size: 3.6 MB (3581658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad656ed833315b61ea674706f32c2d18d7412c7120926442af57b9131ee72ee`  
		Last Modified: Thu, 08 Jul 2021 22:38:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a9d07bc1851494b8935d8593efecfea98e2c4a4ff1c3eaf2e5319eb31cb3a2`  
		Last Modified: Thu, 08 Jul 2021 22:41:47 GMT  
		Size: 19.9 MB (19889336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d50c8fd3318db7f0dbb1d50a8aa4e571ae4926440e66c07be861dd4685211d`  
		Last Modified: Thu, 08 Jul 2021 22:41:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e030b8560a875bcd9c87e7dd1c8faf94a9d48cf039ee0bf125017750cc802b`  
		Last Modified: Wed, 14 Jul 2021 20:37:07 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c0006aa2ad99f9ffc9d729323dc4d6fe56017cf11735d341570e65864f6425`  
		Last Modified: Wed, 14 Jul 2021 20:37:17 GMT  
		Size: 69.5 MB (69526405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde1c41e26debfed4512ebfbeb0a14368410a36df9e8a30216966c830eee17ad`  
		Last Modified: Wed, 14 Jul 2021 20:37:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968695fc5116055ee483a173dbd08fdd5e9aba5dea28a955cdc730ae9f0bba52`  
		Last Modified: Wed, 14 Jul 2021 20:37:04 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c82c1c8b2f323e74c94315a3f2612cfb3ccc41eb9f247db68ff0821e0e089ba`  
		Last Modified: Mon, 02 Aug 2021 19:34:56 GMT  
		Size: 2.7 MB (2749721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7662a67f83cd246151d8c35ba66c66751655e34aad0846285c1dfb5a0c63284a`  
		Last Modified: Mon, 02 Aug 2021 19:35:01 GMT  
		Size: 62.5 MB (62511071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8798eb314975e00365c070021fed0c5fcb4587d78e6a72432cef4f1f7974426a`  
		Last Modified: Mon, 02 Aug 2021 19:34:55 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.4-passenger`

```console
$ docker pull redmine@sha256:5c6e20997f65ca9b448dd204a9876048d651859b7b1c5fb6b43e03fc76c96ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1.4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:2c81b66540bf9965be665f52cf1b0d64f64a56dbe812dab5f4232ef6e3aaa44b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232893079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025667f7cf28b19b6bc5b9f9b223e794ec8a85794144ca94fb067769b629d7e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_MAJOR=2.6
# Thu, 22 Jul 2021 17:31:24 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 22 Jul 2021 17:31:25 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 22 Jul 2021 17:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:34:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:34:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:34:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:34:07 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:05:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:05:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:05:50 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:05:50 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:05:50 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:05:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:29:26 GMT
ENV REDMINE_VERSION=4.1.4
# Mon, 02 Aug 2021 19:29:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=beaf6e51bb6a0c7655d73410afdf50c24091ee5f11eda0c9e96f38dfa7a3ab9f
# Mon, 02 Aug 2021 19:29:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:30:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:30:08 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:30:09 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:30:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:30:09 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:30:09 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Mon, 02 Aug 2021 19:30:16 GMT
ENV PASSENGER_VERSION=6.0.10
# Mon, 02 Aug 2021 19:30:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:30:34 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Mon, 02 Aug 2021 19:30:34 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Mon, 02 Aug 2021 19:30:34 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b7373cf9d9195064da3c92860c7157644c595720fffd5bb48615ac96985d5`  
		Last Modified: Thu, 22 Jul 2021 17:43:38 GMT  
		Size: 21.5 MB (21468044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb83e25b0fb68c5c98194adb0ad3740bc7d2242801c213e7d7949281f901679`  
		Last Modified: Thu, 22 Jul 2021 17:43:35 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61371aadcf232eb667c47dbba436a5611088d97ba4c8a9bd0c271f36882b027d`  
		Last Modified: Fri, 23 Jul 2021 11:11:30 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfd1dde1f32f7f8409959b4663cf89b722a2f427f544c5acf3c4dca5ba89961`  
		Last Modified: Fri, 23 Jul 2021 11:11:43 GMT  
		Size: 94.1 MB (94088300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216270a0114d5886d784b5a4bd95e0270c48d34e26e20ced7ee30251aecc0235`  
		Last Modified: Fri, 23 Jul 2021 11:11:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc0835bd828414f95e3e7358066f88a9b754de0e89b47c431fd9eb5f61f4143`  
		Last Modified: Fri, 23 Jul 2021 11:11:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b607a9ed17bf183fba2f9dccf4bb87e2761cc9bec5cfb9b0075a65a6bcb3fbfa`  
		Last Modified: Mon, 02 Aug 2021 19:34:26 GMT  
		Size: 2.7 MB (2749052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0160648d960a2454964d3b9064d49d65a50bb41c534dbc2981c1d75ffb53f1f3`  
		Last Modified: Mon, 02 Aug 2021 19:34:31 GMT  
		Size: 48.6 MB (48632927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2ce4148d6e5ad123e1ed4f5fab2dc2ad17c411e17d178811ac1d5e9607ea69`  
		Last Modified: Mon, 02 Aug 2021 19:34:27 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1626dac6c4d9ff800fe35da237dabc193dbdc7f07135c5322d702b87da59fd3f`  
		Last Modified: Mon, 02 Aug 2021 19:34:45 GMT  
		Size: 21.3 MB (21322664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbf672985eb895d1057965b1448ea42f3c48ad6d94dbc25c415d08aaf6958e1`  
		Last Modified: Mon, 02 Aug 2021 19:34:43 GMT  
		Size: 4.9 MB (4919279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2`

```console
$ docker pull redmine@sha256:eee3e32af89aeb43c91af7b2a61a959c4fba3f6d6cdd9695f56be8c2cefc31b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.2` - linux; amd64

```console
$ docker pull redmine@sha256:a40f8da31978334c3d594ec8a053130245877f460f45911fb36e17be8e6e07a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195494644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c25a3b03269000ce6a7aa543599b627f73fa5bcc07debf1eb1cd10129f908dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 17:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:28:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:28:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:28:25 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:03:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:04:03 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:04:03 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:04:03 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:04:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:26:03 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:26:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:26:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:26:48 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:26:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:26:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:26:49 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:26:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e582c090726ff249b7e30253c7f0c11aa2cd14282a8b6cd0e8055c8615e5586`  
		Last Modified: Thu, 22 Jul 2021 17:42:40 GMT  
		Size: 14.5 MB (14509812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f96a83aedee46aef2be1d4f73cc6990dc7e756981b022462100ac16fad345`  
		Last Modified: Thu, 22 Jul 2021 17:42:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9466f2ac94d013cc74523ee4ad44d9720c72baa51d8aecc2afcba41c3754be44`  
		Last Modified: Fri, 23 Jul 2021 11:10:32 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbad6372ccefa1ce14b5eefe2fe718c0cd234b40bf9a70e3d02e131a9dd65d26`  
		Last Modified: Fri, 23 Jul 2021 11:10:45 GMT  
		Size: 94.1 MB (94087869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b93724991108aa18238773a3122f3fcd80f69331610c0a7f00656f690ac7692`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19466676666dc7f1a145b5b2534855e6f32c152cd3da118bc5536badc24da33d`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97607437e7fff6da79d61cc4ee4518344c291c99e79a6b90c113170646e975a`  
		Last Modified: Mon, 02 Aug 2021 19:33:23 GMT  
		Size: 3.1 MB (3061918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67d0866b331d96beda7e546b964c7d5dc48b95b5ea08b4624257efde2481b4a`  
		Last Modified: Mon, 02 Aug 2021 19:33:27 GMT  
		Size: 44.1 MB (44122231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed36b971f221fb68203ab38c344723da172f129a111027998d95d695bdccfa`  
		Last Modified: Mon, 02 Aug 2021 19:33:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; arm variant v5

```console
$ docker pull redmine@sha256:2ba20de8f2d5813171b6b38d1e727aba839ab6cdd974c966ed2b8cd016b97c70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (196974835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2290c3ececd51c95738415fab07fc46dcc63d3a61e8099fb6c45e290ec3f0d91`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:39:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:39:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 14:39:29 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:48:33 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 14:48:33 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 14:48:34 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 14:52:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 14:52:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 14:52:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 14:52:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 14:52:55 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 14:52:55 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 01:25:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 01:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 01:26:16 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 01:26:17 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 01:26:17 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 01:26:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 20:58:44 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 20:58:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 20:58:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 21:04:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 21:04:31 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 21:04:31 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 21:04:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 21:04:32 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 21:04:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9237058b7c5120d5c6315b5d17a8c1d783be09a228b83772111ce9436c29d078`  
		Last Modified: Thu, 22 Jul 2021 15:15:34 GMT  
		Size: 10.3 MB (10345807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144b4344f580222d2fbc2f0d80fc139ab1a1ddb9a245b6073c41fdca9a93c23e`  
		Last Modified: Thu, 22 Jul 2021 15:15:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8ddbd20410764a5a44de2520de7417bddfcc0fdf2f4fa1b1d4e9ac785ce253`  
		Last Modified: Thu, 22 Jul 2021 15:17:00 GMT  
		Size: 13.9 MB (13871315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1fe10899466e387c0fc9cc130a0a900ffeb91af92c09301e387e444836d74f`  
		Last Modified: Thu, 22 Jul 2021 15:16:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b419523e1af1c8a3f9891c74f5e29e5697be8bf7bf57f23880ac551c460f07`  
		Last Modified: Fri, 23 Jul 2021 01:48:00 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d44a2001e78eed6fc3a85dbe0059a0bfae376949cda406c9304941ed617a23`  
		Last Modified: Fri, 23 Jul 2021 01:49:01 GMT  
		Size: 89.6 MB (89576912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2901c80e9a45cf66afe7fb2306719b195ec9c983783f4058ef68246bb10b95`  
		Last Modified: Fri, 23 Jul 2021 01:47:58 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b0cf9a21c70c0994e217daf5f71efd9d2f8ce8f36e062be7c831492162e99a`  
		Last Modified: Fri, 23 Jul 2021 01:47:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342031318accab10946b43b34804e02f1e0c107a6af3af5a4ebb766152ee509`  
		Last Modified: Mon, 02 Aug 2021 21:11:42 GMT  
		Size: 3.1 MB (3061919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648b6a3dac4889e5f68f30776a664fe9d62256592f37d6d2912163da56f265fa`  
		Last Modified: Mon, 02 Aug 2021 21:12:04 GMT  
		Size: 55.2 MB (55235555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5a29c2452fcab6625565bca85ff5fccfbee37e09b6f1e8455655c2735c166a`  
		Last Modified: Mon, 02 Aug 2021 21:11:38 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; arm variant v7

```console
$ docker pull redmine@sha256:cac694ac7078f02298b587000698d84cb3bb69637d30c724bd0bcac087c22f41
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190115136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3187fd285a60bd484a8586f3ee1dc8896c0c94e433a102025bf0dae4c344c1b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:15:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 02:15:46 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 02:25:03 GMT
ENV RUBY_MAJOR=2.7
# Fri, 23 Jul 2021 02:25:04 GMT
ENV RUBY_VERSION=2.7.4
# Fri, 23 Jul 2021 02:25:04 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Fri, 23 Jul 2021 02:29:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 02:29:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 02:29:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 02:29:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 02:29:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 02:29:10 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 21:18:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 21:19:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 21:19:37 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 21:19:37 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 21:19:38 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 21:19:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 03 Aug 2021 00:00:45 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 03 Aug 2021 00:00:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 03 Aug 2021 00:00:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 03 Aug 2021 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 03 Aug 2021 00:06:06 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 03 Aug 2021 00:06:07 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 03 Aug 2021 00:06:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Aug 2021 00:06:08 GMT
EXPOSE 3000
# Tue, 03 Aug 2021 00:06:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b8c791d70de7f22816846fbb07e0a1d7d419841c7e539a7cf57ef05fd50c5`  
		Last Modified: Fri, 23 Jul 2021 03:05:10 GMT  
		Size: 9.9 MB (9872218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb12a7edb0af862efa24dc389d7901cd2a894f2e106a1cef931ba0a6d675e2c0`  
		Last Modified: Fri, 23 Jul 2021 03:05:04 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b75d257bf75804e51385b730af2aaba386a501ef50517b8379966d4372c8597`  
		Last Modified: Fri, 23 Jul 2021 03:06:48 GMT  
		Size: 13.8 MB (13766962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc7c7e0536ed6ba4a99c1b8960d7c1d7365c8bc52d230b8af44d07d085916f`  
		Last Modified: Fri, 23 Jul 2021 03:06:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9cbdbb67af5c0b986c2fd6f93a2bacf3c795b046bfdf19e8f483dbc780c643`  
		Last Modified: Fri, 23 Jul 2021 21:39:57 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823bb8e3702405c250a7cc3dadba844fef162cbd0f5b9fb70a107f618dffeddf`  
		Last Modified: Fri, 23 Jul 2021 21:40:51 GMT  
		Size: 85.6 MB (85590187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930c9cc4f262f629914e37abf7b88697bc949d34260a237f8d740ea30ddf5902`  
		Last Modified: Fri, 23 Jul 2021 21:39:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e7aa3a63516ee59c6e77fd1a74b1ce0b303c09b2a97dd0ca3b0af594021030`  
		Last Modified: Fri, 23 Jul 2021 21:39:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2c8055fd9194f59346984cbb7941b37a40023edc25ab3dec3e42e9b8c01287`  
		Last Modified: Tue, 03 Aug 2021 00:12:46 GMT  
		Size: 3.1 MB (3061917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836246f3dcf57e23a39d002b3b9d9a09fedb40b5b6accc7268b28ae167eca128`  
		Last Modified: Tue, 03 Aug 2021 00:13:05 GMT  
		Size: 55.1 MB (55073644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63001a72a77f002e6a9f105ba97f4e5cb147287597ca1e71c8670c6b0e768390`  
		Last Modified: Tue, 03 Aug 2021 00:12:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:168d7ed49573c2aaecf2d0d8adcc21280d9e2c18dc1ddb19848393c9847211e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203243298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a980ba1133cf226e557df7c34d75d5c5e7bfb359db4c611a013f2dd737ac6dc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:11:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_MAJOR=2.7
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 17 Aug 2021 04:20:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:20:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:20:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:20:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:20:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:20:13 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 14:17:02 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 14:17:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:17:25 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 14:17:26 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 14:17:26 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 14:17:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 14:17:27 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 17 Aug 2021 14:17:27 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 17 Aug 2021 14:17:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 14:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:19:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 14:19:47 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 14:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:19:48 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:19:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ab80b058f00336b15786a8d20ce50706c5277560dc1ddb487b7e5c9d24b10`  
		Last Modified: Tue, 17 Aug 2021 04:34:12 GMT  
		Size: 11.3 MB (11263042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6eb72cd750a3e09673b73506f2a2ce24b3006d1773293eb65b72c9a2cdf7190`  
		Last Modified: Tue, 17 Aug 2021 04:34:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2cb28558c1dd6c31a020484f10c613185335d6d30e7c7a81d3e6ffd0f374f0`  
		Last Modified: Tue, 17 Aug 2021 04:35:35 GMT  
		Size: 14.4 MB (14356587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49391d2e67bfbf4fd993b49c9be1225f0a09d4177c605548f82d49cbcfe78b99`  
		Last Modified: Tue, 17 Aug 2021 04:35:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9307e85455464623a9445ee9314b11fd777c561cefed9b38e6f9067bd30653a`  
		Last Modified: Tue, 17 Aug 2021 14:26:18 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba598bababc240a9c29cf82ac1a0b01837945e37b3cb2b17a3a55ba776227b76`  
		Last Modified: Tue, 17 Aug 2021 14:26:34 GMT  
		Size: 92.6 MB (92611086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc88258ae8d8cf36219a3b41b130d1e21bf4c2dfb6e1cf9c3f6b3ae2395817`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c9b592ea00c036970d3b4b7baf687de5e9394670884daa30890ab191cfe5bb`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e8230053e3f65d96319f5f2351fc906de79749654a83811bf21ea7b34f3bee`  
		Last Modified: Tue, 17 Aug 2021 14:26:17 GMT  
		Size: 3.1 MB (3061920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe117b5c157b62194a629b77cf9c9b15c6821516a74c96470c098adba14546ba`  
		Last Modified: Tue, 17 Aug 2021 14:26:22 GMT  
		Size: 56.0 MB (56031346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff9fc675e51cbab5a7a0574bbd10f6ebdc614381aa4a451a98f5884e386b455`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; 386

```console
$ docker pull redmine@sha256:0b76e0e34b7153ffc2a922fe7cc584cdf37e53c0bf95d204bb3ff857e242f139
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202124661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d0b99035f254ab4f5e3822b673034b671859094e70176d730c1807bed1c7d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:39:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 15:39:00 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 15:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:49:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:49:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:49:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:49:39 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 00:10:49 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 00:11:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:11:45 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 00:11:45 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 00:11:46 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 00:11:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:53:31 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 23:53:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 23:53:36 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:54:26 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:54:26 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:54:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:54:27 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:54:27 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071d04ca5200ad3b98494cfde36960022dbd29c9afc33d685ac499fae8a05d63`  
		Last Modified: Thu, 22 Jul 2021 16:06:57 GMT  
		Size: 17.2 MB (17227285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d9d06c9e919afbd9358b702cad5bc0f28b8150722ffedb25ece16dc1f19b2`  
		Last Modified: Thu, 22 Jul 2021 16:06:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9e06bdf88f28c2f5d5893c862c6da8a6a73eb098cb2cd8eec57656d9a79b69`  
		Last Modified: Thu, 22 Jul 2021 16:08:14 GMT  
		Size: 14.0 MB (13992268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f84633b2fe0d1dff5a1fd6ab3a5506af8978d94ded4f5a0f2727ce06805d4`  
		Last Modified: Thu, 22 Jul 2021 16:08:11 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ef59b51318d382563cb5fdab4577df04d06c56bd8885926c9a9374a31ed7c`  
		Last Modified: Fri, 23 Jul 2021 00:22:32 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2922ffac0f77cf1fd832a20d48b586a6621e1d75610c055227f6d76e34928b16`  
		Last Modified: Fri, 23 Jul 2021 00:23:09 GMT  
		Size: 95.7 MB (95703233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb8c5967872202784509fa53a811f849c714ef794dd53a40047d0c81585ce4`  
		Last Modified: Fri, 23 Jul 2021 00:22:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2c1ffe6294aae5e8df812aee47c20e59fe0f4ec3593946e4ed069116ebb9f1`  
		Last Modified: Fri, 23 Jul 2021 00:22:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2101d5d051bcf08ee904abd42115ca10712771f5cf1c4e0b423529da86e741a6`  
		Last Modified: Mon, 02 Aug 2021 23:56:03 GMT  
		Size: 3.1 MB (3061914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fcbda204aa9670b17dc8d7e97735f16ce74df3a60c6d2d9569f7318a335249`  
		Last Modified: Mon, 02 Aug 2021 23:56:09 GMT  
		Size: 44.3 MB (44338267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3a655d5b411d7076572c42fcece59f2189f79f1c6bfa2759554c0fe12a0ec3`  
		Last Modified: Mon, 02 Aug 2021 23:56:01 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; ppc64le

```console
$ docker pull redmine@sha256:ecdb00827fcf83f2f12c122af3ffc2420a6faa270cd7b048c9756f927f7c77fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219650618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57391c1536ff89c22d27544dc68890a924a8d455796c92bdc28721108b71a53c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 00:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 00:33:06 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 00:52:18 GMT
ENV RUBY_MAJOR=2.7
# Fri, 23 Jul 2021 00:52:28 GMT
ENV RUBY_VERSION=2.7.4
# Fri, 23 Jul 2021 00:52:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Fri, 23 Jul 2021 01:01:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 01:01:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 01:01:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 01:01:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 01:01:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 01:01:58 GMT
CMD ["irb"]
# Sat, 24 Jul 2021 02:42:41 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sat, 24 Jul 2021 02:46:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Jul 2021 02:46:14 GMT
ENV RAILS_ENV=production
# Sat, 24 Jul 2021 02:46:17 GMT
WORKDIR /usr/src/redmine
# Sat, 24 Jul 2021 02:46:19 GMT
ENV HOME=/home/redmine
# Sat, 24 Jul 2021 02:46:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:16:59 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 23:17:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 23:17:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:23:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:23:26 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:23:29 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:23:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:23:37 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:23:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f17b372a9c9122b881c2d22680e91d78ef4c329094595c61f5acb2523f41b7`  
		Last Modified: Fri, 23 Jul 2021 01:35:00 GMT  
		Size: 12.7 MB (12704330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064c16cae6894266abd8c9d33cfb671a4ebb2705d8b8bb7495bafc50c3dcd344`  
		Last Modified: Fri, 23 Jul 2021 01:34:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76d2032e7e646d23109ea1a55abb581c169350b85836914155a6837d64eb757`  
		Last Modified: Fri, 23 Jul 2021 01:36:48 GMT  
		Size: 15.0 MB (14997545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996a3088f8cd5e20b9f19c3aebdd4a6228a85b6c0a83f9dde8e2a5ec82976d3`  
		Last Modified: Fri, 23 Jul 2021 01:36:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acdc172d0fc27092df5794b7a17e2c42e7f2497e85086076f490e273db428fe`  
		Last Modified: Sat, 24 Jul 2021 03:36:05 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fe4ded3f0db610cc9dca87e98b2305c850cbaf595886ccb44e3492ad727b18`  
		Last Modified: Sat, 24 Jul 2021 03:36:28 GMT  
		Size: 101.3 MB (101327533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14617640fcda340a6bc04fd1c65d4183ad0dd01a4e3b44fb313d164071471e95`  
		Last Modified: Sat, 24 Jul 2021 03:36:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1b361a5633d0ca044cc644bddc99329645edadfff1cbb48e966deb9b0d079a`  
		Last Modified: Sat, 24 Jul 2021 03:36:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bfbd857622d0239bfa521d75318f40925e9e4608a62a4be7abc2bc89801ec3`  
		Last Modified: Mon, 02 Aug 2021 23:30:32 GMT  
		Size: 3.1 MB (3061921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e4b836dd92fc0980e6e61a697cc881ceb76ca811af742788283ab3211698e1`  
		Last Modified: Mon, 02 Aug 2021 23:30:38 GMT  
		Size: 57.0 MB (57001331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2976222796409af9d080f03664b07bc2a177c8b37d29e7937c0620ba5f908d03`  
		Last Modified: Mon, 02 Aug 2021 23:30:31 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; s390x

```console
$ docker pull redmine@sha256:33d5a2369e443a1bb092e9da696586fae6988113fc4ef99bf98b5af5e03135f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202554693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f13509159fb8e3ef52d7620d4ef325ebe2d7a388fec2faf172536b64ee9ae9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:21:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:21:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:37:51 GMT
ENV RUBY_MAJOR=2.7
# Tue, 17 Aug 2021 04:37:51 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 17 Aug 2021 04:37:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 17 Aug 2021 04:40:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:40:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:40:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:40:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:40:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:40:24 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 13:32:53 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 13:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 13:33:28 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 13:33:28 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 13:33:28 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 13:33:29 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 13:33:29 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 17 Aug 2021 13:33:29 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 17 Aug 2021 13:33:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 13:35:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 13:35:38 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 13:35:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 13:35:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 13:35:39 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 13:35:39 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c03f413a15f7a98caaa2b027613636c576e3d98d8e1a98805c5978f2cc985f`  
		Last Modified: Tue, 17 Aug 2021 05:03:55 GMT  
		Size: 10.8 MB (10814401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ded0951dc51ddc1b38edf558277fec87d4169c1607312f67af2c4ffb9c4f19`  
		Last Modified: Tue, 17 Aug 2021 05:03:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d49ef1e1c8f0247bfa63924e738fc94dc0c4a81ec0e4b2b73df09f08d080005`  
		Last Modified: Tue, 17 Aug 2021 05:04:49 GMT  
		Size: 14.7 MB (14697415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54919ecbd2a42d851761e24bb9a1e9e71346c6ecd753a4c6b7868679823367b`  
		Last Modified: Tue, 17 Aug 2021 05:04:47 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159f1e20f87d626bb303eea037968c316700fdd1fd9fa734e8ebacf14608ab2`  
		Last Modified: Tue, 17 Aug 2021 13:42:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223675cd45b3e6a43e45f6ad1a699c278dc5effe72583bec3657746c84a2a692`  
		Last Modified: Tue, 17 Aug 2021 13:42:24 GMT  
		Size: 91.8 MB (91792621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f55e74adea5c6a7d4c0be869fe00b2451a51e188e2c0e1466d72eaad06cc9d`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cd2e454b71a3aea72543018a9596e611b94ee88301b3d5971854daab02981`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b885ccd7ef756fbf397809a3541c6cadba886972a35c3f9d9d00cc920b16ef2`  
		Last Modified: Tue, 17 Aug 2021 13:42:11 GMT  
		Size: 3.1 MB (3061920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde4808141553382cd3c73078af6ba86889e806ed72c6251287678fbce48b5ea`  
		Last Modified: Tue, 17 Aug 2021 13:42:15 GMT  
		Size: 56.4 MB (56423232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed18e7c147f9b19d7cb774a6462749d36a61882e80d34fff6912e4ed7990252d`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2-alpine`

```console
$ docker pull redmine@sha256:34362d64f5cac220ecf3058a2982583ec0e2cba35273960105a4cff3dc0c4a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:429416f2012459eaa042fe2879ae170f0d1ee68b283059b2e4f855edcaae0101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150082289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a3f4194f1bef28b7e8c9cb584331cfe9876976fd1c68e194837191b82282e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 08 Jul 2021 21:57:27 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 08 Jul 2021 21:57:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 08 Jul 2021 21:57:30 GMT
ENV LANG=C.UTF-8
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_MAJOR=2.7
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 08 Jul 2021 22:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 22:18:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 22:18:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 22:18:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 22:18:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 22:18:51 GMT
CMD ["irb"]
# Wed, 14 Jul 2021 20:22:24 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 14 Jul 2021 20:22:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 14 Jul 2021 20:22:33 GMT
ENV RAILS_ENV=production
# Wed, 14 Jul 2021 20:22:33 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jul 2021 20:22:33 GMT
ENV HOME=/home/redmine
# Wed, 14 Jul 2021 20:22:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:27:15 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:27:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:27:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:27:19 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 02 Aug 2021 19:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Mon, 02 Aug 2021 19:29:21 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:29:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Mon, 02 Aug 2021 19:29:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:29:22 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:29:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5b0ea69e9ed42c49b5af449b703a12a4d2f2e28d87905af6fcd903fdae5689`  
		Last Modified: Thu, 08 Jul 2021 22:38:46 GMT  
		Size: 3.6 MB (3581658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad656ed833315b61ea674706f32c2d18d7412c7120926442af57b9131ee72ee`  
		Last Modified: Thu, 08 Jul 2021 22:38:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626f6830afc6fb7a05a8f18f2b98e4ea4db3d2dd50803e5cd2c627fe25150dc8`  
		Last Modified: Thu, 08 Jul 2021 22:40:13 GMT  
		Size: 14.4 MB (14373123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5375389679c9573d241b22905aee17b20981e2628989561698087f107fcfed4a`  
		Last Modified: Thu, 08 Jul 2021 22:40:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76a82132aeb154f32b80803eecedc3e27e062a35ae1e05284dc2d7e6c7f4f59`  
		Last Modified: Wed, 14 Jul 2021 20:35:42 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb4af997128346f54fa569d3a04180c718e02a90e90eff7161241d54deef92`  
		Last Modified: Wed, 14 Jul 2021 20:35:52 GMT  
		Size: 69.5 MB (69526214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da2816c58ef08b826f823d7b6a4126bb63594ed1109880b795c28cc4d3f032`  
		Last Modified: Wed, 14 Jul 2021 20:35:39 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f34be07349b94807cc58a0e31cecec279d0591b9a6f1f65f1dbe94a4713462`  
		Last Modified: Wed, 14 Jul 2021 20:35:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98c03ed41f8aa891bcd79e61fbb88cda198d71f5a8de4f510950e7f58aa1a15`  
		Last Modified: Mon, 02 Aug 2021 19:34:04 GMT  
		Size: 3.1 MB (3062843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08d14dd9ea01201645da35bc3855c4b0a6270b9d4ae9510f9da35fb4150e833`  
		Last Modified: Mon, 02 Aug 2021 19:34:08 GMT  
		Size: 56.7 MB (56722754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bee94fd486f4fb693e4765ade966dd49ee96cd0aff32109f156b9a2511d1af3`  
		Last Modified: Mon, 02 Aug 2021 19:34:03 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2-passenger`

```console
$ docker pull redmine@sha256:1227b146ef6133442f3c82299c894fd310739b1042176653e2126cf65a6bb369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:8f065daab31dbf85b85fa0bd93241a0225439d387e574f3b3c3ed2bac86bacc5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221545515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5b06ed983bc1e6cfc65432f997639be41bac864baaa904857feedfda309362`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 17:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:28:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:28:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:28:25 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:03:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:04:03 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:04:03 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:04:03 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:04:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:26:03 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:26:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:26:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:26:48 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:26:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:26:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:26:49 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:26:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Mon, 02 Aug 2021 19:26:54 GMT
ENV PASSENGER_VERSION=6.0.10
# Mon, 02 Aug 2021 19:27:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:27:11 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Mon, 02 Aug 2021 19:27:11 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Mon, 02 Aug 2021 19:27:11 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e582c090726ff249b7e30253c7f0c11aa2cd14282a8b6cd0e8055c8615e5586`  
		Last Modified: Thu, 22 Jul 2021 17:42:40 GMT  
		Size: 14.5 MB (14509812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f96a83aedee46aef2be1d4f73cc6990dc7e756981b022462100ac16fad345`  
		Last Modified: Thu, 22 Jul 2021 17:42:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9466f2ac94d013cc74523ee4ad44d9720c72baa51d8aecc2afcba41c3754be44`  
		Last Modified: Fri, 23 Jul 2021 11:10:32 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbad6372ccefa1ce14b5eefe2fe718c0cd234b40bf9a70e3d02e131a9dd65d26`  
		Last Modified: Fri, 23 Jul 2021 11:10:45 GMT  
		Size: 94.1 MB (94087869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b93724991108aa18238773a3122f3fcd80f69331610c0a7f00656f690ac7692`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19466676666dc7f1a145b5b2534855e6f32c152cd3da118bc5536badc24da33d`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97607437e7fff6da79d61cc4ee4518344c291c99e79a6b90c113170646e975a`  
		Last Modified: Mon, 02 Aug 2021 19:33:23 GMT  
		Size: 3.1 MB (3061918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67d0866b331d96beda7e546b964c7d5dc48b95b5ea08b4624257efde2481b4a`  
		Last Modified: Mon, 02 Aug 2021 19:33:27 GMT  
		Size: 44.1 MB (44122231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed36b971f221fb68203ab38c344723da172f129a111027998d95d695bdccfa`  
		Last Modified: Mon, 02 Aug 2021 19:33:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913b642de7599d445e0069c22e66310828fb96025c0b69e5be168036e5cae921`  
		Last Modified: Mon, 02 Aug 2021 19:33:47 GMT  
		Size: 21.1 MB (21131586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c214594b43db5e8aa08dd61b352a254deb095023ee416412ce655e42e783c5`  
		Last Modified: Mon, 02 Aug 2021 19:33:45 GMT  
		Size: 4.9 MB (4919285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2.2`

```console
$ docker pull redmine@sha256:eee3e32af89aeb43c91af7b2a61a959c4fba3f6d6cdd9695f56be8c2cefc31b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:4.2.2` - linux; amd64

```console
$ docker pull redmine@sha256:a40f8da31978334c3d594ec8a053130245877f460f45911fb36e17be8e6e07a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195494644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c25a3b03269000ce6a7aa543599b627f73fa5bcc07debf1eb1cd10129f908dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 17:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:28:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:28:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:28:25 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:03:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:04:03 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:04:03 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:04:03 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:04:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:26:03 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:26:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:26:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:26:48 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:26:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:26:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:26:49 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:26:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e582c090726ff249b7e30253c7f0c11aa2cd14282a8b6cd0e8055c8615e5586`  
		Last Modified: Thu, 22 Jul 2021 17:42:40 GMT  
		Size: 14.5 MB (14509812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f96a83aedee46aef2be1d4f73cc6990dc7e756981b022462100ac16fad345`  
		Last Modified: Thu, 22 Jul 2021 17:42:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9466f2ac94d013cc74523ee4ad44d9720c72baa51d8aecc2afcba41c3754be44`  
		Last Modified: Fri, 23 Jul 2021 11:10:32 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbad6372ccefa1ce14b5eefe2fe718c0cd234b40bf9a70e3d02e131a9dd65d26`  
		Last Modified: Fri, 23 Jul 2021 11:10:45 GMT  
		Size: 94.1 MB (94087869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b93724991108aa18238773a3122f3fcd80f69331610c0a7f00656f690ac7692`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19466676666dc7f1a145b5b2534855e6f32c152cd3da118bc5536badc24da33d`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97607437e7fff6da79d61cc4ee4518344c291c99e79a6b90c113170646e975a`  
		Last Modified: Mon, 02 Aug 2021 19:33:23 GMT  
		Size: 3.1 MB (3061918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67d0866b331d96beda7e546b964c7d5dc48b95b5ea08b4624257efde2481b4a`  
		Last Modified: Mon, 02 Aug 2021 19:33:27 GMT  
		Size: 44.1 MB (44122231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed36b971f221fb68203ab38c344723da172f129a111027998d95d695bdccfa`  
		Last Modified: Mon, 02 Aug 2021 19:33:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.2` - linux; arm variant v5

```console
$ docker pull redmine@sha256:2ba20de8f2d5813171b6b38d1e727aba839ab6cdd974c966ed2b8cd016b97c70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (196974835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2290c3ececd51c95738415fab07fc46dcc63d3a61e8099fb6c45e290ec3f0d91`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:39:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:39:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 14:39:29 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:48:33 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 14:48:33 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 14:48:34 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 14:52:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 14:52:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 14:52:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 14:52:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 14:52:55 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 14:52:55 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 01:25:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 01:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 01:26:16 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 01:26:17 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 01:26:17 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 01:26:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 20:58:44 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 20:58:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 20:58:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 21:04:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 21:04:31 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 21:04:31 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 21:04:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 21:04:32 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 21:04:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9237058b7c5120d5c6315b5d17a8c1d783be09a228b83772111ce9436c29d078`  
		Last Modified: Thu, 22 Jul 2021 15:15:34 GMT  
		Size: 10.3 MB (10345807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144b4344f580222d2fbc2f0d80fc139ab1a1ddb9a245b6073c41fdca9a93c23e`  
		Last Modified: Thu, 22 Jul 2021 15:15:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8ddbd20410764a5a44de2520de7417bddfcc0fdf2f4fa1b1d4e9ac785ce253`  
		Last Modified: Thu, 22 Jul 2021 15:17:00 GMT  
		Size: 13.9 MB (13871315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1fe10899466e387c0fc9cc130a0a900ffeb91af92c09301e387e444836d74f`  
		Last Modified: Thu, 22 Jul 2021 15:16:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b419523e1af1c8a3f9891c74f5e29e5697be8bf7bf57f23880ac551c460f07`  
		Last Modified: Fri, 23 Jul 2021 01:48:00 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d44a2001e78eed6fc3a85dbe0059a0bfae376949cda406c9304941ed617a23`  
		Last Modified: Fri, 23 Jul 2021 01:49:01 GMT  
		Size: 89.6 MB (89576912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2901c80e9a45cf66afe7fb2306719b195ec9c983783f4058ef68246bb10b95`  
		Last Modified: Fri, 23 Jul 2021 01:47:58 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b0cf9a21c70c0994e217daf5f71efd9d2f8ce8f36e062be7c831492162e99a`  
		Last Modified: Fri, 23 Jul 2021 01:47:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342031318accab10946b43b34804e02f1e0c107a6af3af5a4ebb766152ee509`  
		Last Modified: Mon, 02 Aug 2021 21:11:42 GMT  
		Size: 3.1 MB (3061919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648b6a3dac4889e5f68f30776a664fe9d62256592f37d6d2912163da56f265fa`  
		Last Modified: Mon, 02 Aug 2021 21:12:04 GMT  
		Size: 55.2 MB (55235555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5a29c2452fcab6625565bca85ff5fccfbee37e09b6f1e8455655c2735c166a`  
		Last Modified: Mon, 02 Aug 2021 21:11:38 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.2` - linux; arm variant v7

```console
$ docker pull redmine@sha256:cac694ac7078f02298b587000698d84cb3bb69637d30c724bd0bcac087c22f41
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190115136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3187fd285a60bd484a8586f3ee1dc8896c0c94e433a102025bf0dae4c344c1b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:15:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 02:15:46 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 02:25:03 GMT
ENV RUBY_MAJOR=2.7
# Fri, 23 Jul 2021 02:25:04 GMT
ENV RUBY_VERSION=2.7.4
# Fri, 23 Jul 2021 02:25:04 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Fri, 23 Jul 2021 02:29:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 02:29:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 02:29:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 02:29:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 02:29:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 02:29:10 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 21:18:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 21:19:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 21:19:37 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 21:19:37 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 21:19:38 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 21:19:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 03 Aug 2021 00:00:45 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 03 Aug 2021 00:00:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 03 Aug 2021 00:00:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 03 Aug 2021 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 03 Aug 2021 00:06:06 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 03 Aug 2021 00:06:07 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 03 Aug 2021 00:06:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Aug 2021 00:06:08 GMT
EXPOSE 3000
# Tue, 03 Aug 2021 00:06:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b8c791d70de7f22816846fbb07e0a1d7d419841c7e539a7cf57ef05fd50c5`  
		Last Modified: Fri, 23 Jul 2021 03:05:10 GMT  
		Size: 9.9 MB (9872218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb12a7edb0af862efa24dc389d7901cd2a894f2e106a1cef931ba0a6d675e2c0`  
		Last Modified: Fri, 23 Jul 2021 03:05:04 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b75d257bf75804e51385b730af2aaba386a501ef50517b8379966d4372c8597`  
		Last Modified: Fri, 23 Jul 2021 03:06:48 GMT  
		Size: 13.8 MB (13766962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc7c7e0536ed6ba4a99c1b8960d7c1d7365c8bc52d230b8af44d07d085916f`  
		Last Modified: Fri, 23 Jul 2021 03:06:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9cbdbb67af5c0b986c2fd6f93a2bacf3c795b046bfdf19e8f483dbc780c643`  
		Last Modified: Fri, 23 Jul 2021 21:39:57 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823bb8e3702405c250a7cc3dadba844fef162cbd0f5b9fb70a107f618dffeddf`  
		Last Modified: Fri, 23 Jul 2021 21:40:51 GMT  
		Size: 85.6 MB (85590187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930c9cc4f262f629914e37abf7b88697bc949d34260a237f8d740ea30ddf5902`  
		Last Modified: Fri, 23 Jul 2021 21:39:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e7aa3a63516ee59c6e77fd1a74b1ce0b303c09b2a97dd0ca3b0af594021030`  
		Last Modified: Fri, 23 Jul 2021 21:39:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2c8055fd9194f59346984cbb7941b37a40023edc25ab3dec3e42e9b8c01287`  
		Last Modified: Tue, 03 Aug 2021 00:12:46 GMT  
		Size: 3.1 MB (3061917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836246f3dcf57e23a39d002b3b9d9a09fedb40b5b6accc7268b28ae167eca128`  
		Last Modified: Tue, 03 Aug 2021 00:13:05 GMT  
		Size: 55.1 MB (55073644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63001a72a77f002e6a9f105ba97f4e5cb147287597ca1e71c8670c6b0e768390`  
		Last Modified: Tue, 03 Aug 2021 00:12:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.2` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:168d7ed49573c2aaecf2d0d8adcc21280d9e2c18dc1ddb19848393c9847211e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203243298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a980ba1133cf226e557df7c34d75d5c5e7bfb359db4c611a013f2dd737ac6dc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:11:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_MAJOR=2.7
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 17 Aug 2021 04:20:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:20:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:20:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:20:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:20:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:20:13 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 14:17:02 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 14:17:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:17:25 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 14:17:26 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 14:17:26 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 14:17:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 14:17:27 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 17 Aug 2021 14:17:27 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 17 Aug 2021 14:17:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 14:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:19:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 14:19:47 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 14:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:19:48 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:19:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ab80b058f00336b15786a8d20ce50706c5277560dc1ddb487b7e5c9d24b10`  
		Last Modified: Tue, 17 Aug 2021 04:34:12 GMT  
		Size: 11.3 MB (11263042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6eb72cd750a3e09673b73506f2a2ce24b3006d1773293eb65b72c9a2cdf7190`  
		Last Modified: Tue, 17 Aug 2021 04:34:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2cb28558c1dd6c31a020484f10c613185335d6d30e7c7a81d3e6ffd0f374f0`  
		Last Modified: Tue, 17 Aug 2021 04:35:35 GMT  
		Size: 14.4 MB (14356587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49391d2e67bfbf4fd993b49c9be1225f0a09d4177c605548f82d49cbcfe78b99`  
		Last Modified: Tue, 17 Aug 2021 04:35:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9307e85455464623a9445ee9314b11fd777c561cefed9b38e6f9067bd30653a`  
		Last Modified: Tue, 17 Aug 2021 14:26:18 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba598bababc240a9c29cf82ac1a0b01837945e37b3cb2b17a3a55ba776227b76`  
		Last Modified: Tue, 17 Aug 2021 14:26:34 GMT  
		Size: 92.6 MB (92611086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc88258ae8d8cf36219a3b41b130d1e21bf4c2dfb6e1cf9c3f6b3ae2395817`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c9b592ea00c036970d3b4b7baf687de5e9394670884daa30890ab191cfe5bb`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e8230053e3f65d96319f5f2351fc906de79749654a83811bf21ea7b34f3bee`  
		Last Modified: Tue, 17 Aug 2021 14:26:17 GMT  
		Size: 3.1 MB (3061920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe117b5c157b62194a629b77cf9c9b15c6821516a74c96470c098adba14546ba`  
		Last Modified: Tue, 17 Aug 2021 14:26:22 GMT  
		Size: 56.0 MB (56031346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff9fc675e51cbab5a7a0574bbd10f6ebdc614381aa4a451a98f5884e386b455`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.2` - linux; 386

```console
$ docker pull redmine@sha256:0b76e0e34b7153ffc2a922fe7cc584cdf37e53c0bf95d204bb3ff857e242f139
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202124661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d0b99035f254ab4f5e3822b673034b671859094e70176d730c1807bed1c7d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:39:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 15:39:00 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 15:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:49:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:49:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:49:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:49:39 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 00:10:49 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 00:11:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:11:45 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 00:11:45 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 00:11:46 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 00:11:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:53:31 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 23:53:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 23:53:36 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:54:26 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:54:26 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:54:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:54:27 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:54:27 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071d04ca5200ad3b98494cfde36960022dbd29c9afc33d685ac499fae8a05d63`  
		Last Modified: Thu, 22 Jul 2021 16:06:57 GMT  
		Size: 17.2 MB (17227285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d9d06c9e919afbd9358b702cad5bc0f28b8150722ffedb25ece16dc1f19b2`  
		Last Modified: Thu, 22 Jul 2021 16:06:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9e06bdf88f28c2f5d5893c862c6da8a6a73eb098cb2cd8eec57656d9a79b69`  
		Last Modified: Thu, 22 Jul 2021 16:08:14 GMT  
		Size: 14.0 MB (13992268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f84633b2fe0d1dff5a1fd6ab3a5506af8978d94ded4f5a0f2727ce06805d4`  
		Last Modified: Thu, 22 Jul 2021 16:08:11 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ef59b51318d382563cb5fdab4577df04d06c56bd8885926c9a9374a31ed7c`  
		Last Modified: Fri, 23 Jul 2021 00:22:32 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2922ffac0f77cf1fd832a20d48b586a6621e1d75610c055227f6d76e34928b16`  
		Last Modified: Fri, 23 Jul 2021 00:23:09 GMT  
		Size: 95.7 MB (95703233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb8c5967872202784509fa53a811f849c714ef794dd53a40047d0c81585ce4`  
		Last Modified: Fri, 23 Jul 2021 00:22:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2c1ffe6294aae5e8df812aee47c20e59fe0f4ec3593946e4ed069116ebb9f1`  
		Last Modified: Fri, 23 Jul 2021 00:22:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2101d5d051bcf08ee904abd42115ca10712771f5cf1c4e0b423529da86e741a6`  
		Last Modified: Mon, 02 Aug 2021 23:56:03 GMT  
		Size: 3.1 MB (3061914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fcbda204aa9670b17dc8d7e97735f16ce74df3a60c6d2d9569f7318a335249`  
		Last Modified: Mon, 02 Aug 2021 23:56:09 GMT  
		Size: 44.3 MB (44338267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3a655d5b411d7076572c42fcece59f2189f79f1c6bfa2759554c0fe12a0ec3`  
		Last Modified: Mon, 02 Aug 2021 23:56:01 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.2` - linux; ppc64le

```console
$ docker pull redmine@sha256:ecdb00827fcf83f2f12c122af3ffc2420a6faa270cd7b048c9756f927f7c77fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219650618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57391c1536ff89c22d27544dc68890a924a8d455796c92bdc28721108b71a53c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 00:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 00:33:06 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 00:52:18 GMT
ENV RUBY_MAJOR=2.7
# Fri, 23 Jul 2021 00:52:28 GMT
ENV RUBY_VERSION=2.7.4
# Fri, 23 Jul 2021 00:52:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Fri, 23 Jul 2021 01:01:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 01:01:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 01:01:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 01:01:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 01:01:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 01:01:58 GMT
CMD ["irb"]
# Sat, 24 Jul 2021 02:42:41 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sat, 24 Jul 2021 02:46:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Jul 2021 02:46:14 GMT
ENV RAILS_ENV=production
# Sat, 24 Jul 2021 02:46:17 GMT
WORKDIR /usr/src/redmine
# Sat, 24 Jul 2021 02:46:19 GMT
ENV HOME=/home/redmine
# Sat, 24 Jul 2021 02:46:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:16:59 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 23:17:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 23:17:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:23:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:23:26 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:23:29 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:23:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:23:37 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:23:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f17b372a9c9122b881c2d22680e91d78ef4c329094595c61f5acb2523f41b7`  
		Last Modified: Fri, 23 Jul 2021 01:35:00 GMT  
		Size: 12.7 MB (12704330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064c16cae6894266abd8c9d33cfb671a4ebb2705d8b8bb7495bafc50c3dcd344`  
		Last Modified: Fri, 23 Jul 2021 01:34:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76d2032e7e646d23109ea1a55abb581c169350b85836914155a6837d64eb757`  
		Last Modified: Fri, 23 Jul 2021 01:36:48 GMT  
		Size: 15.0 MB (14997545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996a3088f8cd5e20b9f19c3aebdd4a6228a85b6c0a83f9dde8e2a5ec82976d3`  
		Last Modified: Fri, 23 Jul 2021 01:36:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acdc172d0fc27092df5794b7a17e2c42e7f2497e85086076f490e273db428fe`  
		Last Modified: Sat, 24 Jul 2021 03:36:05 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fe4ded3f0db610cc9dca87e98b2305c850cbaf595886ccb44e3492ad727b18`  
		Last Modified: Sat, 24 Jul 2021 03:36:28 GMT  
		Size: 101.3 MB (101327533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14617640fcda340a6bc04fd1c65d4183ad0dd01a4e3b44fb313d164071471e95`  
		Last Modified: Sat, 24 Jul 2021 03:36:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1b361a5633d0ca044cc644bddc99329645edadfff1cbb48e966deb9b0d079a`  
		Last Modified: Sat, 24 Jul 2021 03:36:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bfbd857622d0239bfa521d75318f40925e9e4608a62a4be7abc2bc89801ec3`  
		Last Modified: Mon, 02 Aug 2021 23:30:32 GMT  
		Size: 3.1 MB (3061921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e4b836dd92fc0980e6e61a697cc881ceb76ca811af742788283ab3211698e1`  
		Last Modified: Mon, 02 Aug 2021 23:30:38 GMT  
		Size: 57.0 MB (57001331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2976222796409af9d080f03664b07bc2a177c8b37d29e7937c0620ba5f908d03`  
		Last Modified: Mon, 02 Aug 2021 23:30:31 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.2` - linux; s390x

```console
$ docker pull redmine@sha256:33d5a2369e443a1bb092e9da696586fae6988113fc4ef99bf98b5af5e03135f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202554693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f13509159fb8e3ef52d7620d4ef325ebe2d7a388fec2faf172536b64ee9ae9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:21:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:21:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:37:51 GMT
ENV RUBY_MAJOR=2.7
# Tue, 17 Aug 2021 04:37:51 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 17 Aug 2021 04:37:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 17 Aug 2021 04:40:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:40:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:40:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:40:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:40:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:40:24 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 13:32:53 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 13:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 13:33:28 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 13:33:28 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 13:33:28 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 13:33:29 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 13:33:29 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 17 Aug 2021 13:33:29 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 17 Aug 2021 13:33:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 13:35:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 13:35:38 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 13:35:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 13:35:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 13:35:39 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 13:35:39 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c03f413a15f7a98caaa2b027613636c576e3d98d8e1a98805c5978f2cc985f`  
		Last Modified: Tue, 17 Aug 2021 05:03:55 GMT  
		Size: 10.8 MB (10814401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ded0951dc51ddc1b38edf558277fec87d4169c1607312f67af2c4ffb9c4f19`  
		Last Modified: Tue, 17 Aug 2021 05:03:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d49ef1e1c8f0247bfa63924e738fc94dc0c4a81ec0e4b2b73df09f08d080005`  
		Last Modified: Tue, 17 Aug 2021 05:04:49 GMT  
		Size: 14.7 MB (14697415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54919ecbd2a42d851761e24bb9a1e9e71346c6ecd753a4c6b7868679823367b`  
		Last Modified: Tue, 17 Aug 2021 05:04:47 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159f1e20f87d626bb303eea037968c316700fdd1fd9fa734e8ebacf14608ab2`  
		Last Modified: Tue, 17 Aug 2021 13:42:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223675cd45b3e6a43e45f6ad1a699c278dc5effe72583bec3657746c84a2a692`  
		Last Modified: Tue, 17 Aug 2021 13:42:24 GMT  
		Size: 91.8 MB (91792621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f55e74adea5c6a7d4c0be869fe00b2451a51e188e2c0e1466d72eaad06cc9d`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cd2e454b71a3aea72543018a9596e611b94ee88301b3d5971854daab02981`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b885ccd7ef756fbf397809a3541c6cadba886972a35c3f9d9d00cc920b16ef2`  
		Last Modified: Tue, 17 Aug 2021 13:42:11 GMT  
		Size: 3.1 MB (3061920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde4808141553382cd3c73078af6ba86889e806ed72c6251287678fbce48b5ea`  
		Last Modified: Tue, 17 Aug 2021 13:42:15 GMT  
		Size: 56.4 MB (56423232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed18e7c147f9b19d7cb774a6462749d36a61882e80d34fff6912e4ed7990252d`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2.2-alpine`

```console
$ docker pull redmine@sha256:34362d64f5cac220ecf3058a2982583ec0e2cba35273960105a4cff3dc0c4a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2.2-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:429416f2012459eaa042fe2879ae170f0d1ee68b283059b2e4f855edcaae0101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150082289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a3f4194f1bef28b7e8c9cb584331cfe9876976fd1c68e194837191b82282e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 08 Jul 2021 21:57:27 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 08 Jul 2021 21:57:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 08 Jul 2021 21:57:30 GMT
ENV LANG=C.UTF-8
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_MAJOR=2.7
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 08 Jul 2021 22:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 22:18:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 22:18:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 22:18:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 22:18:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 22:18:51 GMT
CMD ["irb"]
# Wed, 14 Jul 2021 20:22:24 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 14 Jul 2021 20:22:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 14 Jul 2021 20:22:33 GMT
ENV RAILS_ENV=production
# Wed, 14 Jul 2021 20:22:33 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jul 2021 20:22:33 GMT
ENV HOME=/home/redmine
# Wed, 14 Jul 2021 20:22:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:27:15 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:27:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:27:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:27:19 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 02 Aug 2021 19:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Mon, 02 Aug 2021 19:29:21 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:29:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Mon, 02 Aug 2021 19:29:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:29:22 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:29:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5b0ea69e9ed42c49b5af449b703a12a4d2f2e28d87905af6fcd903fdae5689`  
		Last Modified: Thu, 08 Jul 2021 22:38:46 GMT  
		Size: 3.6 MB (3581658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad656ed833315b61ea674706f32c2d18d7412c7120926442af57b9131ee72ee`  
		Last Modified: Thu, 08 Jul 2021 22:38:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626f6830afc6fb7a05a8f18f2b98e4ea4db3d2dd50803e5cd2c627fe25150dc8`  
		Last Modified: Thu, 08 Jul 2021 22:40:13 GMT  
		Size: 14.4 MB (14373123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5375389679c9573d241b22905aee17b20981e2628989561698087f107fcfed4a`  
		Last Modified: Thu, 08 Jul 2021 22:40:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76a82132aeb154f32b80803eecedc3e27e062a35ae1e05284dc2d7e6c7f4f59`  
		Last Modified: Wed, 14 Jul 2021 20:35:42 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb4af997128346f54fa569d3a04180c718e02a90e90eff7161241d54deef92`  
		Last Modified: Wed, 14 Jul 2021 20:35:52 GMT  
		Size: 69.5 MB (69526214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da2816c58ef08b826f823d7b6a4126bb63594ed1109880b795c28cc4d3f032`  
		Last Modified: Wed, 14 Jul 2021 20:35:39 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f34be07349b94807cc58a0e31cecec279d0591b9a6f1f65f1dbe94a4713462`  
		Last Modified: Wed, 14 Jul 2021 20:35:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98c03ed41f8aa891bcd79e61fbb88cda198d71f5a8de4f510950e7f58aa1a15`  
		Last Modified: Mon, 02 Aug 2021 19:34:04 GMT  
		Size: 3.1 MB (3062843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08d14dd9ea01201645da35bc3855c4b0a6270b9d4ae9510f9da35fb4150e833`  
		Last Modified: Mon, 02 Aug 2021 19:34:08 GMT  
		Size: 56.7 MB (56722754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bee94fd486f4fb693e4765ade966dd49ee96cd0aff32109f156b9a2511d1af3`  
		Last Modified: Mon, 02 Aug 2021 19:34:03 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2.2-passenger`

```console
$ docker pull redmine@sha256:1227b146ef6133442f3c82299c894fd310739b1042176653e2126cf65a6bb369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2.2-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:8f065daab31dbf85b85fa0bd93241a0225439d387e574f3b3c3ed2bac86bacc5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221545515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5b06ed983bc1e6cfc65432f997639be41bac864baaa904857feedfda309362`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 17:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:28:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:28:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:28:25 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:03:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:04:03 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:04:03 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:04:03 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:04:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:26:03 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:26:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:26:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:26:48 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:26:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:26:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:26:49 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:26:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Mon, 02 Aug 2021 19:26:54 GMT
ENV PASSENGER_VERSION=6.0.10
# Mon, 02 Aug 2021 19:27:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:27:11 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Mon, 02 Aug 2021 19:27:11 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Mon, 02 Aug 2021 19:27:11 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e582c090726ff249b7e30253c7f0c11aa2cd14282a8b6cd0e8055c8615e5586`  
		Last Modified: Thu, 22 Jul 2021 17:42:40 GMT  
		Size: 14.5 MB (14509812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f96a83aedee46aef2be1d4f73cc6990dc7e756981b022462100ac16fad345`  
		Last Modified: Thu, 22 Jul 2021 17:42:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9466f2ac94d013cc74523ee4ad44d9720c72baa51d8aecc2afcba41c3754be44`  
		Last Modified: Fri, 23 Jul 2021 11:10:32 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbad6372ccefa1ce14b5eefe2fe718c0cd234b40bf9a70e3d02e131a9dd65d26`  
		Last Modified: Fri, 23 Jul 2021 11:10:45 GMT  
		Size: 94.1 MB (94087869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b93724991108aa18238773a3122f3fcd80f69331610c0a7f00656f690ac7692`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19466676666dc7f1a145b5b2534855e6f32c152cd3da118bc5536badc24da33d`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97607437e7fff6da79d61cc4ee4518344c291c99e79a6b90c113170646e975a`  
		Last Modified: Mon, 02 Aug 2021 19:33:23 GMT  
		Size: 3.1 MB (3061918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67d0866b331d96beda7e546b964c7d5dc48b95b5ea08b4624257efde2481b4a`  
		Last Modified: Mon, 02 Aug 2021 19:33:27 GMT  
		Size: 44.1 MB (44122231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed36b971f221fb68203ab38c344723da172f129a111027998d95d695bdccfa`  
		Last Modified: Mon, 02 Aug 2021 19:33:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913b642de7599d445e0069c22e66310828fb96025c0b69e5be168036e5cae921`  
		Last Modified: Mon, 02 Aug 2021 19:33:47 GMT  
		Size: 21.1 MB (21131586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c214594b43db5e8aa08dd61b352a254deb095023ee416412ce655e42e783c5`  
		Last Modified: Mon, 02 Aug 2021 19:33:45 GMT  
		Size: 4.9 MB (4919285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:alpine`

```console
$ docker pull redmine@sha256:34362d64f5cac220ecf3058a2982583ec0e2cba35273960105a4cff3dc0c4a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:429416f2012459eaa042fe2879ae170f0d1ee68b283059b2e4f855edcaae0101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150082289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a3f4194f1bef28b7e8c9cb584331cfe9876976fd1c68e194837191b82282e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 08 Jul 2021 21:57:27 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 08 Jul 2021 21:57:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 08 Jul 2021 21:57:30 GMT
ENV LANG=C.UTF-8
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_MAJOR=2.7
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 08 Jul 2021 22:15:57 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 08 Jul 2021 22:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 08 Jul 2021 22:18:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 08 Jul 2021 22:18:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 08 Jul 2021 22:18:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jul 2021 22:18:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 08 Jul 2021 22:18:51 GMT
CMD ["irb"]
# Wed, 14 Jul 2021 20:22:24 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 14 Jul 2021 20:22:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 14 Jul 2021 20:22:33 GMT
ENV RAILS_ENV=production
# Wed, 14 Jul 2021 20:22:33 GMT
WORKDIR /usr/src/redmine
# Wed, 14 Jul 2021 20:22:33 GMT
ENV HOME=/home/redmine
# Wed, 14 Jul 2021 20:22:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:27:15 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:27:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:27:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:27:19 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 02 Aug 2021 19:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Mon, 02 Aug 2021 19:29:21 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:29:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Mon, 02 Aug 2021 19:29:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:29:22 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:29:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5b0ea69e9ed42c49b5af449b703a12a4d2f2e28d87905af6fcd903fdae5689`  
		Last Modified: Thu, 08 Jul 2021 22:38:46 GMT  
		Size: 3.6 MB (3581658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad656ed833315b61ea674706f32c2d18d7412c7120926442af57b9131ee72ee`  
		Last Modified: Thu, 08 Jul 2021 22:38:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626f6830afc6fb7a05a8f18f2b98e4ea4db3d2dd50803e5cd2c627fe25150dc8`  
		Last Modified: Thu, 08 Jul 2021 22:40:13 GMT  
		Size: 14.4 MB (14373123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5375389679c9573d241b22905aee17b20981e2628989561698087f107fcfed4a`  
		Last Modified: Thu, 08 Jul 2021 22:40:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76a82132aeb154f32b80803eecedc3e27e062a35ae1e05284dc2d7e6c7f4f59`  
		Last Modified: Wed, 14 Jul 2021 20:35:42 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb4af997128346f54fa569d3a04180c718e02a90e90eff7161241d54deef92`  
		Last Modified: Wed, 14 Jul 2021 20:35:52 GMT  
		Size: 69.5 MB (69526214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14da2816c58ef08b826f823d7b6a4126bb63594ed1109880b795c28cc4d3f032`  
		Last Modified: Wed, 14 Jul 2021 20:35:39 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f34be07349b94807cc58a0e31cecec279d0591b9a6f1f65f1dbe94a4713462`  
		Last Modified: Wed, 14 Jul 2021 20:35:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98c03ed41f8aa891bcd79e61fbb88cda198d71f5a8de4f510950e7f58aa1a15`  
		Last Modified: Mon, 02 Aug 2021 19:34:04 GMT  
		Size: 3.1 MB (3062843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08d14dd9ea01201645da35bc3855c4b0a6270b9d4ae9510f9da35fb4150e833`  
		Last Modified: Mon, 02 Aug 2021 19:34:08 GMT  
		Size: 56.7 MB (56722754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bee94fd486f4fb693e4765ade966dd49ee96cd0aff32109f156b9a2511d1af3`  
		Last Modified: Mon, 02 Aug 2021 19:34:03 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:latest`

```console
$ docker pull redmine@sha256:eee3e32af89aeb43c91af7b2a61a959c4fba3f6d6cdd9695f56be8c2cefc31b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:latest` - linux; amd64

```console
$ docker pull redmine@sha256:a40f8da31978334c3d594ec8a053130245877f460f45911fb36e17be8e6e07a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195494644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c25a3b03269000ce6a7aa543599b627f73fa5bcc07debf1eb1cd10129f908dd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 17:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:28:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:28:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:28:25 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:03:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:04:03 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:04:03 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:04:03 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:04:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:26:03 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:26:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:26:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:26:48 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:26:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:26:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:26:49 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:26:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e582c090726ff249b7e30253c7f0c11aa2cd14282a8b6cd0e8055c8615e5586`  
		Last Modified: Thu, 22 Jul 2021 17:42:40 GMT  
		Size: 14.5 MB (14509812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f96a83aedee46aef2be1d4f73cc6990dc7e756981b022462100ac16fad345`  
		Last Modified: Thu, 22 Jul 2021 17:42:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9466f2ac94d013cc74523ee4ad44d9720c72baa51d8aecc2afcba41c3754be44`  
		Last Modified: Fri, 23 Jul 2021 11:10:32 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbad6372ccefa1ce14b5eefe2fe718c0cd234b40bf9a70e3d02e131a9dd65d26`  
		Last Modified: Fri, 23 Jul 2021 11:10:45 GMT  
		Size: 94.1 MB (94087869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b93724991108aa18238773a3122f3fcd80f69331610c0a7f00656f690ac7692`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19466676666dc7f1a145b5b2534855e6f32c152cd3da118bc5536badc24da33d`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97607437e7fff6da79d61cc4ee4518344c291c99e79a6b90c113170646e975a`  
		Last Modified: Mon, 02 Aug 2021 19:33:23 GMT  
		Size: 3.1 MB (3061918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67d0866b331d96beda7e546b964c7d5dc48b95b5ea08b4624257efde2481b4a`  
		Last Modified: Mon, 02 Aug 2021 19:33:27 GMT  
		Size: 44.1 MB (44122231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed36b971f221fb68203ab38c344723da172f129a111027998d95d695bdccfa`  
		Last Modified: Mon, 02 Aug 2021 19:33:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:2ba20de8f2d5813171b6b38d1e727aba839ab6cdd974c966ed2b8cd016b97c70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (196974835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2290c3ececd51c95738415fab07fc46dcc63d3a61e8099fb6c45e290ec3f0d91`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:39:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:39:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 14:39:29 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:48:33 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 14:48:33 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 14:48:34 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 14:52:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 14:52:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 14:52:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 14:52:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 14:52:55 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 14:52:55 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 01:25:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 01:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 01:26:16 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 01:26:17 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 01:26:17 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 01:26:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 20:58:44 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 20:58:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 20:58:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 21:04:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 21:04:31 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 21:04:31 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 21:04:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 21:04:32 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 21:04:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9237058b7c5120d5c6315b5d17a8c1d783be09a228b83772111ce9436c29d078`  
		Last Modified: Thu, 22 Jul 2021 15:15:34 GMT  
		Size: 10.3 MB (10345807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144b4344f580222d2fbc2f0d80fc139ab1a1ddb9a245b6073c41fdca9a93c23e`  
		Last Modified: Thu, 22 Jul 2021 15:15:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8ddbd20410764a5a44de2520de7417bddfcc0fdf2f4fa1b1d4e9ac785ce253`  
		Last Modified: Thu, 22 Jul 2021 15:17:00 GMT  
		Size: 13.9 MB (13871315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1fe10899466e387c0fc9cc130a0a900ffeb91af92c09301e387e444836d74f`  
		Last Modified: Thu, 22 Jul 2021 15:16:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b419523e1af1c8a3f9891c74f5e29e5697be8bf7bf57f23880ac551c460f07`  
		Last Modified: Fri, 23 Jul 2021 01:48:00 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d44a2001e78eed6fc3a85dbe0059a0bfae376949cda406c9304941ed617a23`  
		Last Modified: Fri, 23 Jul 2021 01:49:01 GMT  
		Size: 89.6 MB (89576912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2901c80e9a45cf66afe7fb2306719b195ec9c983783f4058ef68246bb10b95`  
		Last Modified: Fri, 23 Jul 2021 01:47:58 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b0cf9a21c70c0994e217daf5f71efd9d2f8ce8f36e062be7c831492162e99a`  
		Last Modified: Fri, 23 Jul 2021 01:47:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342031318accab10946b43b34804e02f1e0c107a6af3af5a4ebb766152ee509`  
		Last Modified: Mon, 02 Aug 2021 21:11:42 GMT  
		Size: 3.1 MB (3061919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648b6a3dac4889e5f68f30776a664fe9d62256592f37d6d2912163da56f265fa`  
		Last Modified: Mon, 02 Aug 2021 21:12:04 GMT  
		Size: 55.2 MB (55235555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5a29c2452fcab6625565bca85ff5fccfbee37e09b6f1e8455655c2735c166a`  
		Last Modified: Mon, 02 Aug 2021 21:11:38 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:cac694ac7078f02298b587000698d84cb3bb69637d30c724bd0bcac087c22f41
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190115136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3187fd285a60bd484a8586f3ee1dc8896c0c94e433a102025bf0dae4c344c1b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 02:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:15:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 02:15:46 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 02:25:03 GMT
ENV RUBY_MAJOR=2.7
# Fri, 23 Jul 2021 02:25:04 GMT
ENV RUBY_VERSION=2.7.4
# Fri, 23 Jul 2021 02:25:04 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Fri, 23 Jul 2021 02:29:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 02:29:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 02:29:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 02:29:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 02:29:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 02:29:10 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 21:18:32 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 21:19:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 21:19:37 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 21:19:37 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 21:19:38 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 21:19:39 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 03 Aug 2021 00:00:45 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 03 Aug 2021 00:00:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 03 Aug 2021 00:00:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 03 Aug 2021 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 03 Aug 2021 00:06:06 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 03 Aug 2021 00:06:07 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 03 Aug 2021 00:06:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 03 Aug 2021 00:06:08 GMT
EXPOSE 3000
# Tue, 03 Aug 2021 00:06:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011b8c791d70de7f22816846fbb07e0a1d7d419841c7e539a7cf57ef05fd50c5`  
		Last Modified: Fri, 23 Jul 2021 03:05:10 GMT  
		Size: 9.9 MB (9872218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb12a7edb0af862efa24dc389d7901cd2a894f2e106a1cef931ba0a6d675e2c0`  
		Last Modified: Fri, 23 Jul 2021 03:05:04 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b75d257bf75804e51385b730af2aaba386a501ef50517b8379966d4372c8597`  
		Last Modified: Fri, 23 Jul 2021 03:06:48 GMT  
		Size: 13.8 MB (13766962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc7c7e0536ed6ba4a99c1b8960d7c1d7365c8bc52d230b8af44d07d085916f`  
		Last Modified: Fri, 23 Jul 2021 03:06:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9cbdbb67af5c0b986c2fd6f93a2bacf3c795b046bfdf19e8f483dbc780c643`  
		Last Modified: Fri, 23 Jul 2021 21:39:57 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823bb8e3702405c250a7cc3dadba844fef162cbd0f5b9fb70a107f618dffeddf`  
		Last Modified: Fri, 23 Jul 2021 21:40:51 GMT  
		Size: 85.6 MB (85590187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930c9cc4f262f629914e37abf7b88697bc949d34260a237f8d740ea30ddf5902`  
		Last Modified: Fri, 23 Jul 2021 21:39:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e7aa3a63516ee59c6e77fd1a74b1ce0b303c09b2a97dd0ca3b0af594021030`  
		Last Modified: Fri, 23 Jul 2021 21:39:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2c8055fd9194f59346984cbb7941b37a40023edc25ab3dec3e42e9b8c01287`  
		Last Modified: Tue, 03 Aug 2021 00:12:46 GMT  
		Size: 3.1 MB (3061917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836246f3dcf57e23a39d002b3b9d9a09fedb40b5b6accc7268b28ae167eca128`  
		Last Modified: Tue, 03 Aug 2021 00:13:05 GMT  
		Size: 55.1 MB (55073644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63001a72a77f002e6a9f105ba97f4e5cb147287597ca1e71c8670c6b0e768390`  
		Last Modified: Tue, 03 Aug 2021 00:12:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:168d7ed49573c2aaecf2d0d8adcc21280d9e2c18dc1ddb19848393c9847211e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203243298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a980ba1133cf226e557df7c34d75d5c5e7bfb359db4c611a013f2dd737ac6dc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:11:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_MAJOR=2.7
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 17 Aug 2021 04:18:12 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 17 Aug 2021 04:20:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:20:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:20:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:20:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:20:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:20:13 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 14:17:02 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 14:17:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:17:25 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 14:17:26 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 14:17:26 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 14:17:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 14:17:27 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 17 Aug 2021 14:17:27 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 17 Aug 2021 14:17:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 14:19:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 14:19:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 14:19:47 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 14:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:19:48 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 14:19:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ab80b058f00336b15786a8d20ce50706c5277560dc1ddb487b7e5c9d24b10`  
		Last Modified: Tue, 17 Aug 2021 04:34:12 GMT  
		Size: 11.3 MB (11263042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6eb72cd750a3e09673b73506f2a2ce24b3006d1773293eb65b72c9a2cdf7190`  
		Last Modified: Tue, 17 Aug 2021 04:34:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2cb28558c1dd6c31a020484f10c613185335d6d30e7c7a81d3e6ffd0f374f0`  
		Last Modified: Tue, 17 Aug 2021 04:35:35 GMT  
		Size: 14.4 MB (14356587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49391d2e67bfbf4fd993b49c9be1225f0a09d4177c605548f82d49cbcfe78b99`  
		Last Modified: Tue, 17 Aug 2021 04:35:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9307e85455464623a9445ee9314b11fd777c561cefed9b38e6f9067bd30653a`  
		Last Modified: Tue, 17 Aug 2021 14:26:18 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba598bababc240a9c29cf82ac1a0b01837945e37b3cb2b17a3a55ba776227b76`  
		Last Modified: Tue, 17 Aug 2021 14:26:34 GMT  
		Size: 92.6 MB (92611086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73dc88258ae8d8cf36219a3b41b130d1e21bf4c2dfb6e1cf9c3f6b3ae2395817`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c9b592ea00c036970d3b4b7baf687de5e9394670884daa30890ab191cfe5bb`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e8230053e3f65d96319f5f2351fc906de79749654a83811bf21ea7b34f3bee`  
		Last Modified: Tue, 17 Aug 2021 14:26:17 GMT  
		Size: 3.1 MB (3061920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe117b5c157b62194a629b77cf9c9b15c6821516a74c96470c098adba14546ba`  
		Last Modified: Tue, 17 Aug 2021 14:26:22 GMT  
		Size: 56.0 MB (56031346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff9fc675e51cbab5a7a0574bbd10f6ebdc614381aa4a451a98f5884e386b455`  
		Last Modified: Tue, 17 Aug 2021 14:26:16 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:0b76e0e34b7153ffc2a922fe7cc584cdf37e53c0bf95d204bb3ff857e242f139
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202124661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d0b99035f254ab4f5e3822b673034b671859094e70176d730c1807bed1c7d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:38:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:39:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 15:39:00 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 15:46:48 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 15:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 15:49:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 15:49:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 15:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:49:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 15:49:39 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 00:10:49 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 00:11:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:11:45 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 00:11:45 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 00:11:46 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 00:11:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:53:31 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 23:53:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 23:53:36 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:54:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:54:26 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:54:26 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:54:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:54:27 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:54:27 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071d04ca5200ad3b98494cfde36960022dbd29c9afc33d685ac499fae8a05d63`  
		Last Modified: Thu, 22 Jul 2021 16:06:57 GMT  
		Size: 17.2 MB (17227285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d9d06c9e919afbd9358b702cad5bc0f28b8150722ffedb25ece16dc1f19b2`  
		Last Modified: Thu, 22 Jul 2021 16:06:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9e06bdf88f28c2f5d5893c862c6da8a6a73eb098cb2cd8eec57656d9a79b69`  
		Last Modified: Thu, 22 Jul 2021 16:08:14 GMT  
		Size: 14.0 MB (13992268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f84633b2fe0d1dff5a1fd6ab3a5506af8978d94ded4f5a0f2727ce06805d4`  
		Last Modified: Thu, 22 Jul 2021 16:08:11 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57ef59b51318d382563cb5fdab4577df04d06c56bd8885926c9a9374a31ed7c`  
		Last Modified: Fri, 23 Jul 2021 00:22:32 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2922ffac0f77cf1fd832a20d48b586a6621e1d75610c055227f6d76e34928b16`  
		Last Modified: Fri, 23 Jul 2021 00:23:09 GMT  
		Size: 95.7 MB (95703233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb8c5967872202784509fa53a811f849c714ef794dd53a40047d0c81585ce4`  
		Last Modified: Fri, 23 Jul 2021 00:22:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2c1ffe6294aae5e8df812aee47c20e59fe0f4ec3593946e4ed069116ebb9f1`  
		Last Modified: Fri, 23 Jul 2021 00:22:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2101d5d051bcf08ee904abd42115ca10712771f5cf1c4e0b423529da86e741a6`  
		Last Modified: Mon, 02 Aug 2021 23:56:03 GMT  
		Size: 3.1 MB (3061914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fcbda204aa9670b17dc8d7e97735f16ce74df3a60c6d2d9569f7318a335249`  
		Last Modified: Mon, 02 Aug 2021 23:56:09 GMT  
		Size: 44.3 MB (44338267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3a655d5b411d7076572c42fcece59f2189f79f1c6bfa2759554c0fe12a0ec3`  
		Last Modified: Mon, 02 Aug 2021 23:56:01 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:ecdb00827fcf83f2f12c122af3ffc2420a6faa270cd7b048c9756f927f7c77fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219650618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57391c1536ff89c22d27544dc68890a924a8d455796c92bdc28721108b71a53c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Fri, 23 Jul 2021 00:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 00:33:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 23 Jul 2021 00:33:06 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 00:52:18 GMT
ENV RUBY_MAJOR=2.7
# Fri, 23 Jul 2021 00:52:28 GMT
ENV RUBY_VERSION=2.7.4
# Fri, 23 Jul 2021 00:52:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Fri, 23 Jul 2021 01:01:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 23 Jul 2021 01:01:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 Jul 2021 01:01:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 Jul 2021 01:01:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 01:01:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 23 Jul 2021 01:01:58 GMT
CMD ["irb"]
# Sat, 24 Jul 2021 02:42:41 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sat, 24 Jul 2021 02:46:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Jul 2021 02:46:14 GMT
ENV RAILS_ENV=production
# Sat, 24 Jul 2021 02:46:17 GMT
WORKDIR /usr/src/redmine
# Sat, 24 Jul 2021 02:46:19 GMT
ENV HOME=/home/redmine
# Sat, 24 Jul 2021 02:46:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 23:16:59 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 23:17:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 23:17:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 23:23:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 23:23:26 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 23:23:29 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 23:23:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 23:23:37 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 23:23:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f17b372a9c9122b881c2d22680e91d78ef4c329094595c61f5acb2523f41b7`  
		Last Modified: Fri, 23 Jul 2021 01:35:00 GMT  
		Size: 12.7 MB (12704330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064c16cae6894266abd8c9d33cfb671a4ebb2705d8b8bb7495bafc50c3dcd344`  
		Last Modified: Fri, 23 Jul 2021 01:34:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76d2032e7e646d23109ea1a55abb581c169350b85836914155a6837d64eb757`  
		Last Modified: Fri, 23 Jul 2021 01:36:48 GMT  
		Size: 15.0 MB (14997545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996a3088f8cd5e20b9f19c3aebdd4a6228a85b6c0a83f9dde8e2a5ec82976d3`  
		Last Modified: Fri, 23 Jul 2021 01:36:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acdc172d0fc27092df5794b7a17e2c42e7f2497e85086076f490e273db428fe`  
		Last Modified: Sat, 24 Jul 2021 03:36:05 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fe4ded3f0db610cc9dca87e98b2305c850cbaf595886ccb44e3492ad727b18`  
		Last Modified: Sat, 24 Jul 2021 03:36:28 GMT  
		Size: 101.3 MB (101327533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14617640fcda340a6bc04fd1c65d4183ad0dd01a4e3b44fb313d164071471e95`  
		Last Modified: Sat, 24 Jul 2021 03:36:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1b361a5633d0ca044cc644bddc99329645edadfff1cbb48e966deb9b0d079a`  
		Last Modified: Sat, 24 Jul 2021 03:36:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bfbd857622d0239bfa521d75318f40925e9e4608a62a4be7abc2bc89801ec3`  
		Last Modified: Mon, 02 Aug 2021 23:30:32 GMT  
		Size: 3.1 MB (3061921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e4b836dd92fc0980e6e61a697cc881ceb76ca811af742788283ab3211698e1`  
		Last Modified: Mon, 02 Aug 2021 23:30:38 GMT  
		Size: 57.0 MB (57001331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2976222796409af9d080f03664b07bc2a177c8b37d29e7937c0620ba5f908d03`  
		Last Modified: Mon, 02 Aug 2021 23:30:31 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:33d5a2369e443a1bb092e9da696586fae6988113fc4ef99bf98b5af5e03135f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202554693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f13509159fb8e3ef52d7620d4ef325ebe2d7a388fec2faf172536b64ee9ae9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 04:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 04:21:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 17 Aug 2021 04:21:08 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 04:37:51 GMT
ENV RUBY_MAJOR=2.7
# Tue, 17 Aug 2021 04:37:51 GMT
ENV RUBY_VERSION=2.7.4
# Tue, 17 Aug 2021 04:37:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Tue, 17 Aug 2021 04:40:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 17 Aug 2021 04:40:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Aug 2021 04:40:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Aug 2021 04:40:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 04:40:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 17 Aug 2021 04:40:24 GMT
CMD ["irb"]
# Tue, 17 Aug 2021 13:32:53 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 17 Aug 2021 13:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 13:33:28 GMT
ENV RAILS_ENV=production
# Tue, 17 Aug 2021 13:33:28 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Aug 2021 13:33:28 GMT
ENV HOME=/home/redmine
# Tue, 17 Aug 2021 13:33:29 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 17 Aug 2021 13:33:29 GMT
ENV REDMINE_VERSION=4.2.2
# Tue, 17 Aug 2021 13:33:29 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Tue, 17 Aug 2021 13:33:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 17 Aug 2021 13:35:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 13:35:38 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Aug 2021 13:35:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 17 Aug 2021 13:35:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Aug 2021 13:35:39 GMT
EXPOSE 3000
# Tue, 17 Aug 2021 13:35:39 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c03f413a15f7a98caaa2b027613636c576e3d98d8e1a98805c5978f2cc985f`  
		Last Modified: Tue, 17 Aug 2021 05:03:55 GMT  
		Size: 10.8 MB (10814401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ded0951dc51ddc1b38edf558277fec87d4169c1607312f67af2c4ffb9c4f19`  
		Last Modified: Tue, 17 Aug 2021 05:03:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d49ef1e1c8f0247bfa63924e738fc94dc0c4a81ec0e4b2b73df09f08d080005`  
		Last Modified: Tue, 17 Aug 2021 05:04:49 GMT  
		Size: 14.7 MB (14697415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54919ecbd2a42d851761e24bb9a1e9e71346c6ecd753a4c6b7868679823367b`  
		Last Modified: Tue, 17 Aug 2021 05:04:47 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159f1e20f87d626bb303eea037968c316700fdd1fd9fa734e8ebacf14608ab2`  
		Last Modified: Tue, 17 Aug 2021 13:42:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223675cd45b3e6a43e45f6ad1a699c278dc5effe72583bec3657746c84a2a692`  
		Last Modified: Tue, 17 Aug 2021 13:42:24 GMT  
		Size: 91.8 MB (91792621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f55e74adea5c6a7d4c0be869fe00b2451a51e188e2c0e1466d72eaad06cc9d`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013cd2e454b71a3aea72543018a9596e611b94ee88301b3d5971854daab02981`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b885ccd7ef756fbf397809a3541c6cadba886972a35c3f9d9d00cc920b16ef2`  
		Last Modified: Tue, 17 Aug 2021 13:42:11 GMT  
		Size: 3.1 MB (3061920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde4808141553382cd3c73078af6ba86889e806ed72c6251287678fbce48b5ea`  
		Last Modified: Tue, 17 Aug 2021 13:42:15 GMT  
		Size: 56.4 MB (56423232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed18e7c147f9b19d7cb774a6462749d36a61882e80d34fff6912e4ed7990252d`  
		Last Modified: Tue, 17 Aug 2021 13:42:10 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:passenger`

```console
$ docker pull redmine@sha256:1227b146ef6133442f3c82299c894fd310739b1042176653e2126cf65a6bb369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:passenger` - linux; amd64

```console
$ docker pull redmine@sha256:8f065daab31dbf85b85fa0bd93241a0225439d387e574f3b3c3ed2bac86bacc5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221545515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5b06ed983bc1e6cfc65432f997639be41bac864baaa904857feedfda309362`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:20:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:20:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 22 Jul 2021 17:20:06 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_MAJOR=2.7
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 22 Jul 2021 17:25:56 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 22 Jul 2021 17:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 		libgdbm-compat-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 22 Jul 2021 17:28:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 22 Jul 2021 17:28:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 17:28:25 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 22 Jul 2021 17:28:25 GMT
CMD ["irb"]
# Fri, 23 Jul 2021 11:03:34 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 23 Jul 2021 11:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 11:04:03 GMT
ENV RAILS_ENV=production
# Fri, 23 Jul 2021 11:04:03 GMT
WORKDIR /usr/src/redmine
# Fri, 23 Jul 2021 11:04:03 GMT
ENV HOME=/home/redmine
# Fri, 23 Jul 2021 11:04:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 02 Aug 2021 19:26:03 GMT
ENV REDMINE_VERSION=4.2.2
# Mon, 02 Aug 2021 19:26:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=e6fbe9279939a95953d377ef76f180f204a1f3da5229a1d56055d658de7198f6
# Mon, 02 Aug 2021 19:26:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 02 Aug 2021 19:26:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:26:48 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 02 Aug 2021 19:26:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Mon, 02 Aug 2021 19:26:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 02 Aug 2021 19:26:49 GMT
EXPOSE 3000
# Mon, 02 Aug 2021 19:26:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Mon, 02 Aug 2021 19:26:54 GMT
ENV PASSENGER_VERSION=6.0.10
# Mon, 02 Aug 2021 19:27:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 02 Aug 2021 19:27:11 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Mon, 02 Aug 2021 19:27:11 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Mon, 02 Aug 2021 19:27:11 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603cdcbaa70592c67c84ffc51d232163508c6c3480916880fdb7820e7c9b9c17`  
		Last Modified: Thu, 22 Jul 2021 17:41:27 GMT  
		Size: 12.6 MB (12562773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d872ffd3f2a7e6eabea705393351362003a0c6bdee8956d5a53f73dd0b40be`  
		Last Modified: Thu, 22 Jul 2021 17:41:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e582c090726ff249b7e30253c7f0c11aa2cd14282a8b6cd0e8055c8615e5586`  
		Last Modified: Thu, 22 Jul 2021 17:42:40 GMT  
		Size: 14.5 MB (14509812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6f96a83aedee46aef2be1d4f73cc6990dc7e756981b022462100ac16fad345`  
		Last Modified: Thu, 22 Jul 2021 17:42:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9466f2ac94d013cc74523ee4ad44d9720c72baa51d8aecc2afcba41c3754be44`  
		Last Modified: Fri, 23 Jul 2021 11:10:32 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbad6372ccefa1ce14b5eefe2fe718c0cd234b40bf9a70e3d02e131a9dd65d26`  
		Last Modified: Fri, 23 Jul 2021 11:10:45 GMT  
		Size: 94.1 MB (94087869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b93724991108aa18238773a3122f3fcd80f69331610c0a7f00656f690ac7692`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19466676666dc7f1a145b5b2534855e6f32c152cd3da118bc5536badc24da33d`  
		Last Modified: Fri, 23 Jul 2021 11:10:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97607437e7fff6da79d61cc4ee4518344c291c99e79a6b90c113170646e975a`  
		Last Modified: Mon, 02 Aug 2021 19:33:23 GMT  
		Size: 3.1 MB (3061918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67d0866b331d96beda7e546b964c7d5dc48b95b5ea08b4624257efde2481b4a`  
		Last Modified: Mon, 02 Aug 2021 19:33:27 GMT  
		Size: 44.1 MB (44122231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed36b971f221fb68203ab38c344723da172f129a111027998d95d695bdccfa`  
		Last Modified: Mon, 02 Aug 2021 19:33:22 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913b642de7599d445e0069c22e66310828fb96025c0b69e5be168036e5cae921`  
		Last Modified: Mon, 02 Aug 2021 19:33:47 GMT  
		Size: 21.1 MB (21131586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c214594b43db5e8aa08dd61b352a254deb095023ee416412ce655e42e783c5`  
		Last Modified: Mon, 02 Aug 2021 19:33:45 GMT  
		Size: 4.9 MB (4919285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
