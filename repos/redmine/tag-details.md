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
-	[`redmine:4.1.5`](#redmine415)
-	[`redmine:4.1.5-alpine`](#redmine415-alpine)
-	[`redmine:4.1.5-passenger`](#redmine415-passenger)
-	[`redmine:4.2`](#redmine42)
-	[`redmine:4.2-alpine`](#redmine42-alpine)
-	[`redmine:4.2-passenger`](#redmine42-passenger)
-	[`redmine:4.2.3`](#redmine423)
-	[`redmine:4.2.3-alpine`](#redmine423-alpine)
-	[`redmine:4.2.3-passenger`](#redmine423-passenger)
-	[`redmine:alpine`](#redminealpine)
-	[`redmine:latest`](#redminelatest)
-	[`redmine:passenger`](#redminepassenger)

## `redmine:4`

```console
$ docker pull redmine@sha256:6654dea65d5e39a0419ac63df0e0ad6331f5da0f7831043663eca917fb5d3eea
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
$ docker pull redmine@sha256:68e8092f1d13c3e52d3aa807f7c0e5d55239fa8e032135a594f8da178b467623
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194811230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f79246dbb550a5674aad1819a04d406d7df4f3a807a5372f24043786984f50`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:32:12 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 23:34:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:34:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:35:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:35:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:30:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:31:12 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:31:12 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:31:12 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:31:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:31:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:32:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:01 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:32:01 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:32:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:32:01 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:32:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90b12affd87b4d38a8fcc325810d1d00be3ab2e7bcd8190a9c00b84593c078d`  
		Last Modified: Wed, 17 Nov 2021 23:52:50 GMT  
		Size: 14.5 MB (14510130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8d736be43fd318e714161260dcdb9952dad0c90be69d5376da0b7966ffc5a8`  
		Last Modified: Wed, 17 Nov 2021 23:52:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3019ede46444af81796abfe67c49e2fbabb9db7caeae19ac3c3af640d51440`  
		Last Modified: Thu, 18 Nov 2021 20:37:49 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f459f77e5a0c1928192bf809bbd6e9bb46b6ba4ab21a817e21f49658d9a33d`  
		Last Modified: Thu, 18 Nov 2021 20:38:03 GMT  
		Size: 94.1 MB (94089001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8ef100ec39cd24ccf9e86757ced4ffc4872d201ef840683fa0d01bbd478b2f`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676f59fd8e0144196b1551c4862751c016db7e7bd85d9c5ea7f47fd931c64aa`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d506c2d549b6dae794e30276395ea85c0e257a4c3afb861eee7a80aca20209`  
		Last Modified: Thu, 18 Nov 2021 20:37:47 GMT  
		Size: 3.1 MB (3063251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82700c911def9390d43716a8985c018ac47b62ef650f69a942d86a03fd4510ec`  
		Last Modified: Thu, 18 Nov 2021 20:37:51 GMT  
		Size: 43.4 MB (43425778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0cd4260e9359c26c12c25c14dcf660812c0bd324b62fc86c3f52dca359a33a`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm variant v5

```console
$ docker pull redmine@sha256:bf6bb00f96a0b12b11262fb56ebe66a814137dca38016393734d0cea84d063f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196300195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f73d796e667ea07abd3855ad0147a9bbbb9beb37276b61162547c05961f5059`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 20:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:53:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 20:53:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:30:49 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 21:30:50 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 21:30:50 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 21:35:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 21:35:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 21:35:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 21:35:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:35:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 21:35:11 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 14:36:38 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 14:37:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 14:37:57 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 14:37:57 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 14:37:58 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 14:37:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 14:38:00 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 14:38:00 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 14:38:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 14:43:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 14:43:45 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 14:43:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 14:43:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 14:43:47 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 14:43:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58fbebb8e6e22b1601002ddb4252e30c3750edfb93b87424f6c1a971c665bf`  
		Last Modified: Wed, 17 Nov 2021 21:59:40 GMT  
		Size: 10.3 MB (10349405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484eb5c97eceafe50be8deba254566cb365fd68cb0baa2e5418ecece614c2728`  
		Last Modified: Wed, 17 Nov 2021 21:59:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8a3180a4fd6dc5eb70d66bd3e4082e4d6a82432c594b34e550d6feab30b262`  
		Last Modified: Wed, 17 Nov 2021 22:04:27 GMT  
		Size: 13.9 MB (13871351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc80340d626dbcb066ecdc739e235877d725bc16934f56afcf1f9f7a5b1823b`  
		Last Modified: Wed, 17 Nov 2021 22:04:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29e7fbae5e92244d8b1ed80457eecf320d173303fdb99245a84599906c7666`  
		Last Modified: Thu, 18 Nov 2021 14:59:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b55931caf7268bdad6b385d5c79741a8a295c347cfb9fd8f639d1ba7c2a8d8`  
		Last Modified: Thu, 18 Nov 2021 15:00:15 GMT  
		Size: 89.6 MB (89577773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070f8378574f87a9aef84e45e5adeb05df20f39cb6d6d897df940e984084c75`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a18cbf12df5da376627c3bdee43d3813e66f035f637a7c2501f73ad4a1ba60`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2a5a07dcbabe1e7be1e52efada576b24511465600e52c6d7d19effc57d263`  
		Last Modified: Thu, 18 Nov 2021 14:59:15 GMT  
		Size: 3.1 MB (3063252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f00725466b5aef82f5484942c445b1712ba8af31b3158af20834ea48204588`  
		Last Modified: Thu, 18 Nov 2021 14:59:35 GMT  
		Size: 54.5 MB (54547862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49a55ad2f42152245a2269b8f870edac4fcbd328d63a8d72a3da64e94478c59`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm variant v7

```console
$ docker pull redmine@sha256:c92262d9b7966c7a14f0ca89c5545aa12583798740b923fa82f9025a40c1f246
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189440908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054a0dc932e7b49f5a55f646fb5d28485df4f2de75bff349cec7e7934c0fb639`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 08:17:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:17:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 18 Nov 2021 08:17:06 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 08:53:42 GMT
ENV RUBY_MAJOR=2.7
# Thu, 18 Nov 2021 08:53:42 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 18 Nov 2021 08:53:43 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 18 Nov 2021 08:57:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 18 Nov 2021 08:57:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Nov 2021 08:57:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Nov 2021 08:57:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 08:57:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 18 Nov 2021 08:57:49 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 19:59:23 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:00:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:00:29 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:00:30 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:00:30 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:00:32 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:00:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:00:38 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:05:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:05:55 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:05:56 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:05:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:05:57 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:05:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8e57706e11dcf2202a1ed28d022f7fe3daa306f06bf5311fee3d20b17f772`  
		Last Modified: Thu, 18 Nov 2021 09:24:19 GMT  
		Size: 9.9 MB (9872912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad345207fbbb28e02d7546fe9ec9b203219b39a7b6fe1a2c55d63e665ce8dd`  
		Last Modified: Thu, 18 Nov 2021 09:24:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d25e541e934fefcd6dcfff4226d06801527c28c5f31506d802ed03121e1320b`  
		Last Modified: Thu, 18 Nov 2021 09:29:28 GMT  
		Size: 13.8 MB (13767299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3459bd8cf29be58005e7ad4da22bdba7402a2d607ca5295fe58bac3d98f3b4`  
		Last Modified: Thu, 18 Nov 2021 09:29:21 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9465b374f5ec3e1d43e6b89b84be958e52aaf49669b4e1bbcb2f7bde6546969`  
		Last Modified: Thu, 18 Nov 2021 20:20:44 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f9e4f806a27273fd0d86a752ec0c68d34f29a4e216ac255ea3b98c2f8dee89`  
		Last Modified: Thu, 18 Nov 2021 20:21:39 GMT  
		Size: 85.6 MB (85589945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c32930c81becf489baf6eb5aa96cbcab402cc72b77824a8d5f3ef1164e827e`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874cebd85eed66ba44ad4ac91fc7a5c904705679507db88675f20541e50a55f5`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd024f80cae41f24e51ccb8fe006e4561cd72d216a72741b11521e70ecc17f`  
		Last Modified: Thu, 18 Nov 2021 20:20:46 GMT  
		Size: 3.1 MB (3063253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ddc84607a7f4665334e4c31b9dd59b1ba40a30a55fb387506edc020bb2c24`  
		Last Modified: Thu, 18 Nov 2021 20:21:06 GMT  
		Size: 54.4 MB (54388903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2cac2bcb44446a910b068386b9b7b82991cd1aed0cea1e34f6e772c6711ba5`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:86d444c24d077794c0c2cc949e49527863c9ca44e518c17e370b02eb4000216a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202113715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42218f16d6dac2e546b0a2281ab4659b776bbf51ec6e4acfbede94911bc9dcdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:41:19 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:41:20 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:41:21 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:43:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:43:17 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:46:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:46:40 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:46:41 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:46:42 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:46:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:46:44 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 19:46:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 19:46:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:49:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:49:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:49:40 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:49:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e74dfb7a4c0fdaf06af6628a5256217d8dc0d66250a1fbc0c123f00b986e22`  
		Last Modified: Wed, 17 Nov 2021 09:53:40 GMT  
		Size: 14.1 MB (14143923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb526ffb8eba3317294cf51375a464a78d261132b6b7491f254cf7a4a156682`  
		Last Modified: Wed, 17 Nov 2021 09:53:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21518ac2e5bab0f6dfc5e5d56cc37c2ddfe56b2be0f94f479a28844eda6b01df`  
		Last Modified: Wed, 17 Nov 2021 19:56:25 GMT  
		Size: 1.6 KB (1626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76248d3153c26ceb5416c50118694725c0c7d4ce7823824bd66101dc2c5a010d`  
		Last Modified: Wed, 17 Nov 2021 19:56:41 GMT  
		Size: 92.6 MB (92614747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31701ff7128027b1906c22a7653245cdb3cfac2d03494df00e25be248e743991`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac4b0eb26c86bcfc93c2657dfbeb8e1d3ef40e8785866c46e13be70741ec74b`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62ad39d6bc57963dc25a1ff3af302f01bf0d29bf1d984b097d829bcef8e71d3`  
		Last Modified: Wed, 17 Nov 2021 19:56:24 GMT  
		Size: 3.1 MB (3063387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c77a0ff1cda155087e0a1fd87440c1fd1f0de88ddcd0f7b027500ca9b1c5df9`  
		Last Modified: Wed, 17 Nov 2021 19:56:31 GMT  
		Size: 55.1 MB (55102701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe9431487572557c36e17868ec1e44d823b725205b047bd9b29f8cb63fea74`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; 386

```console
$ docker pull redmine@sha256:541bbc59f1f2165794af255e943fd64e76f231e68941d6e893fb057442a80b34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201449024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8a65a7d03b8eef85a6b4790bedd723f2249542a83c9e248f86e8bfe4ab2be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 18:58:23 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 19:02:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:02:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:02:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:02:53 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:36:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:36:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:36:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:36:42 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:36:43 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 00:36:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 00:36:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:37:43 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:37:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:37:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:37:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:37:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59002f4fc409c3fdcbd829fcc8f9d9186a49f4b1977b2c959714978bd07c75`  
		Last Modified: Wed, 17 Nov 2021 19:19:42 GMT  
		Size: 14.0 MB (13992752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1a3cc73f29df585791125514b63252077c65f4a1e212d1021c4e3020df3dd8`  
		Last Modified: Wed, 17 Nov 2021 19:19:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cff4a558af0642405c8aec1556aebdbaf4c9a86c0632d964e532934f76466c`  
		Last Modified: Thu, 18 Nov 2021 00:43:12 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700278801433da9ce13b80f7e86e2e5368cccf0e303e9862c537a154f05a540a`  
		Last Modified: Thu, 18 Nov 2021 00:43:36 GMT  
		Size: 95.7 MB (95702657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af28efd287aeb351d175e3c0f5ed184fa551cd1af7172bb7791a60a0537af9de`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8937baf10e23d531e21069ea81323b01572eee4aed6f64640685bb7ffaab8`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eb84ecf78a6f2698456d871cbe794d0bb45a6cece674d3d8251894cb1c1a01`  
		Last Modified: Thu, 18 Nov 2021 00:43:11 GMT  
		Size: 3.1 MB (3063250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676ab58b071fabf24debb26ce72f971b94290b362f51e44b6a19c2fe9b3371a9`  
		Last Modified: Thu, 18 Nov 2021 00:43:18 GMT  
		Size: 43.7 MB (43654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940c5fbe3e6915f01902f8855bf33b917442025553bce6ff1b11353827a7b58`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; ppc64le

```console
$ docker pull redmine@sha256:bc9e80acf291615ffb33dbb7ddbc4a7565d1de7ea50ce44aa4333ba6d433e342
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218955951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cacd26122b566b805c31159146c851de24b306f5db8b8302285459e98d9913b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 03:30:22 GMT
ADD file:c0f8b5d4d419bef7a494df5330ecf7bbea3cbb6462308ca0b2f26771f125dea0 in / 
# Wed, 17 Nov 2021 03:30:29 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:17:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 13:17:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 13:56:53 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 13:56:56 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 13:56:58 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 14:03:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 14:03:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 14:03:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 14:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 14:03:22 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 14:03:24 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 12:26:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 12:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 12:29:27 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 12:29:33 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 12:29:36 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 12:29:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 12:29:46 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 12:29:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 12:29:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 12:33:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 12:34:04 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 12:34:05 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 12:34:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 12:34:08 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 12:34:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:459de0a111d5c931674a5150ef4ae6bb1ffb1685380f4aafdba04a37d556c5de`  
		Last Modified: Wed, 17 Nov 2021 03:58:14 GMT  
		Size: 30.6 MB (30562278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4a8cb8add512175dbaeb682e1d37722eb039847e94d43b2c548f6bf9f4566`  
		Last Modified: Wed, 17 Nov 2021 14:30:35 GMT  
		Size: 12.7 MB (12705482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02accf8c69e0fb54236daa23b1409d80e215845f8d744672e8be1de6353c73f4`  
		Last Modified: Wed, 17 Nov 2021 14:30:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437d94d7e24e0cdbb2879c03363f9b475da2c6828f1d6efd64e6ace62304f455`  
		Last Modified: Wed, 17 Nov 2021 14:34:16 GMT  
		Size: 15.0 MB (14997053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b39e4205e8291bddd16d32f0575a50d2838f1141cdb3dfe1e4502de89dbb1bc`  
		Last Modified: Wed, 17 Nov 2021 14:34:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57265642992f45aec31dcaf12b72927b3e6854aae997a3fd18e7bda9b690b4d`  
		Last Modified: Thu, 18 Nov 2021 12:53:53 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27021a17b8f3615fdf08ab3a986a106ed0d9e0238da2792c9469b5fc2aa38b18`  
		Last Modified: Thu, 18 Nov 2021 12:54:12 GMT  
		Size: 101.3 MB (101327196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9324734dc2a75f7aa6a9f8488945f3181ad665697ef6c85255ff8ab2ebf892f7`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596f052e5e4de085618e67aac634fafdbd606e08d0d7f9f5017875238164e5a8`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c13ff8c3199f6a072a472251f1deeddc585eea60ad17ea7b97b08c06734d2`  
		Last Modified: Thu, 18 Nov 2021 12:53:51 GMT  
		Size: 3.1 MB (3063249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3621788bcdb3caeb1153a2622168e546f76b07dd3cc425b4bb733bbbc94d097`  
		Last Modified: Thu, 18 Nov 2021 12:53:58 GMT  
		Size: 56.3 MB (56296448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5cd3a2223e6188ca96341a558e604ad5bfecb69d6e230c836d280401865d7`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4` - linux; s390x

```console
$ docker pull redmine@sha256:49a1c1b85f8ccd222764c18d3694feaf0642800543699062e12064d13fecc636
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201879289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd54a6734cf67e04ecc514a8756a628f6b402e434e592dc8d1bf2a75b15627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:37:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:37:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:37:16 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:31:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:32:10 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:32:10 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:32:10 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:32:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 20:32:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:34:07 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:34:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:34:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:34:08 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:34:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa70e45053269d04d1a7217aca754f0b1fd37826bacef60c3e79535af03de7e`  
		Last Modified: Wed, 17 Nov 2021 09:50:18 GMT  
		Size: 14.7 MB (14697150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6665bc1be788124ffa49dc9aca2a874932441c39767aac3628a05b46b7f808`  
		Last Modified: Wed, 17 Nov 2021 09:50:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ad94a5ab88cff035b5e7ab928b3855131115a475ac3f69d13d3b648539b059`  
		Last Modified: Wed, 17 Nov 2021 20:39:22 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef81635c9981af53c3728bbbdf8957635a0b7afccb029ae985a6fe7e6ae527`  
		Last Modified: Wed, 17 Nov 2021 20:39:34 GMT  
		Size: 91.8 MB (91791039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8be6a475176385654d74664b9bc12bade950866233a6eb369175876849a61a9`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d214f8c5411f63986c0d7ee3a9032324738c7b89be0432e0ff9616a27a72485f`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a849b87f96d4317e30bb0352a51b94195d07907f8535be33300f0452e6808655`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05a462fbf41e321955f3c91b6791ba04c37145f855bda5355c75973c4705c2`  
		Last Modified: Wed, 17 Nov 2021 20:39:25 GMT  
		Size: 55.7 MB (55739301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740e646b3a43cb2398040cad7d9e0ed87da62a1457bd92bcc4d0c5a0b8be27c`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4-alpine`

```console
$ docker pull redmine@sha256:cf4ec4d559c84d289809ddc6554057e6522d3720200a340c70ba098c12202c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:518ba4effd92c427ef19922743eea649ed001436d8a66fe0de469abb2de00949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149044368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a04de41bf1795abeee36effc817551b3de5069209d3ec827816281c81211a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_MAJOR=2.7
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_VERSION=2.7.4
# Sat, 13 Nov 2021 06:44:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Sat, 13 Nov 2021 06:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:47:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:47:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:47:56 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:28:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:29:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:29:07 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:29:08 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:29:08 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_VERSION=4.2.3
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Sat, 13 Nov 2021 14:29:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:29:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:31:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:31:21 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:31:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:31:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:31:22 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:31:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e81c0605571c3961987ae1ce872ebef2b5bcb439010c194e90b47282556c32d`  
		Last Modified: Sat, 13 Nov 2021 06:58:25 GMT  
		Size: 14.0 MB (13994126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2814005984530d27bc89e1c810fb8cb01371038a28bc3d85a1e95b710d9e043e`  
		Last Modified: Sat, 13 Nov 2021 06:58:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171914095295d927972128e1f66156ce389cb697d40fc6d7ea68c919861015e`  
		Last Modified: Sat, 13 Nov 2021 14:36:45 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9802858485f172f49a49aa23ebc2ef97aa9a7dff598d4d6b18f27e107ae24436`  
		Last Modified: Sat, 13 Nov 2021 14:36:55 GMT  
		Size: 69.5 MB (69548252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5b29e3b352df46dbdcf96478507ab2ace06abee4b91e86cea6852a73067d98`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd79647c11e0ebdbaa7b41c71d969403768f7950e69f1b9eda5545fe42e86b3`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20504c29a1f01e91c83c2e1e82a90fb05c118bbf74d44fa621ec588a179bce4b`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 3.1 MB (3064272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7d43b9df6162fdd2b107724ff288c851a49738e7e04fa16cd34fddde661b04`  
		Last Modified: Sat, 13 Nov 2021 14:36:48 GMT  
		Size: 56.0 MB (56029256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561c4b4d66001dcdc5ff09131812075d6a6d4f6430e175565724033921e826f1`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:1d213433b63a0ead8a70d021a5c132c60e4e748bbc9ca9a924df306b70f3244c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:e18a6ae0dcfc40dd6410992648ef1012830deff650ee75fe39dbfe061d12a342
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220974188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27853838e5a87da41ee207d9032436259a01c1e6474419f2c9c796931a4c34eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:32:12 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 23:34:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:34:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:35:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:35:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:30:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:31:12 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:31:12 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:31:12 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:31:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:31:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:32:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:01 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:32:01 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:32:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:32:01 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:32:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 18 Nov 2021 20:32:05 GMT
ENV PASSENGER_VERSION=6.0.12
# Thu, 18 Nov 2021 20:32:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:22 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 18 Nov 2021 20:32:23 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 18 Nov 2021 20:32:23 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90b12affd87b4d38a8fcc325810d1d00be3ab2e7bcd8190a9c00b84593c078d`  
		Last Modified: Wed, 17 Nov 2021 23:52:50 GMT  
		Size: 14.5 MB (14510130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8d736be43fd318e714161260dcdb9952dad0c90be69d5376da0b7966ffc5a8`  
		Last Modified: Wed, 17 Nov 2021 23:52:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3019ede46444af81796abfe67c49e2fbabb9db7caeae19ac3c3af640d51440`  
		Last Modified: Thu, 18 Nov 2021 20:37:49 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f459f77e5a0c1928192bf809bbd6e9bb46b6ba4ab21a817e21f49658d9a33d`  
		Last Modified: Thu, 18 Nov 2021 20:38:03 GMT  
		Size: 94.1 MB (94089001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8ef100ec39cd24ccf9e86757ced4ffc4872d201ef840683fa0d01bbd478b2f`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676f59fd8e0144196b1551c4862751c016db7e7bd85d9c5ea7f47fd931c64aa`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d506c2d549b6dae794e30276395ea85c0e257a4c3afb861eee7a80aca20209`  
		Last Modified: Thu, 18 Nov 2021 20:37:47 GMT  
		Size: 3.1 MB (3063251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82700c911def9390d43716a8985c018ac47b62ef650f69a942d86a03fd4510ec`  
		Last Modified: Thu, 18 Nov 2021 20:37:51 GMT  
		Size: 43.4 MB (43425778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0cd4260e9359c26c12c25c14dcf660812c0bd324b62fc86c3f52dca359a33a`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b65724c681012a606e5d41cfbe37546052cd471086212e239e21a5dfbdadaa1`  
		Last Modified: Thu, 18 Nov 2021 20:38:23 GMT  
		Size: 21.2 MB (21238341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916ee64f10c4bd1e7cf1bfcadb56aba80a65c2b1193197e39b1fa3be4829a355`  
		Last Modified: Thu, 18 Nov 2021 20:38:20 GMT  
		Size: 4.9 MB (4924617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0`

```console
$ docker pull redmine@sha256:4d822d5d019f1969c1f0e218654d660c61828080868166d0b37353d2507a30f0
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
$ docker pull redmine@sha256:c44c0548e533e54f10782bb4cb14b7edc63926122edaba5cdc13fb8a11929196
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205095735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0153b08dec0342bdeb4960f121672a3a03e912a9a521a71e68cd20a3261b578d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 23:47:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:47:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:47:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:47:17 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:32:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:34:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:34:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:34:43 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:34:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:34:43 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 20:34:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 20:34:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:36:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:36:48 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:36:48 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:36:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:36:49 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:36:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0513aa66c0fb3e8b2ca883a3e8d1981bbfe8bfb788a9a888b723787293986e7d`  
		Last Modified: Wed, 17 Nov 2021 23:53:54 GMT  
		Size: 21.5 MB (21467890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dcedae4b9e16af3b588b2e085edcdc9b5895d6dcbd0f3c7886780233e285c2`  
		Last Modified: Wed, 17 Nov 2021 23:53:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31fda4ca0ea33330c7d7c55c465fd2b24a8bd41e15481cc208eddeb93c3aa72`  
		Last Modified: Thu, 18 Nov 2021 20:38:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9647538f90e6d8079158a334291526054be9f9baa1d00e0b4828a9363e3f92`  
		Last Modified: Thu, 18 Nov 2021 20:39:39 GMT  
		Size: 81.2 MB (81200246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8972d6130a8fe50a34eb323dcffca6ccfc098d985f074e08e3badf25890af0`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56991c7d2e73b3615e48d4b75afc4bc168af36045ebe4c66eb1034d29ca75996`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0ebf9fce3a7b8a16c7566fa9ed1edbeab1d2ba828b7b322c5da4418501d569`  
		Last Modified: Thu, 18 Nov 2021 20:39:24 GMT  
		Size: 2.5 MB (2542545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c91fe34b38ffbb891de3fffb08ad12983ba88aa7f48ab4d74b3ad502aeb49a`  
		Last Modified: Thu, 18 Nov 2021 20:39:33 GMT  
		Size: 60.2 MB (60161990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd17ac1130132640ad42caac391d9ac3edf34cf6031e72afd6d506f5c8d982b`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm variant v5

```console
$ docker pull redmine@sha256:626796677c39ac694e716bb310af5cd0fc5bda937047b59ce65ef6fe80663ee4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194751147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00afec53b5b1461458224d8ca8f6a7c3d13c017d9257ede01d0ba8c05997da8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 20:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:53:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 20:53:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:48:32 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 21:48:33 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 21:48:33 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 21:52:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 21:52:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 21:53:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 21:53:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:53:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 21:53:02 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 14:44:02 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 14:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 14:52:14 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 14:52:14 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 14:52:15 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 14:52:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 14:52:17 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 14:52:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 14:52:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 14:58:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 14:58:16 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 14:58:16 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 14:58:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 14:58:17 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 14:58:18 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58fbebb8e6e22b1601002ddb4252e30c3750edfb93b87424f6c1a971c665bf`  
		Last Modified: Wed, 17 Nov 2021 21:59:40 GMT  
		Size: 10.3 MB (10349405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484eb5c97eceafe50be8deba254566cb365fd68cb0baa2e5418ecece614c2728`  
		Last Modified: Wed, 17 Nov 2021 21:59:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036dbb00becdfbc8994f79e0968b90235a36a6cd3adc53d1b0c485d366b86b8e`  
		Last Modified: Wed, 17 Nov 2021 22:06:25 GMT  
		Size: 20.7 MB (20733420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806e9836f556f43332540c90936bf1e6812bc8a816ed3e8303d24274160315a6`  
		Last Modified: Wed, 17 Nov 2021 22:06:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f025c68191e2d7bfb99dff9d80fb197ff374bbf772cd136ee4832dd436b780`  
		Last Modified: Thu, 18 Nov 2021 15:00:38 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79f6e6e365c03808596b46ce13a82e2b8c1a3da95624931f5f59a224f9549bd`  
		Last Modified: Thu, 18 Nov 2021 15:02:44 GMT  
		Size: 77.0 MB (76964470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f135efb34ece029671809b7ae80150aadf8c3724cdba0588b8ff87ef1224227`  
		Last Modified: Thu, 18 Nov 2021 15:01:51 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38867eecb4ec440cc48a550e529430f90e0b4745f94919936a931fc0041bff66`  
		Last Modified: Thu, 18 Nov 2021 15:01:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc099e4e9f75f835a1f0339860fc8b8533fde96cedc8fcfe0ca7219cecdc6a85`  
		Last Modified: Thu, 18 Nov 2021 15:01:54 GMT  
		Size: 2.5 MB (2542551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ebb46e18b26d98e8e2d94140210db1fa8c838198c5d4202c34fa2fdea09b85`  
		Last Modified: Thu, 18 Nov 2021 15:02:22 GMT  
		Size: 59.3 MB (59270748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada58c23bd32d4b5b9e6f99ba3b97683da5c8a87530d4d3de76a05d666f9ee93`  
		Last Modified: Thu, 18 Nov 2021 15:01:51 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm variant v7

```console
$ docker pull redmine@sha256:3892174962d8c670eb7c63e24b336313b7ad97a3d979b796fea3d3e5269a0caa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188085945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559ede31734de6478903de58f430ef69899169b2bc9f743524da3d28c8537f03`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 08:17:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:17:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 18 Nov 2021 08:17:06 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 09:11:05 GMT
ENV RUBY_MAJOR=2.6
# Thu, 18 Nov 2021 09:11:06 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 18 Nov 2021 09:11:06 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 18 Nov 2021 09:15:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 18 Nov 2021 09:15:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Nov 2021 09:15:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Nov 2021 09:15:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 09:15:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 18 Nov 2021 09:15:18 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:06:17 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:14:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:14:07 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:14:08 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:14:08 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:14:10 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:14:10 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 20:14:10 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 20:14:16 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:19:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:19:49 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:19:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:19:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:19:50 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:19:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8e57706e11dcf2202a1ed28d022f7fe3daa306f06bf5311fee3d20b17f772`  
		Last Modified: Thu, 18 Nov 2021 09:24:19 GMT  
		Size: 9.9 MB (9872912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad345207fbbb28e02d7546fe9ec9b203219b39a7b6fe1a2c55d63e665ce8dd`  
		Last Modified: Thu, 18 Nov 2021 09:24:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb93faf1d4d1280ed90b904594838922fe363b19f403a1b9f79ea35b777e723`  
		Last Modified: Thu, 18 Nov 2021 09:31:29 GMT  
		Size: 20.6 MB (20643872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0931e5d4868154d483cf1176a216b4308c09ff1d5974bdf06aa52e79249b1b`  
		Last Modified: Thu, 18 Nov 2021 09:31:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34924d8de6aa6fc15f014748545368c4050bd41e82c42881addaad1d6ce5af1d`  
		Last Modified: Thu, 18 Nov 2021 20:22:03 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc4ee82c0134f6182306ab3d2f61de004598566e8d2a2768eb1e63d13c644a4`  
		Last Modified: Thu, 18 Nov 2021 20:23:59 GMT  
		Size: 73.3 MB (73264189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402e8559ef48139698794afc8023a202e2be4f9ac51a5b080cfc047db5b22024`  
		Last Modified: Thu, 18 Nov 2021 20:23:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d6fa89d913df5345fdd72246f21f872dd586f3dea82b74a8e2af86802d5f3`  
		Last Modified: Thu, 18 Nov 2021 20:23:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13913cd63e2f8a5e762bb5e11365d6eb6c9686742557fa3d1686db455b28d67e`  
		Last Modified: Thu, 18 Nov 2021 20:23:15 GMT  
		Size: 2.5 MB (2542552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7570cde0c2f33b880c2785dcc331643dcef309d8d11c405d588bbd8fa16d995e`  
		Last Modified: Thu, 18 Nov 2021 20:23:39 GMT  
		Size: 59.0 MB (59003825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a9987538c74ac886de99b4739802fd6543f23305c5c5e3ac0404f46c5b410a`  
		Last Modified: Thu, 18 Nov 2021 20:23:11 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:e1640a145bf5840bf0b9e2ab84e9d93a0d24a18ed393b43f6be7a2f7b18fce0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200438417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd7ec9b45c45b3a02a7ee54c69afa603f673991915570396bea1f1457a0e750`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:46:01 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:46:02 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:46:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:48:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:48:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:48:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:48:06 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:49:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:53:13 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:53:14 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:53:15 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:53:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:53:17 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 17 Nov 2021 19:53:18 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 17 Nov 2021 19:53:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:55:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:55:45 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:55:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:55:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:55:47 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:55:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16912dae180f72843a7e6b7dd25071e1090943354879adab903dcd984c8cee67`  
		Last Modified: Wed, 17 Nov 2021 09:54:26 GMT  
		Size: 21.1 MB (21095263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b73b9ee9aa5f816c4fb7665c7e19fe1663007ac1aacb74064aac56ece594983`  
		Last Modified: Wed, 17 Nov 2021 09:54:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb50985615235593da91e201ffe4b1db40feab50ab0a12b02a4c99191da4dfd`  
		Last Modified: Wed, 17 Nov 2021 19:57:02 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde74bffacc846943dfa6d226151f2242bb938be3ad44c6dcdd0dae1d33a42b3`  
		Last Modified: Wed, 17 Nov 2021 19:57:42 GMT  
		Size: 79.8 MB (79758991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279493fe0772df535c0878e63b1b64fba2b226e69a69fe151989981e2e059753`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b03979292e18cc4dce62c30e68343071ed1073cddd16a31506b6a78a29155`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd290e4917e62816eb06bb5841ee9c059f8d44144cff4fa97a200732d285904`  
		Last Modified: Wed, 17 Nov 2021 19:57:29 GMT  
		Size: 2.5 MB (2543981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fdce25f1a772528d0357b38e56069cd549aa907ba49f53e6cbac362540eeef`  
		Last Modified: Wed, 17 Nov 2021 19:57:37 GMT  
		Size: 59.9 MB (59851226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0e7224f51928ab8db5b08f76b818cc36d597e64ea832546f26380efc40f02`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; 386

```console
$ docker pull redmine@sha256:f1fe73108e092e98101c8561db5f30df576481a8663f6260f48c5d493362fc1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210347648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2a96bb39dd0f782181d9ca3c863004466bb821cd3f4eacfd701fa18b69ab5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 19:11:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:11:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:11:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:12:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:12:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:12:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:37:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:40:06 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:40:06 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:40:06 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:40:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:40:08 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 00:40:08 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 00:40:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:42:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:42:32 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:42:33 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:42:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:42:33 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:42:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e5a4df5a8f121515c23ab2e470f17d64c6bb138b6c22dda592fcde5393ca4`  
		Last Modified: Wed, 17 Nov 2021 19:20:39 GMT  
		Size: 20.9 MB (20910059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955765ea073687d915724497fa422005e56011fcf7d74483d30fd502a0ae1992`  
		Last Modified: Wed, 17 Nov 2021 19:20:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114a479d47bf9ce3b07ffb880a448300b978f0dd2fb9b2cf257248dd29de5e84`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7da47a96d23e66f0e9def04a7192dde8c3f9cd839282fda3efd121d97eda435`  
		Last Modified: Thu, 18 Nov 2021 00:45:17 GMT  
		Size: 82.6 MB (82599710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1928f566c831a396b46d1da2e213d7e2a8e77a2d900040af95c718d58cba7f60`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a6707cbab4ac55df2d2037e249005c67725357318531f7673e1887b17fb300`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d499e312e0f51e9de1e154f0944c20e8865d7114738e8b3ad6a65b07e1ce555`  
		Last Modified: Thu, 18 Nov 2021 00:44:49 GMT  
		Size: 2.5 MB (2542545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c34f6b79c0664ea6304fa45c671cc8239eba56a967c5c3f474672d335c96b7a`  
		Last Modified: Thu, 18 Nov 2021 00:45:03 GMT  
		Size: 59.3 MB (59259521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d6247c6cc7f7721a644ff15bf4633ab39ca26e5094d60356b696840bda35ec`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; ppc64le

```console
$ docker pull redmine@sha256:b446701d2307fa9b801d61f8206873f3183be2b01e06853ffd034006bd966006
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216483156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcce807ab1ab2e64ca24a050b61499ff5cf8d4e2b1932817b53042442b7b8ac7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 03:30:22 GMT
ADD file:c0f8b5d4d419bef7a494df5330ecf7bbea3cbb6462308ca0b2f26771f125dea0 in / 
# Wed, 17 Nov 2021 03:30:29 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:17:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 13:17:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 14:18:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 14:18:21 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 14:18:23 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 14:24:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 14:24:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 14:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 14:24:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 14:25:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 14:25:02 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 12:34:28 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 12:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 12:43:38 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 12:43:40 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 12:43:42 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 12:43:49 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 12:43:55 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 12:43:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 12:44:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 12:53:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 12:53:06 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 12:53:07 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 12:53:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 12:53:17 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 12:53:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:459de0a111d5c931674a5150ef4ae6bb1ffb1685380f4aafdba04a37d556c5de`  
		Last Modified: Wed, 17 Nov 2021 03:58:14 GMT  
		Size: 30.6 MB (30562278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4a8cb8add512175dbaeb682e1d37722eb039847e94d43b2c548f6bf9f4566`  
		Last Modified: Wed, 17 Nov 2021 14:30:35 GMT  
		Size: 12.7 MB (12705482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02accf8c69e0fb54236daa23b1409d80e215845f8d744672e8be1de6353c73f4`  
		Last Modified: Wed, 17 Nov 2021 14:30:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecde72085a62fc055b92d08be845488e745acea10ff923c9db7192bc696536f9`  
		Last Modified: Wed, 17 Nov 2021 14:35:36 GMT  
		Size: 22.0 MB (21985050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528aeb277a5e499d35f24f6a6cf6b7ff6d8081b0d8d6aebe5fd6ed9e1acc2ae9`  
		Last Modified: Wed, 17 Nov 2021 14:35:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ab84cc7e1bfe4aea4203f0b208c6c68525b8099d34b3e9e7e10bb8922f336a`  
		Last Modified: Thu, 18 Nov 2021 12:54:36 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0191378aec640fb5d45d1de897c833ad65b9e806c4af4f20e534124da8f1b86e`  
		Last Modified: Thu, 18 Nov 2021 12:55:27 GMT  
		Size: 87.9 MB (87901018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cfeff0c8b235322f39566325d86df1fe6f723088960f429453a4abc4138d97`  
		Last Modified: Thu, 18 Nov 2021 12:55:07 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454afba45a45e9f0cfbd2d2b89236c77f36c837f11c36a1faac55d9514614cb`  
		Last Modified: Thu, 18 Nov 2021 12:55:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed5955455cb71b05d5b8425970058f231ce442a8205d62fc14e3151c2622212`  
		Last Modified: Thu, 18 Nov 2021 12:55:08 GMT  
		Size: 2.5 MB (2542551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2617a080f5d29543f0081e6a79d31e3569e8ea84431aa0bf1bf5266439ecc995`  
		Last Modified: Thu, 18 Nov 2021 12:55:16 GMT  
		Size: 60.8 MB (60782532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291a484d21b345ee6c7321e4934daf23f05d31e40713d7d37df2e302d983fe9`  
		Last Modified: Thu, 18 Nov 2021 12:55:07 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0` - linux; s390x

```console
$ docker pull redmine@sha256:7a08ebb93b3b03597bf02476a2515778130f7bff1e3c33e8fcc00a1073ccfc31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200291030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9aaeccdc23c9bbd5bb63a74995e35e24d80ec599e61878f1a15ad2fa1e82ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:42:37 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:44:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:44:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:44:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:44:07 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:34:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:36:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:37:01 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:37:01 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:37:01 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:37:02 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:37:02 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 17 Nov 2021 20:37:02 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 17 Nov 2021 20:37:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:38:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:38:46 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:38:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:38:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:38:46 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:38:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdaf56dd9686cdaca63c3c8ebab2d6841412a36159619d65853daa75500716`  
		Last Modified: Wed, 17 Nov 2021 09:51:17 GMT  
		Size: 21.6 MB (21619852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80433d0a1bacd8eb06bb301d366ea459dbae5ce9a2bea94372bd52e0939584a0`  
		Last Modified: Wed, 17 Nov 2021 09:51:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e82306e7113526e6aa75620a186091a8a2139c7e63336bc2033df0329cda36e`  
		Last Modified: Wed, 17 Nov 2021 20:39:48 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085d5f5c7261748f638b0c30c5922b96cc7a7139c94d116b31323b1fe50f715c`  
		Last Modified: Wed, 17 Nov 2021 20:40:19 GMT  
		Size: 78.9 MB (78941825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdafcf9171e45387b8e26650c032636412a64ea71a82beb8da9aaadda5a038a`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd65e98466ef8280e1eac2c5693840a60cd00682e5bbdafe9bde2b47edd7275`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48155420ae67e64e5329514da95aeea977ad3762dff4bc8baacdb80a3058`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 2.5 MB (2542547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56cd02bb76bc97344bf358dd1335582e1460a561ab33d1c8dab2a5c27c2f66e`  
		Last Modified: Wed, 17 Nov 2021 20:40:14 GMT  
		Size: 60.6 MB (60598255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05981b15aac91be53d29f32192b2ad7af008afe472c8d7aab11db0049c3de996`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0-alpine`

```console
$ docker pull redmine@sha256:fa8ba213e2dfef7bfb98c3b2ca6af9917a9c0b9b15be67bb8c20499ac3d04aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:01887efbc27065bcc544e6ba80201b994e89e27280c7b25de2c280d6f1b33024
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153558063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abb35ae9e45f8c5510f9bfe3efa808d3e893645c29b1b6aa08bae910bf2aa9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_MAJOR=2.6
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_VERSION=2.6.8
# Sat, 13 Nov 2021 06:51:31 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Sat, 13 Nov 2021 06:54:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:54:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:54:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:54:46 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:31:40 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:34:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Sat, 13 Nov 2021 14:34:29 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:34:29 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:34:29 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:34:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:34:30 GMT
ENV REDMINE_VERSION=4.0.9
# Sat, 13 Nov 2021 14:34:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Sat, 13 Nov 2021 14:34:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:34:34 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:36:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:36:07 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:36:07 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:36:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:36:07 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:36:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fd76747f3be3e4f4af1119b668fd5a9fa53725f84b429575cfb26c0d5f842a`  
		Last Modified: Sat, 13 Nov 2021 06:59:00 GMT  
		Size: 19.5 MB (19500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bbfb1229cd3c27d4dd990a0daf591e427afbc679b854303415a9e9a01ff10b`  
		Last Modified: Sat, 13 Nov 2021 06:58:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c267c2d73515a2e4fbaac349e5a31212348b7d72b21f80611dac1923c5c68666`  
		Last Modified: Sat, 13 Nov 2021 14:37:15 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7ea963f3d5877eea0043f8a2b75f17680ff5a4d362c1a4fce8c8a67c347239`  
		Last Modified: Sat, 13 Nov 2021 14:37:49 GMT  
		Size: 66.2 MB (66199469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05071f335bb9135d55d21c80aaa3523ae388d93f1a98136404e7c91fa99fb524`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a43db45233bb37a8a7df21efee11df06d119f141dd51e3c8672893a9bb6a654`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb71bc10f9decb3a165b48fa2dae4aa79929b41c812f261a1ff1fee173510e8`  
		Last Modified: Sat, 13 Nov 2021 14:37:38 GMT  
		Size: 2.5 MB (2543762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d38dd936d4bdfa095bb3270305cfe38c97043649fdf48ba25879b221ebbb40`  
		Last Modified: Sat, 13 Nov 2021 14:37:43 GMT  
		Size: 58.9 MB (58906080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ac236fd681e485d4f3495d7195078b72db1997782784f2aca237835c80c236`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0-passenger`

```console
$ docker pull redmine@sha256:d073e1e52d8fd056dca090670da100e0ec5755423e5c2181acf8e398f40b19ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:ed9ff685a3edef9e57bba8a46f67373f932d91a3800ad1980fc084a581e30695
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231459866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a0eaa63f11c5f69ff852f3d50ff83f5bdd0c84d275e14b03fd570c4dac9fb4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 23:47:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:47:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:47:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:47:17 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:32:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:34:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:34:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:34:43 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:34:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:34:43 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 20:34:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 20:34:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:36:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:36:48 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:36:48 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:36:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:36:49 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:36:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 18 Nov 2021 20:36:55 GMT
ENV PASSENGER_VERSION=6.0.12
# Thu, 18 Nov 2021 20:37:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:37:14 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 18 Nov 2021 20:37:14 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 18 Nov 2021 20:37:14 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0513aa66c0fb3e8b2ca883a3e8d1981bbfe8bfb788a9a888b723787293986e7d`  
		Last Modified: Wed, 17 Nov 2021 23:53:54 GMT  
		Size: 21.5 MB (21467890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dcedae4b9e16af3b588b2e085edcdc9b5895d6dcbd0f3c7886780233e285c2`  
		Last Modified: Wed, 17 Nov 2021 23:53:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31fda4ca0ea33330c7d7c55c465fd2b24a8bd41e15481cc208eddeb93c3aa72`  
		Last Modified: Thu, 18 Nov 2021 20:38:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9647538f90e6d8079158a334291526054be9f9baa1d00e0b4828a9363e3f92`  
		Last Modified: Thu, 18 Nov 2021 20:39:39 GMT  
		Size: 81.2 MB (81200246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8972d6130a8fe50a34eb323dcffca6ccfc098d985f074e08e3badf25890af0`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56991c7d2e73b3615e48d4b75afc4bc168af36045ebe4c66eb1034d29ca75996`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0ebf9fce3a7b8a16c7566fa9ed1edbeab1d2ba828b7b322c5da4418501d569`  
		Last Modified: Thu, 18 Nov 2021 20:39:24 GMT  
		Size: 2.5 MB (2542545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c91fe34b38ffbb891de3fffb08ad12983ba88aa7f48ab4d74b3ad502aeb49a`  
		Last Modified: Thu, 18 Nov 2021 20:39:33 GMT  
		Size: 60.2 MB (60161990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd17ac1130132640ad42caac391d9ac3edf34cf6031e72afd6d506f5c8d982b`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4b672afddef690c56715f4abd7042b78fb22e586fb62ec2d47012b70df4f63`  
		Last Modified: Thu, 18 Nov 2021 20:39:53 GMT  
		Size: 21.4 MB (21439477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffd89f64397f98d8225a7299e4d4c2174922d07733d60f1aebeb4e2ec448a75`  
		Last Modified: Thu, 18 Nov 2021 20:39:50 GMT  
		Size: 4.9 MB (4924654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.9`

```console
$ docker pull redmine@sha256:4d822d5d019f1969c1f0e218654d660c61828080868166d0b37353d2507a30f0
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
$ docker pull redmine@sha256:c44c0548e533e54f10782bb4cb14b7edc63926122edaba5cdc13fb8a11929196
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205095735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0153b08dec0342bdeb4960f121672a3a03e912a9a521a71e68cd20a3261b578d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 23:47:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:47:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:47:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:47:17 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:32:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:34:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:34:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:34:43 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:34:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:34:43 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 20:34:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 20:34:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:36:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:36:48 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:36:48 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:36:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:36:49 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:36:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0513aa66c0fb3e8b2ca883a3e8d1981bbfe8bfb788a9a888b723787293986e7d`  
		Last Modified: Wed, 17 Nov 2021 23:53:54 GMT  
		Size: 21.5 MB (21467890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dcedae4b9e16af3b588b2e085edcdc9b5895d6dcbd0f3c7886780233e285c2`  
		Last Modified: Wed, 17 Nov 2021 23:53:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31fda4ca0ea33330c7d7c55c465fd2b24a8bd41e15481cc208eddeb93c3aa72`  
		Last Modified: Thu, 18 Nov 2021 20:38:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9647538f90e6d8079158a334291526054be9f9baa1d00e0b4828a9363e3f92`  
		Last Modified: Thu, 18 Nov 2021 20:39:39 GMT  
		Size: 81.2 MB (81200246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8972d6130a8fe50a34eb323dcffca6ccfc098d985f074e08e3badf25890af0`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56991c7d2e73b3615e48d4b75afc4bc168af36045ebe4c66eb1034d29ca75996`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0ebf9fce3a7b8a16c7566fa9ed1edbeab1d2ba828b7b322c5da4418501d569`  
		Last Modified: Thu, 18 Nov 2021 20:39:24 GMT  
		Size: 2.5 MB (2542545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c91fe34b38ffbb891de3fffb08ad12983ba88aa7f48ab4d74b3ad502aeb49a`  
		Last Modified: Thu, 18 Nov 2021 20:39:33 GMT  
		Size: 60.2 MB (60161990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd17ac1130132640ad42caac391d9ac3edf34cf6031e72afd6d506f5c8d982b`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; arm variant v5

```console
$ docker pull redmine@sha256:626796677c39ac694e716bb310af5cd0fc5bda937047b59ce65ef6fe80663ee4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194751147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00afec53b5b1461458224d8ca8f6a7c3d13c017d9257ede01d0ba8c05997da8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 20:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:53:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 20:53:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:48:32 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 21:48:33 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 21:48:33 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 21:52:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 21:52:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 21:53:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 21:53:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:53:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 21:53:02 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 14:44:02 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 14:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 14:52:14 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 14:52:14 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 14:52:15 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 14:52:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 14:52:17 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 14:52:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 14:52:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 14:58:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 14:58:16 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 14:58:16 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 14:58:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 14:58:17 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 14:58:18 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58fbebb8e6e22b1601002ddb4252e30c3750edfb93b87424f6c1a971c665bf`  
		Last Modified: Wed, 17 Nov 2021 21:59:40 GMT  
		Size: 10.3 MB (10349405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484eb5c97eceafe50be8deba254566cb365fd68cb0baa2e5418ecece614c2728`  
		Last Modified: Wed, 17 Nov 2021 21:59:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036dbb00becdfbc8994f79e0968b90235a36a6cd3adc53d1b0c485d366b86b8e`  
		Last Modified: Wed, 17 Nov 2021 22:06:25 GMT  
		Size: 20.7 MB (20733420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806e9836f556f43332540c90936bf1e6812bc8a816ed3e8303d24274160315a6`  
		Last Modified: Wed, 17 Nov 2021 22:06:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f025c68191e2d7bfb99dff9d80fb197ff374bbf772cd136ee4832dd436b780`  
		Last Modified: Thu, 18 Nov 2021 15:00:38 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79f6e6e365c03808596b46ce13a82e2b8c1a3da95624931f5f59a224f9549bd`  
		Last Modified: Thu, 18 Nov 2021 15:02:44 GMT  
		Size: 77.0 MB (76964470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f135efb34ece029671809b7ae80150aadf8c3724cdba0588b8ff87ef1224227`  
		Last Modified: Thu, 18 Nov 2021 15:01:51 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38867eecb4ec440cc48a550e529430f90e0b4745f94919936a931fc0041bff66`  
		Last Modified: Thu, 18 Nov 2021 15:01:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc099e4e9f75f835a1f0339860fc8b8533fde96cedc8fcfe0ca7219cecdc6a85`  
		Last Modified: Thu, 18 Nov 2021 15:01:54 GMT  
		Size: 2.5 MB (2542551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ebb46e18b26d98e8e2d94140210db1fa8c838198c5d4202c34fa2fdea09b85`  
		Last Modified: Thu, 18 Nov 2021 15:02:22 GMT  
		Size: 59.3 MB (59270748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada58c23bd32d4b5b9e6f99ba3b97683da5c8a87530d4d3de76a05d666f9ee93`  
		Last Modified: Thu, 18 Nov 2021 15:01:51 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; arm variant v7

```console
$ docker pull redmine@sha256:3892174962d8c670eb7c63e24b336313b7ad97a3d979b796fea3d3e5269a0caa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188085945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559ede31734de6478903de58f430ef69899169b2bc9f743524da3d28c8537f03`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 08:17:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:17:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 18 Nov 2021 08:17:06 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 09:11:05 GMT
ENV RUBY_MAJOR=2.6
# Thu, 18 Nov 2021 09:11:06 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 18 Nov 2021 09:11:06 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 18 Nov 2021 09:15:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 18 Nov 2021 09:15:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Nov 2021 09:15:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Nov 2021 09:15:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 09:15:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 18 Nov 2021 09:15:18 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:06:17 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:14:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:14:07 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:14:08 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:14:08 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:14:10 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:14:10 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 20:14:10 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 20:14:16 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:19:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:19:49 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:19:49 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:19:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:19:50 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:19:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8e57706e11dcf2202a1ed28d022f7fe3daa306f06bf5311fee3d20b17f772`  
		Last Modified: Thu, 18 Nov 2021 09:24:19 GMT  
		Size: 9.9 MB (9872912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad345207fbbb28e02d7546fe9ec9b203219b39a7b6fe1a2c55d63e665ce8dd`  
		Last Modified: Thu, 18 Nov 2021 09:24:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb93faf1d4d1280ed90b904594838922fe363b19f403a1b9f79ea35b777e723`  
		Last Modified: Thu, 18 Nov 2021 09:31:29 GMT  
		Size: 20.6 MB (20643872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0931e5d4868154d483cf1176a216b4308c09ff1d5974bdf06aa52e79249b1b`  
		Last Modified: Thu, 18 Nov 2021 09:31:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34924d8de6aa6fc15f014748545368c4050bd41e82c42881addaad1d6ce5af1d`  
		Last Modified: Thu, 18 Nov 2021 20:22:03 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc4ee82c0134f6182306ab3d2f61de004598566e8d2a2768eb1e63d13c644a4`  
		Last Modified: Thu, 18 Nov 2021 20:23:59 GMT  
		Size: 73.3 MB (73264189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402e8559ef48139698794afc8023a202e2be4f9ac51a5b080cfc047db5b22024`  
		Last Modified: Thu, 18 Nov 2021 20:23:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d6fa89d913df5345fdd72246f21f872dd586f3dea82b74a8e2af86802d5f3`  
		Last Modified: Thu, 18 Nov 2021 20:23:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13913cd63e2f8a5e762bb5e11365d6eb6c9686742557fa3d1686db455b28d67e`  
		Last Modified: Thu, 18 Nov 2021 20:23:15 GMT  
		Size: 2.5 MB (2542552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7570cde0c2f33b880c2785dcc331643dcef309d8d11c405d588bbd8fa16d995e`  
		Last Modified: Thu, 18 Nov 2021 20:23:39 GMT  
		Size: 59.0 MB (59003825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a9987538c74ac886de99b4739802fd6543f23305c5c5e3ac0404f46c5b410a`  
		Last Modified: Thu, 18 Nov 2021 20:23:11 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:e1640a145bf5840bf0b9e2ab84e9d93a0d24a18ed393b43f6be7a2f7b18fce0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200438417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd7ec9b45c45b3a02a7ee54c69afa603f673991915570396bea1f1457a0e750`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:46:01 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:46:02 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:46:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:48:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:48:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:48:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:48:06 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:49:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:53:13 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:53:14 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:53:15 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:53:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:53:17 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 17 Nov 2021 19:53:18 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 17 Nov 2021 19:53:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:55:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:55:45 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:55:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:55:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:55:47 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:55:48 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16912dae180f72843a7e6b7dd25071e1090943354879adab903dcd984c8cee67`  
		Last Modified: Wed, 17 Nov 2021 09:54:26 GMT  
		Size: 21.1 MB (21095263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b73b9ee9aa5f816c4fb7665c7e19fe1663007ac1aacb74064aac56ece594983`  
		Last Modified: Wed, 17 Nov 2021 09:54:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb50985615235593da91e201ffe4b1db40feab50ab0a12b02a4c99191da4dfd`  
		Last Modified: Wed, 17 Nov 2021 19:57:02 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde74bffacc846943dfa6d226151f2242bb938be3ad44c6dcdd0dae1d33a42b3`  
		Last Modified: Wed, 17 Nov 2021 19:57:42 GMT  
		Size: 79.8 MB (79758991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279493fe0772df535c0878e63b1b64fba2b226e69a69fe151989981e2e059753`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55b03979292e18cc4dce62c30e68343071ed1073cddd16a31506b6a78a29155`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd290e4917e62816eb06bb5841ee9c059f8d44144cff4fa97a200732d285904`  
		Last Modified: Wed, 17 Nov 2021 19:57:29 GMT  
		Size: 2.5 MB (2543981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fdce25f1a772528d0357b38e56069cd549aa907ba49f53e6cbac362540eeef`  
		Last Modified: Wed, 17 Nov 2021 19:57:37 GMT  
		Size: 59.9 MB (59851226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0e7224f51928ab8db5b08f76b818cc36d597e64ea832546f26380efc40f02`  
		Last Modified: Wed, 17 Nov 2021 19:57:28 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; 386

```console
$ docker pull redmine@sha256:f1fe73108e092e98101c8561db5f30df576481a8663f6260f48c5d493362fc1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210347648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2a96bb39dd0f782181d9ca3c863004466bb821cd3f4eacfd701fa18b69ab5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 19:11:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:11:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:11:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:12:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:12:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:12:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:37:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:40:06 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:40:06 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:40:06 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:40:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:40:08 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 00:40:08 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 00:40:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:42:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:42:32 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:42:33 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:42:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:42:33 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:42:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e5a4df5a8f121515c23ab2e470f17d64c6bb138b6c22dda592fcde5393ca4`  
		Last Modified: Wed, 17 Nov 2021 19:20:39 GMT  
		Size: 20.9 MB (20910059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955765ea073687d915724497fa422005e56011fcf7d74483d30fd502a0ae1992`  
		Last Modified: Wed, 17 Nov 2021 19:20:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114a479d47bf9ce3b07ffb880a448300b978f0dd2fb9b2cf257248dd29de5e84`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7da47a96d23e66f0e9def04a7192dde8c3f9cd839282fda3efd121d97eda435`  
		Last Modified: Thu, 18 Nov 2021 00:45:17 GMT  
		Size: 82.6 MB (82599710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1928f566c831a396b46d1da2e213d7e2a8e77a2d900040af95c718d58cba7f60`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a6707cbab4ac55df2d2037e249005c67725357318531f7673e1887b17fb300`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d499e312e0f51e9de1e154f0944c20e8865d7114738e8b3ad6a65b07e1ce555`  
		Last Modified: Thu, 18 Nov 2021 00:44:49 GMT  
		Size: 2.5 MB (2542545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c34f6b79c0664ea6304fa45c671cc8239eba56a967c5c3f474672d335c96b7a`  
		Last Modified: Thu, 18 Nov 2021 00:45:03 GMT  
		Size: 59.3 MB (59259521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d6247c6cc7f7721a644ff15bf4633ab39ca26e5094d60356b696840bda35ec`  
		Last Modified: Thu, 18 Nov 2021 00:44:47 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; ppc64le

```console
$ docker pull redmine@sha256:b446701d2307fa9b801d61f8206873f3183be2b01e06853ffd034006bd966006
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216483156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcce807ab1ab2e64ca24a050b61499ff5cf8d4e2b1932817b53042442b7b8ac7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 03:30:22 GMT
ADD file:c0f8b5d4d419bef7a494df5330ecf7bbea3cbb6462308ca0b2f26771f125dea0 in / 
# Wed, 17 Nov 2021 03:30:29 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:17:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 13:17:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 14:18:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 14:18:21 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 14:18:23 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 14:24:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 14:24:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 14:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 14:24:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 14:25:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 14:25:02 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 12:34:28 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 12:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 12:43:38 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 12:43:40 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 12:43:42 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 12:43:49 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 12:43:55 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 12:43:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 12:44:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 12:53:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 12:53:06 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 12:53:07 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 12:53:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 12:53:17 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 12:53:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:459de0a111d5c931674a5150ef4ae6bb1ffb1685380f4aafdba04a37d556c5de`  
		Last Modified: Wed, 17 Nov 2021 03:58:14 GMT  
		Size: 30.6 MB (30562278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4a8cb8add512175dbaeb682e1d37722eb039847e94d43b2c548f6bf9f4566`  
		Last Modified: Wed, 17 Nov 2021 14:30:35 GMT  
		Size: 12.7 MB (12705482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02accf8c69e0fb54236daa23b1409d80e215845f8d744672e8be1de6353c73f4`  
		Last Modified: Wed, 17 Nov 2021 14:30:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecde72085a62fc055b92d08be845488e745acea10ff923c9db7192bc696536f9`  
		Last Modified: Wed, 17 Nov 2021 14:35:36 GMT  
		Size: 22.0 MB (21985050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528aeb277a5e499d35f24f6a6cf6b7ff6d8081b0d8d6aebe5fd6ed9e1acc2ae9`  
		Last Modified: Wed, 17 Nov 2021 14:35:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ab84cc7e1bfe4aea4203f0b208c6c68525b8099d34b3e9e7e10bb8922f336a`  
		Last Modified: Thu, 18 Nov 2021 12:54:36 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0191378aec640fb5d45d1de897c833ad65b9e806c4af4f20e534124da8f1b86e`  
		Last Modified: Thu, 18 Nov 2021 12:55:27 GMT  
		Size: 87.9 MB (87901018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cfeff0c8b235322f39566325d86df1fe6f723088960f429453a4abc4138d97`  
		Last Modified: Thu, 18 Nov 2021 12:55:07 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d454afba45a45e9f0cfbd2d2b89236c77f36c837f11c36a1faac55d9514614cb`  
		Last Modified: Thu, 18 Nov 2021 12:55:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed5955455cb71b05d5b8425970058f231ce442a8205d62fc14e3151c2622212`  
		Last Modified: Thu, 18 Nov 2021 12:55:08 GMT  
		Size: 2.5 MB (2542551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2617a080f5d29543f0081e6a79d31e3569e8ea84431aa0bf1bf5266439ecc995`  
		Last Modified: Thu, 18 Nov 2021 12:55:16 GMT  
		Size: 60.8 MB (60782532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0291a484d21b345ee6c7321e4934daf23f05d31e40713d7d37df2e302d983fe9`  
		Last Modified: Thu, 18 Nov 2021 12:55:07 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.0.9` - linux; s390x

```console
$ docker pull redmine@sha256:7a08ebb93b3b03597bf02476a2515778130f7bff1e3c33e8fcc00a1073ccfc31
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200291030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9aaeccdc23c9bbd5bb63a74995e35e24d80ec599e61878f1a15ad2fa1e82ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:42:37 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:44:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:44:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:44:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:44:07 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:34:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:36:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:37:01 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:37:01 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:37:01 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:37:02 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:37:02 GMT
ENV REDMINE_VERSION=4.0.9
# Wed, 17 Nov 2021 20:37:02 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Wed, 17 Nov 2021 20:37:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:38:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:38:46 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:38:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:38:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:38:46 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:38:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdaf56dd9686cdaca63c3c8ebab2d6841412a36159619d65853daa75500716`  
		Last Modified: Wed, 17 Nov 2021 09:51:17 GMT  
		Size: 21.6 MB (21619852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80433d0a1bacd8eb06bb301d366ea459dbae5ce9a2bea94372bd52e0939584a0`  
		Last Modified: Wed, 17 Nov 2021 09:51:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e82306e7113526e6aa75620a186091a8a2139c7e63336bc2033df0329cda36e`  
		Last Modified: Wed, 17 Nov 2021 20:39:48 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085d5f5c7261748f638b0c30c5922b96cc7a7139c94d116b31323b1fe50f715c`  
		Last Modified: Wed, 17 Nov 2021 20:40:19 GMT  
		Size: 78.9 MB (78941825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdafcf9171e45387b8e26650c032636412a64ea71a82beb8da9aaadda5a038a`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd65e98466ef8280e1eac2c5693840a60cd00682e5bbdafe9bde2b47edd7275`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48155420ae67e64e5329514da95aeea977ad3762dff4bc8baacdb80a3058`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 2.5 MB (2542547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56cd02bb76bc97344bf358dd1335582e1460a561ab33d1c8dab2a5c27c2f66e`  
		Last Modified: Wed, 17 Nov 2021 20:40:14 GMT  
		Size: 60.6 MB (60598255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05981b15aac91be53d29f32192b2ad7af008afe472c8d7aab11db0049c3de996`  
		Last Modified: Wed, 17 Nov 2021 20:40:08 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.9-alpine`

```console
$ docker pull redmine@sha256:fa8ba213e2dfef7bfb98c3b2ca6af9917a9c0b9b15be67bb8c20499ac3d04aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0.9-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:01887efbc27065bcc544e6ba80201b994e89e27280c7b25de2c280d6f1b33024
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153558063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abb35ae9e45f8c5510f9bfe3efa808d3e893645c29b1b6aa08bae910bf2aa9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_MAJOR=2.6
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_VERSION=2.6.8
# Sat, 13 Nov 2021 06:51:31 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Sat, 13 Nov 2021 06:54:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:54:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:54:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:54:46 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:31:40 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:34:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript-fonts 		imagemagick6 	;
# Sat, 13 Nov 2021 14:34:29 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:34:29 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:34:29 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:34:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:34:30 GMT
ENV REDMINE_VERSION=4.0.9
# Sat, 13 Nov 2021 14:34:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Sat, 13 Nov 2021 14:34:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:34:34 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:36:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 		imagemagick6-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:36:07 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:36:07 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:36:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:36:07 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:36:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fd76747f3be3e4f4af1119b668fd5a9fa53725f84b429575cfb26c0d5f842a`  
		Last Modified: Sat, 13 Nov 2021 06:59:00 GMT  
		Size: 19.5 MB (19500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bbfb1229cd3c27d4dd990a0daf591e427afbc679b854303415a9e9a01ff10b`  
		Last Modified: Sat, 13 Nov 2021 06:58:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c267c2d73515a2e4fbaac349e5a31212348b7d72b21f80611dac1923c5c68666`  
		Last Modified: Sat, 13 Nov 2021 14:37:15 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7ea963f3d5877eea0043f8a2b75f17680ff5a4d362c1a4fce8c8a67c347239`  
		Last Modified: Sat, 13 Nov 2021 14:37:49 GMT  
		Size: 66.2 MB (66199469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05071f335bb9135d55d21c80aaa3523ae388d93f1a98136404e7c91fa99fb524`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a43db45233bb37a8a7df21efee11df06d119f141dd51e3c8672893a9bb6a654`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb71bc10f9decb3a165b48fa2dae4aa79929b41c812f261a1ff1fee173510e8`  
		Last Modified: Sat, 13 Nov 2021 14:37:38 GMT  
		Size: 2.5 MB (2543762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d38dd936d4bdfa095bb3270305cfe38c97043649fdf48ba25879b221ebbb40`  
		Last Modified: Sat, 13 Nov 2021 14:37:43 GMT  
		Size: 58.9 MB (58906080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ac236fd681e485d4f3495d7195078b72db1997782784f2aca237835c80c236`  
		Last Modified: Sat, 13 Nov 2021 14:37:37 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.0.9-passenger`

```console
$ docker pull redmine@sha256:d073e1e52d8fd056dca090670da100e0ec5755423e5c2181acf8e398f40b19ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.0.9-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:ed9ff685a3edef9e57bba8a46f67373f932d91a3800ad1980fc084a581e30695
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231459866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a0eaa63f11c5f69ff852f3d50ff83f5bdd0c84d275e14b03fd570c4dac9fb4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 23:47:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:47:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:47:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:47:17 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:32:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				gsfonts 		imagemagick 		gosu 		tini 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:34:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:34:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:34:43 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:34:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:34:43 GMT
ENV REDMINE_VERSION=4.0.9
# Thu, 18 Nov 2021 20:34:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=04a772b0b8f8ce6493614a7cb22ed82cb9b43c75dcdbeb5c2f925bae98e0d5df
# Thu, 18 Nov 2021 20:34:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:36:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 		libmagickcore-dev libmagickwand-dev 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:36:48 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:36:48 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:36:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:36:49 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:36:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 18 Nov 2021 20:36:55 GMT
ENV PASSENGER_VERSION=6.0.12
# Thu, 18 Nov 2021 20:37:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:37:14 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 18 Nov 2021 20:37:14 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 18 Nov 2021 20:37:14 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0513aa66c0fb3e8b2ca883a3e8d1981bbfe8bfb788a9a888b723787293986e7d`  
		Last Modified: Wed, 17 Nov 2021 23:53:54 GMT  
		Size: 21.5 MB (21467890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dcedae4b9e16af3b588b2e085edcdc9b5895d6dcbd0f3c7886780233e285c2`  
		Last Modified: Wed, 17 Nov 2021 23:53:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31fda4ca0ea33330c7d7c55c465fd2b24a8bd41e15481cc208eddeb93c3aa72`  
		Last Modified: Thu, 18 Nov 2021 20:38:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9647538f90e6d8079158a334291526054be9f9baa1d00e0b4828a9363e3f92`  
		Last Modified: Thu, 18 Nov 2021 20:39:39 GMT  
		Size: 81.2 MB (81200246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8972d6130a8fe50a34eb323dcffca6ccfc098d985f074e08e3badf25890af0`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56991c7d2e73b3615e48d4b75afc4bc168af36045ebe4c66eb1034d29ca75996`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0ebf9fce3a7b8a16c7566fa9ed1edbeab1d2ba828b7b322c5da4418501d569`  
		Last Modified: Thu, 18 Nov 2021 20:39:24 GMT  
		Size: 2.5 MB (2542545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c91fe34b38ffbb891de3fffb08ad12983ba88aa7f48ab4d74b3ad502aeb49a`  
		Last Modified: Thu, 18 Nov 2021 20:39:33 GMT  
		Size: 60.2 MB (60161990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd17ac1130132640ad42caac391d9ac3edf34cf6031e72afd6d506f5c8d982b`  
		Last Modified: Thu, 18 Nov 2021 20:39:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4b672afddef690c56715f4abd7042b78fb22e586fb62ec2d47012b70df4f63`  
		Last Modified: Thu, 18 Nov 2021 20:39:53 GMT  
		Size: 21.4 MB (21439477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffd89f64397f98d8225a7299e4d4c2174922d07733d60f1aebeb4e2ec448a75`  
		Last Modified: Thu, 18 Nov 2021 20:39:50 GMT  
		Size: 4.9 MB (4924654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1`

```console
$ docker pull redmine@sha256:73d4140c6a63fdfd3aecd3995e1eab4a865089eb8745597b706c6c43ee3bc9f2
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
$ docker pull redmine@sha256:e64090cf4e8222741582e7ca5eeea4b11b2207e28d54cbd805ab79aa7e090a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205967320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d1171fd21f42b7973c030b65604a792fb7887cdd44eeaa0b9d877d2fba6a64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 23:47:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:47:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:47:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:47:17 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:32:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:32:57 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:32:57 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:32:58 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:32:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:32:59 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 20:32:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 20:33:03 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:33:44 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:33:44 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:33:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:33:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:33:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0513aa66c0fb3e8b2ca883a3e8d1981bbfe8bfb788a9a888b723787293986e7d`  
		Last Modified: Wed, 17 Nov 2021 23:53:54 GMT  
		Size: 21.5 MB (21467890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dcedae4b9e16af3b588b2e085edcdc9b5895d6dcbd0f3c7886780233e285c2`  
		Last Modified: Wed, 17 Nov 2021 23:53:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31fda4ca0ea33330c7d7c55c465fd2b24a8bd41e15481cc208eddeb93c3aa72`  
		Last Modified: Thu, 18 Nov 2021 20:38:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1094964e4a9a3498a54642ac2a0993b548287ab34427c8f3ad03217fb4e31df1`  
		Last Modified: Thu, 18 Nov 2021 20:38:58 GMT  
		Size: 94.1 MB (94086142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b39fdcb59e4fd92888f29e12fe787da7cbd3ae68f1b4cbe5a1f22a3503761f`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c0c4680fcc99ce7feec161178b633a6e149735dba692adcddd78a4d3f62e66`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe18ef703b3280b5a608d351b9967f0441103296f4ac67f5ffa8772492c42877`  
		Last Modified: Thu, 18 Nov 2021 20:38:41 GMT  
		Size: 2.7 MB (2749693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8beb40f499f277318dbeaeb906ac2767f6a116457f9e0e8bc9e31c5e34c8950`  
		Last Modified: Thu, 18 Nov 2021 20:38:46 GMT  
		Size: 47.9 MB (47940531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc66131f0ad46ada0132e9bd266dff4315cc7cdf0de54deba17ffe354d8954b`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm variant v5

```console
$ docker pull redmine@sha256:1c94633e8399caf4c132a211446786e5619f3aaf3ada17936c3fd61a4d5b8d75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (209987469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda7e6f28c2718c2fd381ac850bc956317f91deebb5e1b09c36b4c90aeaf63d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 20:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:53:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 20:53:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:48:32 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 21:48:33 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 21:48:33 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 21:52:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 21:52:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 21:53:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 21:53:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:53:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 21:53:02 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 14:44:02 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 14:45:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 14:45:12 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 14:45:13 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 14:45:13 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 14:45:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 14:45:15 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 14:45:16 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 14:45:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 14:50:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 14:50:50 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 14:50:51 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 14:50:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 14:50:52 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 14:50:52 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58fbebb8e6e22b1601002ddb4252e30c3750edfb93b87424f6c1a971c665bf`  
		Last Modified: Wed, 17 Nov 2021 21:59:40 GMT  
		Size: 10.3 MB (10349405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484eb5c97eceafe50be8deba254566cb365fd68cb0baa2e5418ecece614c2728`  
		Last Modified: Wed, 17 Nov 2021 21:59:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036dbb00becdfbc8994f79e0968b90235a36a6cd3adc53d1b0c485d366b86b8e`  
		Last Modified: Wed, 17 Nov 2021 22:06:25 GMT  
		Size: 20.7 MB (20733420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806e9836f556f43332540c90936bf1e6812bc8a816ed3e8303d24274160315a6`  
		Last Modified: Wed, 17 Nov 2021 22:06:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f025c68191e2d7bfb99dff9d80fb197ff374bbf772cd136ee4832dd436b780`  
		Last Modified: Thu, 18 Nov 2021 15:00:38 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e7e4e417ce998b2acf5a43d5e3d310e5d173f0350246f67d6a64d2eb65efd3`  
		Last Modified: Thu, 18 Nov 2021 15:01:38 GMT  
		Size: 89.6 MB (89577157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca15bf4b25fc8043840be160137dbf12973d10853056a17e105122ff7fb7488b`  
		Last Modified: Thu, 18 Nov 2021 15:00:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de134ee415ecb51b4b8f7f8245896598264f9a051bc523882011eadb9c808ddc`  
		Last Modified: Thu, 18 Nov 2021 15:00:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46654bccee7c4ee01c5b4e984f1138dc6d5021a27ee4f16d4c9563e27df207a2`  
		Last Modified: Thu, 18 Nov 2021 15:00:40 GMT  
		Size: 2.7 MB (2749688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08825881a785d1b44df9240ad1d4946af7d2f9f5514731680fc5b481bdf23b64`  
		Last Modified: Thu, 18 Nov 2021 15:01:05 GMT  
		Size: 61.7 MB (61687247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5eb3a1c5d65c75b6f9876aa32b8dacfbc3cfec3213dd1d9ecf44359de733040`  
		Last Modified: Thu, 18 Nov 2021 15:00:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm variant v7

```console
$ docker pull redmine@sha256:389987777a69d488dc09951bbed7578a3b4fa5fc31508b370cefeeff5dd5489e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203154542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7962ae32020d8125d72ff7386cb75d025459c2377ae72427084b34d3f625133b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 08:17:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:17:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 18 Nov 2021 08:17:06 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 09:11:05 GMT
ENV RUBY_MAJOR=2.6
# Thu, 18 Nov 2021 09:11:06 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 18 Nov 2021 09:11:06 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 18 Nov 2021 09:15:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 18 Nov 2021 09:15:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Nov 2021 09:15:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Nov 2021 09:15:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 09:15:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 18 Nov 2021 09:15:18 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:06:17 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:07:21 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:07:21 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:07:22 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:07:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:07:24 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 20:07:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 20:07:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:12:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:12:45 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:12:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:12:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:12:46 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:12:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8e57706e11dcf2202a1ed28d022f7fe3daa306f06bf5311fee3d20b17f772`  
		Last Modified: Thu, 18 Nov 2021 09:24:19 GMT  
		Size: 9.9 MB (9872912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad345207fbbb28e02d7546fe9ec9b203219b39a7b6fe1a2c55d63e665ce8dd`  
		Last Modified: Thu, 18 Nov 2021 09:24:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb93faf1d4d1280ed90b904594838922fe363b19f403a1b9f79ea35b777e723`  
		Last Modified: Thu, 18 Nov 2021 09:31:29 GMT  
		Size: 20.6 MB (20643872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0931e5d4868154d483cf1176a216b4308c09ff1d5974bdf06aa52e79249b1b`  
		Last Modified: Thu, 18 Nov 2021 09:31:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34924d8de6aa6fc15f014748545368c4050bd41e82c42881addaad1d6ce5af1d`  
		Last Modified: Thu, 18 Nov 2021 20:22:03 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe847a0cc5e49032edaabc4ad79b83561b131b1c8a64b36cc4035b34c45cd2bd`  
		Last Modified: Thu, 18 Nov 2021 20:22:58 GMT  
		Size: 85.6 MB (85589341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1271f98e88e2007683620d81d1d7ce1b142d0a611489db9590e907c2cf09d568`  
		Last Modified: Thu, 18 Nov 2021 20:22:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2774949041c54ccd1dc64156df7789cc9153f1bbffdaf1af8144f160f53c1f`  
		Last Modified: Thu, 18 Nov 2021 20:22:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b1a61dcb7c1a9b2700646db446500e50b5f2a99f9b3b23eb023f785c1b2986`  
		Last Modified: Thu, 18 Nov 2021 20:22:05 GMT  
		Size: 2.7 MB (2749688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46bdde1d4f5ccd620ae520c006f1ae9e16a531d474e1cb8357b26d4dc81ca85`  
		Last Modified: Thu, 18 Nov 2021 20:22:28 GMT  
		Size: 61.5 MB (61540135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a98df33a6bb62fe1a80d31d76b11984e941c4966a3b70ded2ca0c1a22d0fed3`  
		Last Modified: Thu, 18 Nov 2021 20:22:02 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b222b2102035ba87c72076afd3f971a910dd6cfa4627c0423b876748b40dea1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216401827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871b1f794b4d0fcb638c8a57721a72acc701c347e2e647a928da47a7dc1c8c9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:46:01 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:46:02 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:46:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:48:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:48:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:48:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:48:06 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:49:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:50:19 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:50:20 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:50:21 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:50:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:50:23 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 17 Nov 2021 19:50:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 17 Nov 2021 19:50:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:52:38 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:52:40 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:52:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:52:41 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:52:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16912dae180f72843a7e6b7dd25071e1090943354879adab903dcd984c8cee67`  
		Last Modified: Wed, 17 Nov 2021 09:54:26 GMT  
		Size: 21.1 MB (21095263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b73b9ee9aa5f816c4fb7665c7e19fe1663007ac1aacb74064aac56ece594983`  
		Last Modified: Wed, 17 Nov 2021 09:54:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb50985615235593da91e201ffe4b1db40feab50ab0a12b02a4c99191da4dfd`  
		Last Modified: Wed, 17 Nov 2021 19:57:02 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b972b42f387b463ec4f85b98ff1de46778da88cde8db5210abd6cdb28fcfe996`  
		Last Modified: Wed, 17 Nov 2021 19:57:16 GMT  
		Size: 92.6 MB (92615309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d5c078974fd14c58f0b3b7716527a89b7fd62214cbd050a80d385982968927`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302584afc613dd65a75b5bcda18ac7919a7c809a1df57148453b3f76954ed897`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d073b657b29ddf797af445ca3996a8594b19899f364b2cc3d189f86a3fcf0deb`  
		Last Modified: Wed, 17 Nov 2021 19:57:00 GMT  
		Size: 2.7 MB (2749627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca343679f96ad8123399df85aad69f3174b5d405b2d11bf4804a0840974e2710`  
		Last Modified: Wed, 17 Nov 2021 19:57:10 GMT  
		Size: 62.8 MB (62752672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1dcf76925b4813ce41dd25c0b93567defab250f8d74eac3e070f92b49c068`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; 386

```console
$ docker pull redmine@sha256:156a98e108ae32310750def5670b7f14ce4791c8fba4fc62b4389d126421ee10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212332382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b8c8954f2416156578d6b917f84622fb2feacefa48597e8b97e216b5700b97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 19:11:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:11:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:11:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:12:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:12:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:12:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:37:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:38:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:38:32 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:38:33 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:38:33 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:38:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:38:34 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 00:38:34 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 00:38:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:39:29 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:39:29 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:39:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:39:30 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:39:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e5a4df5a8f121515c23ab2e470f17d64c6bb138b6c22dda592fcde5393ca4`  
		Last Modified: Wed, 17 Nov 2021 19:20:39 GMT  
		Size: 20.9 MB (20910059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955765ea073687d915724497fa422005e56011fcf7d74483d30fd502a0ae1992`  
		Last Modified: Wed, 17 Nov 2021 19:20:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114a479d47bf9ce3b07ffb880a448300b978f0dd2fb9b2cf257248dd29de5e84`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae5a388a1926cb6bd2604c7cd0f60a2b859f5e9fee54ab1e3c28cc3c479ab3`  
		Last Modified: Thu, 18 Nov 2021 00:44:34 GMT  
		Size: 95.7 MB (95703056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f35b4aed8fe029d1de9c2be5697656a92bf97140d97728899485277fc3dc043`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b65826b08c9f8a035ad260f0b62525f5a8d4fb146976d525e46b4f75d06daad`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69ab7947819ba989edf4080ac113062525d4d969acf0cae72997265373542b`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 2.7 MB (2749693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17daca5299618a3df09e55bfc7d4ca161dd7625f44b57e9168de012d0cba9bf`  
		Last Modified: Thu, 18 Nov 2021 00:44:13 GMT  
		Size: 47.9 MB (47933761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1076865c1e2494ca329b3cc9ff6da40aab3182b6dd6a011e88f0ac330903a38`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; ppc64le

```console
$ docker pull redmine@sha256:b2a72eec46af19fb7d6ed6d7e92357dae1dad9c78913fdd1804e9cf91b88dded
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 MB (233416507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7901d28503a819d617abb587836a5e24d00896d36d2c06bfb971214e9c1a7ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 03:30:22 GMT
ADD file:c0f8b5d4d419bef7a494df5330ecf7bbea3cbb6462308ca0b2f26771f125dea0 in / 
# Wed, 17 Nov 2021 03:30:29 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:17:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 13:17:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 14:18:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 14:18:21 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 14:18:23 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 14:24:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 14:24:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 14:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 14:24:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 14:25:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 14:25:02 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 12:34:28 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 12:36:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 12:36:47 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 12:36:49 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 12:36:52 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 12:36:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 12:36:59 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 12:37:03 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 12:37:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 12:41:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 12:41:06 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 12:41:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 12:41:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 12:41:12 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 12:41:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:459de0a111d5c931674a5150ef4ae6bb1ffb1685380f4aafdba04a37d556c5de`  
		Last Modified: Wed, 17 Nov 2021 03:58:14 GMT  
		Size: 30.6 MB (30562278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4a8cb8add512175dbaeb682e1d37722eb039847e94d43b2c548f6bf9f4566`  
		Last Modified: Wed, 17 Nov 2021 14:30:35 GMT  
		Size: 12.7 MB (12705482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02accf8c69e0fb54236daa23b1409d80e215845f8d744672e8be1de6353c73f4`  
		Last Modified: Wed, 17 Nov 2021 14:30:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecde72085a62fc055b92d08be845488e745acea10ff923c9db7192bc696536f9`  
		Last Modified: Wed, 17 Nov 2021 14:35:36 GMT  
		Size: 22.0 MB (21985050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528aeb277a5e499d35f24f6a6cf6b7ff6d8081b0d8d6aebe5fd6ed9e1acc2ae9`  
		Last Modified: Wed, 17 Nov 2021 14:35:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ab84cc7e1bfe4aea4203f0b208c6c68525b8099d34b3e9e7e10bb8922f336a`  
		Last Modified: Thu, 18 Nov 2021 12:54:36 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac3ad29bd5d2fa76fc3e17b2cad931e27e964c1ab1d5719764c7ebee0499afb`  
		Last Modified: Thu, 18 Nov 2021 12:54:54 GMT  
		Size: 101.3 MB (101327224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611b8e12805d003ae459b61332e6f65bd87cbba3e536963dc9a54f590a900f4e`  
		Last Modified: Thu, 18 Nov 2021 12:54:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86fa7e52248ab830b7e4145f15e2faeaeef1d3a14eb38547c6b9f84565f52f0`  
		Last Modified: Thu, 18 Nov 2021 12:54:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6d03f3c26482ecff5d578cf84f5fe1e686d358fca9f81d29c304aeed3ccbd8`  
		Last Modified: Thu, 18 Nov 2021 12:54:33 GMT  
		Size: 2.7 MB (2749697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80771f58c2852198736609e9b5a7bd5424e523ff86f0572cf8a582b6497b9ac`  
		Last Modified: Thu, 18 Nov 2021 12:54:41 GMT  
		Size: 64.1 MB (64082530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984738625303ed821d53f4cdee26807e146ccdcf61904dc8c6154234573d0fc`  
		Last Modified: Thu, 18 Nov 2021 12:54:32 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1` - linux; s390x

```console
$ docker pull redmine@sha256:9826545cabb708f82a39645294fa6b4fe18682bb2a4ffb5ab0e03df343105640
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c5a19ee3f59933d996cab7415a6e6c2b50b869db65a686da493239b6369795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:42:37 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:44:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:44:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:44:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:44:07 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:34:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:34:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:34:43 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:34:43 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:34:43 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:34:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:34:44 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 17 Nov 2021 20:34:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 17 Nov 2021 20:34:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:36:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:36:25 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:36:25 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:36:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:36:25 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:36:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdaf56dd9686cdaca63c3c8ebab2d6841412a36159619d65853daa75500716`  
		Last Modified: Wed, 17 Nov 2021 09:51:17 GMT  
		Size: 21.6 MB (21619852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80433d0a1bacd8eb06bb301d366ea459dbae5ce9a2bea94372bd52e0939584a0`  
		Last Modified: Wed, 17 Nov 2021 09:51:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e82306e7113526e6aa75620a186091a8a2139c7e63336bc2033df0329cda36e`  
		Last Modified: Wed, 17 Nov 2021 20:39:48 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953e01eb8398b7e411547f900d6743483788b91446a4926c04d404495bcf814d`  
		Last Modified: Wed, 17 Nov 2021 20:40:00 GMT  
		Size: 91.8 MB (91791049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1786d101777e089e8f553bcd02e217229ae859817f642c2f4cc3ca482cc0037`  
		Last Modified: Wed, 17 Nov 2021 20:39:47 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c61376d40c4d7e02c177f7eac3f8f9f9d178c9cd308cd3149faf04c5b996a0c`  
		Last Modified: Wed, 17 Nov 2021 20:39:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724041fbce20361ad4bdeb17188bc355919db94cbb31d708760c028462b42b79`  
		Last Modified: Wed, 17 Nov 2021 20:39:47 GMT  
		Size: 2.7 MB (2749696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04445b75a0da224ae20d97016f3fea6736bd6b4f52e4495f86383539978fd06f`  
		Last Modified: Wed, 17 Nov 2021 20:39:52 GMT  
		Size: 63.5 MB (63473511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a50e8d09d481494c64c56360e2fe1c3ab6735d8af151d9d117a22d56114b82a`  
		Last Modified: Wed, 17 Nov 2021 20:39:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1-alpine`

```console
$ docker pull redmine@sha256:6dbd35c35e023b696f652aa87bf1de330ef19513a1b85a00928f30244c701767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:fae3d2c173aad1c4ccf2ae887f62847716af5f908fa917fbac07b10913b45913
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160030996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4714a18668c5842cac48a8a5bf13f3af01f3662dadbd9b44c49730c89b727d24`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_MAJOR=2.6
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_VERSION=2.6.8
# Sat, 13 Nov 2021 06:51:31 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Sat, 13 Nov 2021 06:54:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:54:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:54:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:54:46 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:31:40 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:31:48 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:31:48 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:31:49 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:31:49 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:31:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:31:50 GMT
ENV REDMINE_VERSION=4.1.5
# Sat, 13 Nov 2021 14:31:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Sat, 13 Nov 2021 14:31:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:31:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:34:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:34:01 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:34:01 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:34:02 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:34:02 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fd76747f3be3e4f4af1119b668fd5a9fa53725f84b429575cfb26c0d5f842a`  
		Last Modified: Sat, 13 Nov 2021 06:59:00 GMT  
		Size: 19.5 MB (19500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bbfb1229cd3c27d4dd990a0daf591e427afbc679b854303415a9e9a01ff10b`  
		Last Modified: Sat, 13 Nov 2021 06:58:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c267c2d73515a2e4fbaac349e5a31212348b7d72b21f80611dac1923c5c68666`  
		Last Modified: Sat, 13 Nov 2021 14:37:15 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e62a0f0fc43b5aab817648e0aea8e8dcd39e0f5e7ee6ce76236ac5f49653e2`  
		Last Modified: Sat, 13 Nov 2021 14:37:25 GMT  
		Size: 69.5 MB (69547670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ce34581c9e5eb65bc5ed69717166b196e1a17a8607e3721ae1b07c1cb90c8`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a2fb4d61b7d1eb854991664d217dae48916bd3cf240c27f4fa2534973b40a5`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6afa58a2a007900b48af7fe611027ca52ed3c1034ea34e75d6db8dddb5b18d1`  
		Last Modified: Sat, 13 Nov 2021 14:37:14 GMT  
		Size: 2.8 MB (2750433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a6c05fbcb5a65730f500ffa36488a9d0667133c3c4e784f88e4c8c966f946c`  
		Last Modified: Sat, 13 Nov 2021 14:37:19 GMT  
		Size: 61.8 MB (61824139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03693e88b691e6215bdd51b25ee8b9e56f1967a1ee89d59e4ecc12f354cbcb28`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1-passenger`

```console
$ docker pull redmine@sha256:a930032d3fae3d9630c334954316d4d43e3a13bee1f1497572d50f01315f0d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:e26cd6b0f6f7327fd56b4bd9b0c3d732db7048a421a7710a82f29e676acc5b84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232328645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c4d4935137f412f34e0743c6d9b95a5cefb4fe36755d9b578fe0f855c9d7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 23:47:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:47:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:47:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:47:17 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:32:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:32:57 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:32:57 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:32:58 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:32:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:32:59 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 20:32:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 20:33:03 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:33:44 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:33:44 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:33:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:33:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:33:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 18 Nov 2021 20:33:53 GMT
ENV PASSENGER_VERSION=6.0.12
# Thu, 18 Nov 2021 20:34:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:34:11 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 18 Nov 2021 20:34:11 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 18 Nov 2021 20:34:11 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0513aa66c0fb3e8b2ca883a3e8d1981bbfe8bfb788a9a888b723787293986e7d`  
		Last Modified: Wed, 17 Nov 2021 23:53:54 GMT  
		Size: 21.5 MB (21467890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dcedae4b9e16af3b588b2e085edcdc9b5895d6dcbd0f3c7886780233e285c2`  
		Last Modified: Wed, 17 Nov 2021 23:53:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31fda4ca0ea33330c7d7c55c465fd2b24a8bd41e15481cc208eddeb93c3aa72`  
		Last Modified: Thu, 18 Nov 2021 20:38:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1094964e4a9a3498a54642ac2a0993b548287ab34427c8f3ad03217fb4e31df1`  
		Last Modified: Thu, 18 Nov 2021 20:38:58 GMT  
		Size: 94.1 MB (94086142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b39fdcb59e4fd92888f29e12fe787da7cbd3ae68f1b4cbe5a1f22a3503761f`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c0c4680fcc99ce7feec161178b633a6e149735dba692adcddd78a4d3f62e66`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe18ef703b3280b5a608d351b9967f0441103296f4ac67f5ffa8772492c42877`  
		Last Modified: Thu, 18 Nov 2021 20:38:41 GMT  
		Size: 2.7 MB (2749693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8beb40f499f277318dbeaeb906ac2767f6a116457f9e0e8bc9e31c5e34c8950`  
		Last Modified: Thu, 18 Nov 2021 20:38:46 GMT  
		Size: 47.9 MB (47940531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc66131f0ad46ada0132e9bd266dff4315cc7cdf0de54deba17ffe354d8954b`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d5debc95815164a7cbb02ecc87215bdb5f4c1d89c4f2eb1037e718ee4e5a27`  
		Last Modified: Thu, 18 Nov 2021 20:39:12 GMT  
		Size: 21.4 MB (21436664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494390e0fc54c983e17ca5623c3288f621d5a136f1e8138e7a8f3408ddf4477e`  
		Last Modified: Thu, 18 Nov 2021 20:39:10 GMT  
		Size: 4.9 MB (4924661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.5`

```console
$ docker pull redmine@sha256:73d4140c6a63fdfd3aecd3995e1eab4a865089eb8745597b706c6c43ee3bc9f2
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

### `redmine:4.1.5` - linux; amd64

```console
$ docker pull redmine@sha256:e64090cf4e8222741582e7ca5eeea4b11b2207e28d54cbd805ab79aa7e090a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205967320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d1171fd21f42b7973c030b65604a792fb7887cdd44eeaa0b9d877d2fba6a64`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 23:47:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:47:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:47:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:47:17 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:32:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:32:57 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:32:57 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:32:58 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:32:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:32:59 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 20:32:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 20:33:03 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:33:44 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:33:44 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:33:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:33:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:33:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0513aa66c0fb3e8b2ca883a3e8d1981bbfe8bfb788a9a888b723787293986e7d`  
		Last Modified: Wed, 17 Nov 2021 23:53:54 GMT  
		Size: 21.5 MB (21467890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dcedae4b9e16af3b588b2e085edcdc9b5895d6dcbd0f3c7886780233e285c2`  
		Last Modified: Wed, 17 Nov 2021 23:53:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31fda4ca0ea33330c7d7c55c465fd2b24a8bd41e15481cc208eddeb93c3aa72`  
		Last Modified: Thu, 18 Nov 2021 20:38:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1094964e4a9a3498a54642ac2a0993b548287ab34427c8f3ad03217fb4e31df1`  
		Last Modified: Thu, 18 Nov 2021 20:38:58 GMT  
		Size: 94.1 MB (94086142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b39fdcb59e4fd92888f29e12fe787da7cbd3ae68f1b4cbe5a1f22a3503761f`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c0c4680fcc99ce7feec161178b633a6e149735dba692adcddd78a4d3f62e66`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe18ef703b3280b5a608d351b9967f0441103296f4ac67f5ffa8772492c42877`  
		Last Modified: Thu, 18 Nov 2021 20:38:41 GMT  
		Size: 2.7 MB (2749693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8beb40f499f277318dbeaeb906ac2767f6a116457f9e0e8bc9e31c5e34c8950`  
		Last Modified: Thu, 18 Nov 2021 20:38:46 GMT  
		Size: 47.9 MB (47940531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc66131f0ad46ada0132e9bd266dff4315cc7cdf0de54deba17ffe354d8954b`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; arm variant v5

```console
$ docker pull redmine@sha256:1c94633e8399caf4c132a211446786e5619f3aaf3ada17936c3fd61a4d5b8d75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (209987469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda7e6f28c2718c2fd381ac850bc956317f91deebb5e1b09c36b4c90aeaf63d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 20:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:53:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 20:53:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:48:32 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 21:48:33 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 21:48:33 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 21:52:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 21:52:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 21:53:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 21:53:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:53:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 21:53:02 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 14:44:02 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 14:45:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 14:45:12 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 14:45:13 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 14:45:13 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 14:45:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 14:45:15 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 14:45:16 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 14:45:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 14:50:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 14:50:50 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 14:50:51 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 14:50:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 14:50:52 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 14:50:52 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58fbebb8e6e22b1601002ddb4252e30c3750edfb93b87424f6c1a971c665bf`  
		Last Modified: Wed, 17 Nov 2021 21:59:40 GMT  
		Size: 10.3 MB (10349405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484eb5c97eceafe50be8deba254566cb365fd68cb0baa2e5418ecece614c2728`  
		Last Modified: Wed, 17 Nov 2021 21:59:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036dbb00becdfbc8994f79e0968b90235a36a6cd3adc53d1b0c485d366b86b8e`  
		Last Modified: Wed, 17 Nov 2021 22:06:25 GMT  
		Size: 20.7 MB (20733420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806e9836f556f43332540c90936bf1e6812bc8a816ed3e8303d24274160315a6`  
		Last Modified: Wed, 17 Nov 2021 22:06:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f025c68191e2d7bfb99dff9d80fb197ff374bbf772cd136ee4832dd436b780`  
		Last Modified: Thu, 18 Nov 2021 15:00:38 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e7e4e417ce998b2acf5a43d5e3d310e5d173f0350246f67d6a64d2eb65efd3`  
		Last Modified: Thu, 18 Nov 2021 15:01:38 GMT  
		Size: 89.6 MB (89577157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca15bf4b25fc8043840be160137dbf12973d10853056a17e105122ff7fb7488b`  
		Last Modified: Thu, 18 Nov 2021 15:00:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de134ee415ecb51b4b8f7f8245896598264f9a051bc523882011eadb9c808ddc`  
		Last Modified: Thu, 18 Nov 2021 15:00:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46654bccee7c4ee01c5b4e984f1138dc6d5021a27ee4f16d4c9563e27df207a2`  
		Last Modified: Thu, 18 Nov 2021 15:00:40 GMT  
		Size: 2.7 MB (2749688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08825881a785d1b44df9240ad1d4946af7d2f9f5514731680fc5b481bdf23b64`  
		Last Modified: Thu, 18 Nov 2021 15:01:05 GMT  
		Size: 61.7 MB (61687247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5eb3a1c5d65c75b6f9876aa32b8dacfbc3cfec3213dd1d9ecf44359de733040`  
		Last Modified: Thu, 18 Nov 2021 15:00:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; arm variant v7

```console
$ docker pull redmine@sha256:389987777a69d488dc09951bbed7578a3b4fa5fc31508b370cefeeff5dd5489e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203154542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7962ae32020d8125d72ff7386cb75d025459c2377ae72427084b34d3f625133b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 08:17:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:17:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 18 Nov 2021 08:17:06 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 09:11:05 GMT
ENV RUBY_MAJOR=2.6
# Thu, 18 Nov 2021 09:11:06 GMT
ENV RUBY_VERSION=2.6.8
# Thu, 18 Nov 2021 09:11:06 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Thu, 18 Nov 2021 09:15:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 18 Nov 2021 09:15:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Nov 2021 09:15:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Nov 2021 09:15:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 09:15:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 18 Nov 2021 09:15:18 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:06:17 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:07:21 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:07:21 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:07:22 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:07:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:07:24 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 20:07:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 20:07:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:12:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:12:45 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:12:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:12:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:12:46 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:12:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8e57706e11dcf2202a1ed28d022f7fe3daa306f06bf5311fee3d20b17f772`  
		Last Modified: Thu, 18 Nov 2021 09:24:19 GMT  
		Size: 9.9 MB (9872912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad345207fbbb28e02d7546fe9ec9b203219b39a7b6fe1a2c55d63e665ce8dd`  
		Last Modified: Thu, 18 Nov 2021 09:24:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb93faf1d4d1280ed90b904594838922fe363b19f403a1b9f79ea35b777e723`  
		Last Modified: Thu, 18 Nov 2021 09:31:29 GMT  
		Size: 20.6 MB (20643872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0931e5d4868154d483cf1176a216b4308c09ff1d5974bdf06aa52e79249b1b`  
		Last Modified: Thu, 18 Nov 2021 09:31:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34924d8de6aa6fc15f014748545368c4050bd41e82c42881addaad1d6ce5af1d`  
		Last Modified: Thu, 18 Nov 2021 20:22:03 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe847a0cc5e49032edaabc4ad79b83561b131b1c8a64b36cc4035b34c45cd2bd`  
		Last Modified: Thu, 18 Nov 2021 20:22:58 GMT  
		Size: 85.6 MB (85589341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1271f98e88e2007683620d81d1d7ce1b142d0a611489db9590e907c2cf09d568`  
		Last Modified: Thu, 18 Nov 2021 20:22:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2774949041c54ccd1dc64156df7789cc9153f1bbffdaf1af8144f160f53c1f`  
		Last Modified: Thu, 18 Nov 2021 20:22:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b1a61dcb7c1a9b2700646db446500e50b5f2a99f9b3b23eb023f785c1b2986`  
		Last Modified: Thu, 18 Nov 2021 20:22:05 GMT  
		Size: 2.7 MB (2749688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46bdde1d4f5ccd620ae520c006f1ae9e16a531d474e1cb8357b26d4dc81ca85`  
		Last Modified: Thu, 18 Nov 2021 20:22:28 GMT  
		Size: 61.5 MB (61540135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a98df33a6bb62fe1a80d31d76b11984e941c4966a3b70ded2ca0c1a22d0fed3`  
		Last Modified: Thu, 18 Nov 2021 20:22:02 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b222b2102035ba87c72076afd3f971a910dd6cfa4627c0423b876748b40dea1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216401827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871b1f794b4d0fcb638c8a57721a72acc701c347e2e647a928da47a7dc1c8c9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:46:01 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:46:02 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:46:03 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:48:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:48:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:48:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:48:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:48:06 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:49:55 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:50:19 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:50:20 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:50:21 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:50:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:50:23 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 17 Nov 2021 19:50:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 17 Nov 2021 19:50:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:52:38 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:52:40 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:52:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:52:41 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:52:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16912dae180f72843a7e6b7dd25071e1090943354879adab903dcd984c8cee67`  
		Last Modified: Wed, 17 Nov 2021 09:54:26 GMT  
		Size: 21.1 MB (21095263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b73b9ee9aa5f816c4fb7665c7e19fe1663007ac1aacb74064aac56ece594983`  
		Last Modified: Wed, 17 Nov 2021 09:54:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb50985615235593da91e201ffe4b1db40feab50ab0a12b02a4c99191da4dfd`  
		Last Modified: Wed, 17 Nov 2021 19:57:02 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b972b42f387b463ec4f85b98ff1de46778da88cde8db5210abd6cdb28fcfe996`  
		Last Modified: Wed, 17 Nov 2021 19:57:16 GMT  
		Size: 92.6 MB (92615309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d5c078974fd14c58f0b3b7716527a89b7fd62214cbd050a80d385982968927`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302584afc613dd65a75b5bcda18ac7919a7c809a1df57148453b3f76954ed897`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d073b657b29ddf797af445ca3996a8594b19899f364b2cc3d189f86a3fcf0deb`  
		Last Modified: Wed, 17 Nov 2021 19:57:00 GMT  
		Size: 2.7 MB (2749627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca343679f96ad8123399df85aad69f3174b5d405b2d11bf4804a0840974e2710`  
		Last Modified: Wed, 17 Nov 2021 19:57:10 GMT  
		Size: 62.8 MB (62752672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1dcf76925b4813ce41dd25c0b93567defab250f8d74eac3e070f92b49c068`  
		Last Modified: Wed, 17 Nov 2021 19:56:59 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; 386

```console
$ docker pull redmine@sha256:156a98e108ae32310750def5670b7f14ce4791c8fba4fc62b4389d126421ee10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212332382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b8c8954f2416156578d6b917f84622fb2feacefa48597e8b97e216b5700b97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 19:07:29 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 19:11:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:11:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:11:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:12:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:12:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:12:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:37:59 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:38:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:38:32 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:38:33 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:38:33 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:38:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:38:34 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 00:38:34 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 00:38:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:39:29 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:39:29 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:39:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:39:30 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:39:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8e5a4df5a8f121515c23ab2e470f17d64c6bb138b6c22dda592fcde5393ca4`  
		Last Modified: Wed, 17 Nov 2021 19:20:39 GMT  
		Size: 20.9 MB (20910059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955765ea073687d915724497fa422005e56011fcf7d74483d30fd502a0ae1992`  
		Last Modified: Wed, 17 Nov 2021 19:20:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114a479d47bf9ce3b07ffb880a448300b978f0dd2fb9b2cf257248dd29de5e84`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ae5a388a1926cb6bd2604c7cd0f60a2b859f5e9fee54ab1e3c28cc3c479ab3`  
		Last Modified: Thu, 18 Nov 2021 00:44:34 GMT  
		Size: 95.7 MB (95703056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f35b4aed8fe029d1de9c2be5697656a92bf97140d97728899485277fc3dc043`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b65826b08c9f8a035ad260f0b62525f5a8d4fb146976d525e46b4f75d06daad`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69ab7947819ba989edf4080ac113062525d4d969acf0cae72997265373542b`  
		Last Modified: Thu, 18 Nov 2021 00:44:01 GMT  
		Size: 2.7 MB (2749693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17daca5299618a3df09e55bfc7d4ca161dd7625f44b57e9168de012d0cba9bf`  
		Last Modified: Thu, 18 Nov 2021 00:44:13 GMT  
		Size: 47.9 MB (47933761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1076865c1e2494ca329b3cc9ff6da40aab3182b6dd6a011e88f0ac330903a38`  
		Last Modified: Thu, 18 Nov 2021 00:43:58 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; ppc64le

```console
$ docker pull redmine@sha256:b2a72eec46af19fb7d6ed6d7e92357dae1dad9c78913fdd1804e9cf91b88dded
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 MB (233416507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7901d28503a819d617abb587836a5e24d00896d36d2c06bfb971214e9c1a7ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 03:30:22 GMT
ADD file:c0f8b5d4d419bef7a494df5330ecf7bbea3cbb6462308ca0b2f26771f125dea0 in / 
# Wed, 17 Nov 2021 03:30:29 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:17:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 13:17:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 14:18:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 14:18:21 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 14:18:23 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 14:24:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 14:24:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 14:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 14:24:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 14:25:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 14:25:02 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 12:34:28 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 12:36:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 12:36:47 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 12:36:49 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 12:36:52 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 12:36:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 12:36:59 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 12:37:03 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 12:37:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 12:41:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 12:41:06 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 12:41:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 12:41:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 12:41:12 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 12:41:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:459de0a111d5c931674a5150ef4ae6bb1ffb1685380f4aafdba04a37d556c5de`  
		Last Modified: Wed, 17 Nov 2021 03:58:14 GMT  
		Size: 30.6 MB (30562278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4a8cb8add512175dbaeb682e1d37722eb039847e94d43b2c548f6bf9f4566`  
		Last Modified: Wed, 17 Nov 2021 14:30:35 GMT  
		Size: 12.7 MB (12705482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02accf8c69e0fb54236daa23b1409d80e215845f8d744672e8be1de6353c73f4`  
		Last Modified: Wed, 17 Nov 2021 14:30:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecde72085a62fc055b92d08be845488e745acea10ff923c9db7192bc696536f9`  
		Last Modified: Wed, 17 Nov 2021 14:35:36 GMT  
		Size: 22.0 MB (21985050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528aeb277a5e499d35f24f6a6cf6b7ff6d8081b0d8d6aebe5fd6ed9e1acc2ae9`  
		Last Modified: Wed, 17 Nov 2021 14:35:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ab84cc7e1bfe4aea4203f0b208c6c68525b8099d34b3e9e7e10bb8922f336a`  
		Last Modified: Thu, 18 Nov 2021 12:54:36 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac3ad29bd5d2fa76fc3e17b2cad931e27e964c1ab1d5719764c7ebee0499afb`  
		Last Modified: Thu, 18 Nov 2021 12:54:54 GMT  
		Size: 101.3 MB (101327224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611b8e12805d003ae459b61332e6f65bd87cbba3e536963dc9a54f590a900f4e`  
		Last Modified: Thu, 18 Nov 2021 12:54:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86fa7e52248ab830b7e4145f15e2faeaeef1d3a14eb38547c6b9f84565f52f0`  
		Last Modified: Thu, 18 Nov 2021 12:54:32 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6d03f3c26482ecff5d578cf84f5fe1e686d358fca9f81d29c304aeed3ccbd8`  
		Last Modified: Thu, 18 Nov 2021 12:54:33 GMT  
		Size: 2.7 MB (2749697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80771f58c2852198736609e9b5a7bd5424e523ff86f0572cf8a582b6497b9ac`  
		Last Modified: Thu, 18 Nov 2021 12:54:41 GMT  
		Size: 64.1 MB (64082530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984738625303ed821d53f4cdee26807e146ccdcf61904dc8c6154234573d0fc`  
		Last Modified: Thu, 18 Nov 2021 12:54:32 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.1.5` - linux; s390x

```console
$ docker pull redmine@sha256:9826545cabb708f82a39645294fa6b4fe18682bb2a4ffb5ab0e03df343105640
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216222662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c5a19ee3f59933d996cab7415a6e6c2b50b869db65a686da493239b6369795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 09:42:36 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 09:42:37 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 09:44:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:44:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:44:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:44:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:44:07 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:34:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:34:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:34:43 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:34:43 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:34:43 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:34:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:34:44 GMT
ENV REDMINE_VERSION=4.1.5
# Wed, 17 Nov 2021 20:34:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Wed, 17 Nov 2021 20:34:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:36:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:36:25 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:36:25 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:36:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:36:25 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:36:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdaf56dd9686cdaca63c3c8ebab2d6841412a36159619d65853daa75500716`  
		Last Modified: Wed, 17 Nov 2021 09:51:17 GMT  
		Size: 21.6 MB (21619852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80433d0a1bacd8eb06bb301d366ea459dbae5ce9a2bea94372bd52e0939584a0`  
		Last Modified: Wed, 17 Nov 2021 09:51:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e82306e7113526e6aa75620a186091a8a2139c7e63336bc2033df0329cda36e`  
		Last Modified: Wed, 17 Nov 2021 20:39:48 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953e01eb8398b7e411547f900d6743483788b91446a4926c04d404495bcf814d`  
		Last Modified: Wed, 17 Nov 2021 20:40:00 GMT  
		Size: 91.8 MB (91791049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1786d101777e089e8f553bcd02e217229ae859817f642c2f4cc3ca482cc0037`  
		Last Modified: Wed, 17 Nov 2021 20:39:47 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c61376d40c4d7e02c177f7eac3f8f9f9d178c9cd308cd3149faf04c5b996a0c`  
		Last Modified: Wed, 17 Nov 2021 20:39:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724041fbce20361ad4bdeb17188bc355919db94cbb31d708760c028462b42b79`  
		Last Modified: Wed, 17 Nov 2021 20:39:47 GMT  
		Size: 2.7 MB (2749696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04445b75a0da224ae20d97016f3fea6736bd6b4f52e4495f86383539978fd06f`  
		Last Modified: Wed, 17 Nov 2021 20:39:52 GMT  
		Size: 63.5 MB (63473511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a50e8d09d481494c64c56360e2fe1c3ab6735d8af151d9d117a22d56114b82a`  
		Last Modified: Wed, 17 Nov 2021 20:39:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.5-alpine`

```console
$ docker pull redmine@sha256:6dbd35c35e023b696f652aa87bf1de330ef19513a1b85a00928f30244c701767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1.5-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:fae3d2c173aad1c4ccf2ae887f62847716af5f908fa917fbac07b10913b45913
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160030996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4714a18668c5842cac48a8a5bf13f3af01f3662dadbd9b44c49730c89b727d24`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_MAJOR=2.6
# Sat, 13 Nov 2021 06:51:30 GMT
ENV RUBY_VERSION=2.6.8
# Sat, 13 Nov 2021 06:51:31 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Sat, 13 Nov 2021 06:54:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:54:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:54:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:54:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:54:46 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:31:40 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:31:48 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:31:48 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:31:49 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:31:49 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:31:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:31:50 GMT
ENV REDMINE_VERSION=4.1.5
# Sat, 13 Nov 2021 14:31:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Sat, 13 Nov 2021 14:31:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:31:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:34:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:34:01 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:34:01 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:34:02 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:34:02 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fd76747f3be3e4f4af1119b668fd5a9fa53725f84b429575cfb26c0d5f842a`  
		Last Modified: Sat, 13 Nov 2021 06:59:00 GMT  
		Size: 19.5 MB (19500293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bbfb1229cd3c27d4dd990a0daf591e427afbc679b854303415a9e9a01ff10b`  
		Last Modified: Sat, 13 Nov 2021 06:58:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c267c2d73515a2e4fbaac349e5a31212348b7d72b21f80611dac1923c5c68666`  
		Last Modified: Sat, 13 Nov 2021 14:37:15 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e62a0f0fc43b5aab817648e0aea8e8dcd39e0f5e7ee6ce76236ac5f49653e2`  
		Last Modified: Sat, 13 Nov 2021 14:37:25 GMT  
		Size: 69.5 MB (69547670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ce34581c9e5eb65bc5ed69717166b196e1a17a8607e3721ae1b07c1cb90c8`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a2fb4d61b7d1eb854991664d217dae48916bd3cf240c27f4fa2534973b40a5`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6afa58a2a007900b48af7fe611027ca52ed3c1034ea34e75d6db8dddb5b18d1`  
		Last Modified: Sat, 13 Nov 2021 14:37:14 GMT  
		Size: 2.8 MB (2750433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a6c05fbcb5a65730f500ffa36488a9d0667133c3c4e784f88e4c8c966f946c`  
		Last Modified: Sat, 13 Nov 2021 14:37:19 GMT  
		Size: 61.8 MB (61824139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03693e88b691e6215bdd51b25ee8b9e56f1967a1ee89d59e4ecc12f354cbcb28`  
		Last Modified: Sat, 13 Nov 2021 14:37:13 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.1.5-passenger`

```console
$ docker pull redmine@sha256:a930032d3fae3d9630c334954316d4d43e3a13bee1f1497572d50f01315f0d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.1.5-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:e26cd6b0f6f7327fd56b4bd9b0c3d732db7048a421a7710a82f29e676acc5b84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232328645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6c4d4935137f412f34e0743c6d9b95a5cefb4fe36755d9b578fe0f855c9d7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_MAJOR=2.6
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_VERSION=2.6.8
# Wed, 17 Nov 2021 23:44:19 GMT
ENV RUBY_DOWNLOAD_SHA256=8262e4663169c85787fdc9bfbd04d9eb86eb2a4b56d7f98373a8fcaa18e593eb
# Wed, 17 Nov 2021 23:47:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:47:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:47:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:47:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:47:17 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:32:31 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:32:57 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:32:57 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:32:58 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:32:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:32:59 GMT
ENV REDMINE_VERSION=4.1.5
# Thu, 18 Nov 2021 20:32:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=624dfeab7db5cda35a03d791b5fa83a836717ca280856c51cd089ed638f8678e
# Thu, 18 Nov 2021 20:33:03 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:33:44 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:33:44 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:33:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:33:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:33:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 18 Nov 2021 20:33:53 GMT
ENV PASSENGER_VERSION=6.0.12
# Thu, 18 Nov 2021 20:34:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:34:11 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 18 Nov 2021 20:34:11 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 18 Nov 2021 20:34:11 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0513aa66c0fb3e8b2ca883a3e8d1981bbfe8bfb788a9a888b723787293986e7d`  
		Last Modified: Wed, 17 Nov 2021 23:53:54 GMT  
		Size: 21.5 MB (21467890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dcedae4b9e16af3b588b2e085edcdc9b5895d6dcbd0f3c7886780233e285c2`  
		Last Modified: Wed, 17 Nov 2021 23:53:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31fda4ca0ea33330c7d7c55c465fd2b24a8bd41e15481cc208eddeb93c3aa72`  
		Last Modified: Thu, 18 Nov 2021 20:38:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1094964e4a9a3498a54642ac2a0993b548287ab34427c8f3ad03217fb4e31df1`  
		Last Modified: Thu, 18 Nov 2021 20:38:58 GMT  
		Size: 94.1 MB (94086142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b39fdcb59e4fd92888f29e12fe787da7cbd3ae68f1b4cbe5a1f22a3503761f`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c0c4680fcc99ce7feec161178b633a6e149735dba692adcddd78a4d3f62e66`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe18ef703b3280b5a608d351b9967f0441103296f4ac67f5ffa8772492c42877`  
		Last Modified: Thu, 18 Nov 2021 20:38:41 GMT  
		Size: 2.7 MB (2749693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8beb40f499f277318dbeaeb906ac2767f6a116457f9e0e8bc9e31c5e34c8950`  
		Last Modified: Thu, 18 Nov 2021 20:38:46 GMT  
		Size: 47.9 MB (47940531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc66131f0ad46ada0132e9bd266dff4315cc7cdf0de54deba17ffe354d8954b`  
		Last Modified: Thu, 18 Nov 2021 20:38:40 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d5debc95815164a7cbb02ecc87215bdb5f4c1d89c4f2eb1037e718ee4e5a27`  
		Last Modified: Thu, 18 Nov 2021 20:39:12 GMT  
		Size: 21.4 MB (21436664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494390e0fc54c983e17ca5623c3288f621d5a136f1e8138e7a8f3408ddf4477e`  
		Last Modified: Thu, 18 Nov 2021 20:39:10 GMT  
		Size: 4.9 MB (4924661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2`

```console
$ docker pull redmine@sha256:6654dea65d5e39a0419ac63df0e0ad6331f5da0f7831043663eca917fb5d3eea
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
$ docker pull redmine@sha256:68e8092f1d13c3e52d3aa807f7c0e5d55239fa8e032135a594f8da178b467623
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194811230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f79246dbb550a5674aad1819a04d406d7df4f3a807a5372f24043786984f50`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:32:12 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 23:34:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:34:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:35:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:35:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:30:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:31:12 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:31:12 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:31:12 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:31:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:31:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:32:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:01 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:32:01 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:32:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:32:01 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:32:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90b12affd87b4d38a8fcc325810d1d00be3ab2e7bcd8190a9c00b84593c078d`  
		Last Modified: Wed, 17 Nov 2021 23:52:50 GMT  
		Size: 14.5 MB (14510130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8d736be43fd318e714161260dcdb9952dad0c90be69d5376da0b7966ffc5a8`  
		Last Modified: Wed, 17 Nov 2021 23:52:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3019ede46444af81796abfe67c49e2fbabb9db7caeae19ac3c3af640d51440`  
		Last Modified: Thu, 18 Nov 2021 20:37:49 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f459f77e5a0c1928192bf809bbd6e9bb46b6ba4ab21a817e21f49658d9a33d`  
		Last Modified: Thu, 18 Nov 2021 20:38:03 GMT  
		Size: 94.1 MB (94089001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8ef100ec39cd24ccf9e86757ced4ffc4872d201ef840683fa0d01bbd478b2f`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676f59fd8e0144196b1551c4862751c016db7e7bd85d9c5ea7f47fd931c64aa`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d506c2d549b6dae794e30276395ea85c0e257a4c3afb861eee7a80aca20209`  
		Last Modified: Thu, 18 Nov 2021 20:37:47 GMT  
		Size: 3.1 MB (3063251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82700c911def9390d43716a8985c018ac47b62ef650f69a942d86a03fd4510ec`  
		Last Modified: Thu, 18 Nov 2021 20:37:51 GMT  
		Size: 43.4 MB (43425778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0cd4260e9359c26c12c25c14dcf660812c0bd324b62fc86c3f52dca359a33a`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; arm variant v5

```console
$ docker pull redmine@sha256:bf6bb00f96a0b12b11262fb56ebe66a814137dca38016393734d0cea84d063f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196300195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f73d796e667ea07abd3855ad0147a9bbbb9beb37276b61162547c05961f5059`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 20:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:53:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 20:53:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:30:49 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 21:30:50 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 21:30:50 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 21:35:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 21:35:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 21:35:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 21:35:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:35:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 21:35:11 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 14:36:38 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 14:37:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 14:37:57 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 14:37:57 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 14:37:58 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 14:37:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 14:38:00 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 14:38:00 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 14:38:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 14:43:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 14:43:45 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 14:43:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 14:43:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 14:43:47 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 14:43:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58fbebb8e6e22b1601002ddb4252e30c3750edfb93b87424f6c1a971c665bf`  
		Last Modified: Wed, 17 Nov 2021 21:59:40 GMT  
		Size: 10.3 MB (10349405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484eb5c97eceafe50be8deba254566cb365fd68cb0baa2e5418ecece614c2728`  
		Last Modified: Wed, 17 Nov 2021 21:59:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8a3180a4fd6dc5eb70d66bd3e4082e4d6a82432c594b34e550d6feab30b262`  
		Last Modified: Wed, 17 Nov 2021 22:04:27 GMT  
		Size: 13.9 MB (13871351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc80340d626dbcb066ecdc739e235877d725bc16934f56afcf1f9f7a5b1823b`  
		Last Modified: Wed, 17 Nov 2021 22:04:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29e7fbae5e92244d8b1ed80457eecf320d173303fdb99245a84599906c7666`  
		Last Modified: Thu, 18 Nov 2021 14:59:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b55931caf7268bdad6b385d5c79741a8a295c347cfb9fd8f639d1ba7c2a8d8`  
		Last Modified: Thu, 18 Nov 2021 15:00:15 GMT  
		Size: 89.6 MB (89577773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070f8378574f87a9aef84e45e5adeb05df20f39cb6d6d897df940e984084c75`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a18cbf12df5da376627c3bdee43d3813e66f035f637a7c2501f73ad4a1ba60`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2a5a07dcbabe1e7be1e52efada576b24511465600e52c6d7d19effc57d263`  
		Last Modified: Thu, 18 Nov 2021 14:59:15 GMT  
		Size: 3.1 MB (3063252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f00725466b5aef82f5484942c445b1712ba8af31b3158af20834ea48204588`  
		Last Modified: Thu, 18 Nov 2021 14:59:35 GMT  
		Size: 54.5 MB (54547862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49a55ad2f42152245a2269b8f870edac4fcbd328d63a8d72a3da64e94478c59`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; arm variant v7

```console
$ docker pull redmine@sha256:c92262d9b7966c7a14f0ca89c5545aa12583798740b923fa82f9025a40c1f246
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189440908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054a0dc932e7b49f5a55f646fb5d28485df4f2de75bff349cec7e7934c0fb639`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 08:17:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:17:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 18 Nov 2021 08:17:06 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 08:53:42 GMT
ENV RUBY_MAJOR=2.7
# Thu, 18 Nov 2021 08:53:42 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 18 Nov 2021 08:53:43 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 18 Nov 2021 08:57:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 18 Nov 2021 08:57:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Nov 2021 08:57:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Nov 2021 08:57:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 08:57:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 18 Nov 2021 08:57:49 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 19:59:23 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:00:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:00:29 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:00:30 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:00:30 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:00:32 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:00:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:00:38 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:05:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:05:55 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:05:56 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:05:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:05:57 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:05:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8e57706e11dcf2202a1ed28d022f7fe3daa306f06bf5311fee3d20b17f772`  
		Last Modified: Thu, 18 Nov 2021 09:24:19 GMT  
		Size: 9.9 MB (9872912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad345207fbbb28e02d7546fe9ec9b203219b39a7b6fe1a2c55d63e665ce8dd`  
		Last Modified: Thu, 18 Nov 2021 09:24:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d25e541e934fefcd6dcfff4226d06801527c28c5f31506d802ed03121e1320b`  
		Last Modified: Thu, 18 Nov 2021 09:29:28 GMT  
		Size: 13.8 MB (13767299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3459bd8cf29be58005e7ad4da22bdba7402a2d607ca5295fe58bac3d98f3b4`  
		Last Modified: Thu, 18 Nov 2021 09:29:21 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9465b374f5ec3e1d43e6b89b84be958e52aaf49669b4e1bbcb2f7bde6546969`  
		Last Modified: Thu, 18 Nov 2021 20:20:44 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f9e4f806a27273fd0d86a752ec0c68d34f29a4e216ac255ea3b98c2f8dee89`  
		Last Modified: Thu, 18 Nov 2021 20:21:39 GMT  
		Size: 85.6 MB (85589945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c32930c81becf489baf6eb5aa96cbcab402cc72b77824a8d5f3ef1164e827e`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874cebd85eed66ba44ad4ac91fc7a5c904705679507db88675f20541e50a55f5`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd024f80cae41f24e51ccb8fe006e4561cd72d216a72741b11521e70ecc17f`  
		Last Modified: Thu, 18 Nov 2021 20:20:46 GMT  
		Size: 3.1 MB (3063253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ddc84607a7f4665334e4c31b9dd59b1ba40a30a55fb387506edc020bb2c24`  
		Last Modified: Thu, 18 Nov 2021 20:21:06 GMT  
		Size: 54.4 MB (54388903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2cac2bcb44446a910b068386b9b7b82991cd1aed0cea1e34f6e772c6711ba5`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:86d444c24d077794c0c2cc949e49527863c9ca44e518c17e370b02eb4000216a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202113715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42218f16d6dac2e546b0a2281ab4659b776bbf51ec6e4acfbede94911bc9dcdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:41:19 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:41:20 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:41:21 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:43:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:43:17 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:46:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:46:40 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:46:41 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:46:42 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:46:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:46:44 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 19:46:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 19:46:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:49:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:49:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:49:40 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:49:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e74dfb7a4c0fdaf06af6628a5256217d8dc0d66250a1fbc0c123f00b986e22`  
		Last Modified: Wed, 17 Nov 2021 09:53:40 GMT  
		Size: 14.1 MB (14143923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb526ffb8eba3317294cf51375a464a78d261132b6b7491f254cf7a4a156682`  
		Last Modified: Wed, 17 Nov 2021 09:53:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21518ac2e5bab0f6dfc5e5d56cc37c2ddfe56b2be0f94f479a28844eda6b01df`  
		Last Modified: Wed, 17 Nov 2021 19:56:25 GMT  
		Size: 1.6 KB (1626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76248d3153c26ceb5416c50118694725c0c7d4ce7823824bd66101dc2c5a010d`  
		Last Modified: Wed, 17 Nov 2021 19:56:41 GMT  
		Size: 92.6 MB (92614747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31701ff7128027b1906c22a7653245cdb3cfac2d03494df00e25be248e743991`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac4b0eb26c86bcfc93c2657dfbeb8e1d3ef40e8785866c46e13be70741ec74b`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62ad39d6bc57963dc25a1ff3af302f01bf0d29bf1d984b097d829bcef8e71d3`  
		Last Modified: Wed, 17 Nov 2021 19:56:24 GMT  
		Size: 3.1 MB (3063387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c77a0ff1cda155087e0a1fd87440c1fd1f0de88ddcd0f7b027500ca9b1c5df9`  
		Last Modified: Wed, 17 Nov 2021 19:56:31 GMT  
		Size: 55.1 MB (55102701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe9431487572557c36e17868ec1e44d823b725205b047bd9b29f8cb63fea74`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; 386

```console
$ docker pull redmine@sha256:541bbc59f1f2165794af255e943fd64e76f231e68941d6e893fb057442a80b34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201449024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8a65a7d03b8eef85a6b4790bedd723f2249542a83c9e248f86e8bfe4ab2be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 18:58:23 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 19:02:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:02:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:02:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:02:53 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:36:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:36:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:36:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:36:42 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:36:43 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 00:36:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 00:36:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:37:43 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:37:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:37:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:37:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:37:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59002f4fc409c3fdcbd829fcc8f9d9186a49f4b1977b2c959714978bd07c75`  
		Last Modified: Wed, 17 Nov 2021 19:19:42 GMT  
		Size: 14.0 MB (13992752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1a3cc73f29df585791125514b63252077c65f4a1e212d1021c4e3020df3dd8`  
		Last Modified: Wed, 17 Nov 2021 19:19:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cff4a558af0642405c8aec1556aebdbaf4c9a86c0632d964e532934f76466c`  
		Last Modified: Thu, 18 Nov 2021 00:43:12 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700278801433da9ce13b80f7e86e2e5368cccf0e303e9862c537a154f05a540a`  
		Last Modified: Thu, 18 Nov 2021 00:43:36 GMT  
		Size: 95.7 MB (95702657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af28efd287aeb351d175e3c0f5ed184fa551cd1af7172bb7791a60a0537af9de`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8937baf10e23d531e21069ea81323b01572eee4aed6f64640685bb7ffaab8`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eb84ecf78a6f2698456d871cbe794d0bb45a6cece674d3d8251894cb1c1a01`  
		Last Modified: Thu, 18 Nov 2021 00:43:11 GMT  
		Size: 3.1 MB (3063250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676ab58b071fabf24debb26ce72f971b94290b362f51e44b6a19c2fe9b3371a9`  
		Last Modified: Thu, 18 Nov 2021 00:43:18 GMT  
		Size: 43.7 MB (43654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940c5fbe3e6915f01902f8855bf33b917442025553bce6ff1b11353827a7b58`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; ppc64le

```console
$ docker pull redmine@sha256:bc9e80acf291615ffb33dbb7ddbc4a7565d1de7ea50ce44aa4333ba6d433e342
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218955951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cacd26122b566b805c31159146c851de24b306f5db8b8302285459e98d9913b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 03:30:22 GMT
ADD file:c0f8b5d4d419bef7a494df5330ecf7bbea3cbb6462308ca0b2f26771f125dea0 in / 
# Wed, 17 Nov 2021 03:30:29 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:17:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 13:17:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 13:56:53 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 13:56:56 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 13:56:58 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 14:03:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 14:03:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 14:03:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 14:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 14:03:22 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 14:03:24 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 12:26:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 12:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 12:29:27 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 12:29:33 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 12:29:36 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 12:29:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 12:29:46 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 12:29:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 12:29:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 12:33:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 12:34:04 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 12:34:05 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 12:34:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 12:34:08 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 12:34:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:459de0a111d5c931674a5150ef4ae6bb1ffb1685380f4aafdba04a37d556c5de`  
		Last Modified: Wed, 17 Nov 2021 03:58:14 GMT  
		Size: 30.6 MB (30562278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4a8cb8add512175dbaeb682e1d37722eb039847e94d43b2c548f6bf9f4566`  
		Last Modified: Wed, 17 Nov 2021 14:30:35 GMT  
		Size: 12.7 MB (12705482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02accf8c69e0fb54236daa23b1409d80e215845f8d744672e8be1de6353c73f4`  
		Last Modified: Wed, 17 Nov 2021 14:30:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437d94d7e24e0cdbb2879c03363f9b475da2c6828f1d6efd64e6ace62304f455`  
		Last Modified: Wed, 17 Nov 2021 14:34:16 GMT  
		Size: 15.0 MB (14997053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b39e4205e8291bddd16d32f0575a50d2838f1141cdb3dfe1e4502de89dbb1bc`  
		Last Modified: Wed, 17 Nov 2021 14:34:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57265642992f45aec31dcaf12b72927b3e6854aae997a3fd18e7bda9b690b4d`  
		Last Modified: Thu, 18 Nov 2021 12:53:53 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27021a17b8f3615fdf08ab3a986a106ed0d9e0238da2792c9469b5fc2aa38b18`  
		Last Modified: Thu, 18 Nov 2021 12:54:12 GMT  
		Size: 101.3 MB (101327196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9324734dc2a75f7aa6a9f8488945f3181ad665697ef6c85255ff8ab2ebf892f7`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596f052e5e4de085618e67aac634fafdbd606e08d0d7f9f5017875238164e5a8`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c13ff8c3199f6a072a472251f1deeddc585eea60ad17ea7b97b08c06734d2`  
		Last Modified: Thu, 18 Nov 2021 12:53:51 GMT  
		Size: 3.1 MB (3063249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3621788bcdb3caeb1153a2622168e546f76b07dd3cc425b4bb733bbbc94d097`  
		Last Modified: Thu, 18 Nov 2021 12:53:58 GMT  
		Size: 56.3 MB (56296448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5cd3a2223e6188ca96341a558e604ad5bfecb69d6e230c836d280401865d7`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2` - linux; s390x

```console
$ docker pull redmine@sha256:49a1c1b85f8ccd222764c18d3694feaf0642800543699062e12064d13fecc636
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201879289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd54a6734cf67e04ecc514a8756a628f6b402e434e592dc8d1bf2a75b15627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:37:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:37:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:37:16 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:31:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:32:10 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:32:10 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:32:10 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:32:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 20:32:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:34:07 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:34:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:34:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:34:08 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:34:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa70e45053269d04d1a7217aca754f0b1fd37826bacef60c3e79535af03de7e`  
		Last Modified: Wed, 17 Nov 2021 09:50:18 GMT  
		Size: 14.7 MB (14697150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6665bc1be788124ffa49dc9aca2a874932441c39767aac3628a05b46b7f808`  
		Last Modified: Wed, 17 Nov 2021 09:50:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ad94a5ab88cff035b5e7ab928b3855131115a475ac3f69d13d3b648539b059`  
		Last Modified: Wed, 17 Nov 2021 20:39:22 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef81635c9981af53c3728bbbdf8957635a0b7afccb029ae985a6fe7e6ae527`  
		Last Modified: Wed, 17 Nov 2021 20:39:34 GMT  
		Size: 91.8 MB (91791039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8be6a475176385654d74664b9bc12bade950866233a6eb369175876849a61a9`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d214f8c5411f63986c0d7ee3a9032324738c7b89be0432e0ff9616a27a72485f`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a849b87f96d4317e30bb0352a51b94195d07907f8535be33300f0452e6808655`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05a462fbf41e321955f3c91b6791ba04c37145f855bda5355c75973c4705c2`  
		Last Modified: Wed, 17 Nov 2021 20:39:25 GMT  
		Size: 55.7 MB (55739301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740e646b3a43cb2398040cad7d9e0ed87da62a1457bd92bcc4d0c5a0b8be27c`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2-alpine`

```console
$ docker pull redmine@sha256:cf4ec4d559c84d289809ddc6554057e6522d3720200a340c70ba098c12202c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:518ba4effd92c427ef19922743eea649ed001436d8a66fe0de469abb2de00949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149044368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a04de41bf1795abeee36effc817551b3de5069209d3ec827816281c81211a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_MAJOR=2.7
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_VERSION=2.7.4
# Sat, 13 Nov 2021 06:44:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Sat, 13 Nov 2021 06:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:47:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:47:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:47:56 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:28:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:29:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:29:07 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:29:08 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:29:08 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_VERSION=4.2.3
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Sat, 13 Nov 2021 14:29:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:29:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:31:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:31:21 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:31:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:31:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:31:22 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:31:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e81c0605571c3961987ae1ce872ebef2b5bcb439010c194e90b47282556c32d`  
		Last Modified: Sat, 13 Nov 2021 06:58:25 GMT  
		Size: 14.0 MB (13994126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2814005984530d27bc89e1c810fb8cb01371038a28bc3d85a1e95b710d9e043e`  
		Last Modified: Sat, 13 Nov 2021 06:58:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171914095295d927972128e1f66156ce389cb697d40fc6d7ea68c919861015e`  
		Last Modified: Sat, 13 Nov 2021 14:36:45 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9802858485f172f49a49aa23ebc2ef97aa9a7dff598d4d6b18f27e107ae24436`  
		Last Modified: Sat, 13 Nov 2021 14:36:55 GMT  
		Size: 69.5 MB (69548252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5b29e3b352df46dbdcf96478507ab2ace06abee4b91e86cea6852a73067d98`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd79647c11e0ebdbaa7b41c71d969403768f7950e69f1b9eda5545fe42e86b3`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20504c29a1f01e91c83c2e1e82a90fb05c118bbf74d44fa621ec588a179bce4b`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 3.1 MB (3064272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7d43b9df6162fdd2b107724ff288c851a49738e7e04fa16cd34fddde661b04`  
		Last Modified: Sat, 13 Nov 2021 14:36:48 GMT  
		Size: 56.0 MB (56029256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561c4b4d66001dcdc5ff09131812075d6a6d4f6430e175565724033921e826f1`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2-passenger`

```console
$ docker pull redmine@sha256:1d213433b63a0ead8a70d021a5c132c60e4e748bbc9ca9a924df306b70f3244c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:e18a6ae0dcfc40dd6410992648ef1012830deff650ee75fe39dbfe061d12a342
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220974188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27853838e5a87da41ee207d9032436259a01c1e6474419f2c9c796931a4c34eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:32:12 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 23:34:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:34:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:35:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:35:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:30:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:31:12 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:31:12 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:31:12 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:31:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:31:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:32:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:01 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:32:01 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:32:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:32:01 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:32:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 18 Nov 2021 20:32:05 GMT
ENV PASSENGER_VERSION=6.0.12
# Thu, 18 Nov 2021 20:32:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:22 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 18 Nov 2021 20:32:23 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 18 Nov 2021 20:32:23 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90b12affd87b4d38a8fcc325810d1d00be3ab2e7bcd8190a9c00b84593c078d`  
		Last Modified: Wed, 17 Nov 2021 23:52:50 GMT  
		Size: 14.5 MB (14510130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8d736be43fd318e714161260dcdb9952dad0c90be69d5376da0b7966ffc5a8`  
		Last Modified: Wed, 17 Nov 2021 23:52:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3019ede46444af81796abfe67c49e2fbabb9db7caeae19ac3c3af640d51440`  
		Last Modified: Thu, 18 Nov 2021 20:37:49 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f459f77e5a0c1928192bf809bbd6e9bb46b6ba4ab21a817e21f49658d9a33d`  
		Last Modified: Thu, 18 Nov 2021 20:38:03 GMT  
		Size: 94.1 MB (94089001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8ef100ec39cd24ccf9e86757ced4ffc4872d201ef840683fa0d01bbd478b2f`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676f59fd8e0144196b1551c4862751c016db7e7bd85d9c5ea7f47fd931c64aa`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d506c2d549b6dae794e30276395ea85c0e257a4c3afb861eee7a80aca20209`  
		Last Modified: Thu, 18 Nov 2021 20:37:47 GMT  
		Size: 3.1 MB (3063251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82700c911def9390d43716a8985c018ac47b62ef650f69a942d86a03fd4510ec`  
		Last Modified: Thu, 18 Nov 2021 20:37:51 GMT  
		Size: 43.4 MB (43425778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0cd4260e9359c26c12c25c14dcf660812c0bd324b62fc86c3f52dca359a33a`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b65724c681012a606e5d41cfbe37546052cd471086212e239e21a5dfbdadaa1`  
		Last Modified: Thu, 18 Nov 2021 20:38:23 GMT  
		Size: 21.2 MB (21238341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916ee64f10c4bd1e7cf1bfcadb56aba80a65c2b1193197e39b1fa3be4829a355`  
		Last Modified: Thu, 18 Nov 2021 20:38:20 GMT  
		Size: 4.9 MB (4924617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2.3`

```console
$ docker pull redmine@sha256:6654dea65d5e39a0419ac63df0e0ad6331f5da0f7831043663eca917fb5d3eea
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

### `redmine:4.2.3` - linux; amd64

```console
$ docker pull redmine@sha256:68e8092f1d13c3e52d3aa807f7c0e5d55239fa8e032135a594f8da178b467623
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194811230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f79246dbb550a5674aad1819a04d406d7df4f3a807a5372f24043786984f50`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:32:12 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 23:34:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:34:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:35:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:35:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:30:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:31:12 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:31:12 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:31:12 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:31:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:31:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:32:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:01 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:32:01 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:32:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:32:01 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:32:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90b12affd87b4d38a8fcc325810d1d00be3ab2e7bcd8190a9c00b84593c078d`  
		Last Modified: Wed, 17 Nov 2021 23:52:50 GMT  
		Size: 14.5 MB (14510130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8d736be43fd318e714161260dcdb9952dad0c90be69d5376da0b7966ffc5a8`  
		Last Modified: Wed, 17 Nov 2021 23:52:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3019ede46444af81796abfe67c49e2fbabb9db7caeae19ac3c3af640d51440`  
		Last Modified: Thu, 18 Nov 2021 20:37:49 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f459f77e5a0c1928192bf809bbd6e9bb46b6ba4ab21a817e21f49658d9a33d`  
		Last Modified: Thu, 18 Nov 2021 20:38:03 GMT  
		Size: 94.1 MB (94089001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8ef100ec39cd24ccf9e86757ced4ffc4872d201ef840683fa0d01bbd478b2f`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676f59fd8e0144196b1551c4862751c016db7e7bd85d9c5ea7f47fd931c64aa`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d506c2d549b6dae794e30276395ea85c0e257a4c3afb861eee7a80aca20209`  
		Last Modified: Thu, 18 Nov 2021 20:37:47 GMT  
		Size: 3.1 MB (3063251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82700c911def9390d43716a8985c018ac47b62ef650f69a942d86a03fd4510ec`  
		Last Modified: Thu, 18 Nov 2021 20:37:51 GMT  
		Size: 43.4 MB (43425778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0cd4260e9359c26c12c25c14dcf660812c0bd324b62fc86c3f52dca359a33a`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; arm variant v5

```console
$ docker pull redmine@sha256:bf6bb00f96a0b12b11262fb56ebe66a814137dca38016393734d0cea84d063f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196300195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f73d796e667ea07abd3855ad0147a9bbbb9beb37276b61162547c05961f5059`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 20:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:53:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 20:53:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:30:49 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 21:30:50 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 21:30:50 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 21:35:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 21:35:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 21:35:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 21:35:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:35:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 21:35:11 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 14:36:38 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 14:37:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 14:37:57 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 14:37:57 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 14:37:58 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 14:37:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 14:38:00 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 14:38:00 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 14:38:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 14:43:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 14:43:45 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 14:43:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 14:43:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 14:43:47 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 14:43:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58fbebb8e6e22b1601002ddb4252e30c3750edfb93b87424f6c1a971c665bf`  
		Last Modified: Wed, 17 Nov 2021 21:59:40 GMT  
		Size: 10.3 MB (10349405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484eb5c97eceafe50be8deba254566cb365fd68cb0baa2e5418ecece614c2728`  
		Last Modified: Wed, 17 Nov 2021 21:59:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8a3180a4fd6dc5eb70d66bd3e4082e4d6a82432c594b34e550d6feab30b262`  
		Last Modified: Wed, 17 Nov 2021 22:04:27 GMT  
		Size: 13.9 MB (13871351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc80340d626dbcb066ecdc739e235877d725bc16934f56afcf1f9f7a5b1823b`  
		Last Modified: Wed, 17 Nov 2021 22:04:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29e7fbae5e92244d8b1ed80457eecf320d173303fdb99245a84599906c7666`  
		Last Modified: Thu, 18 Nov 2021 14:59:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b55931caf7268bdad6b385d5c79741a8a295c347cfb9fd8f639d1ba7c2a8d8`  
		Last Modified: Thu, 18 Nov 2021 15:00:15 GMT  
		Size: 89.6 MB (89577773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070f8378574f87a9aef84e45e5adeb05df20f39cb6d6d897df940e984084c75`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a18cbf12df5da376627c3bdee43d3813e66f035f637a7c2501f73ad4a1ba60`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2a5a07dcbabe1e7be1e52efada576b24511465600e52c6d7d19effc57d263`  
		Last Modified: Thu, 18 Nov 2021 14:59:15 GMT  
		Size: 3.1 MB (3063252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f00725466b5aef82f5484942c445b1712ba8af31b3158af20834ea48204588`  
		Last Modified: Thu, 18 Nov 2021 14:59:35 GMT  
		Size: 54.5 MB (54547862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49a55ad2f42152245a2269b8f870edac4fcbd328d63a8d72a3da64e94478c59`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; arm variant v7

```console
$ docker pull redmine@sha256:c92262d9b7966c7a14f0ca89c5545aa12583798740b923fa82f9025a40c1f246
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189440908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054a0dc932e7b49f5a55f646fb5d28485df4f2de75bff349cec7e7934c0fb639`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 08:17:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:17:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 18 Nov 2021 08:17:06 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 08:53:42 GMT
ENV RUBY_MAJOR=2.7
# Thu, 18 Nov 2021 08:53:42 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 18 Nov 2021 08:53:43 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 18 Nov 2021 08:57:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 18 Nov 2021 08:57:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Nov 2021 08:57:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Nov 2021 08:57:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 08:57:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 18 Nov 2021 08:57:49 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 19:59:23 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:00:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:00:29 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:00:30 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:00:30 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:00:32 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:00:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:00:38 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:05:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:05:55 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:05:56 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:05:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:05:57 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:05:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8e57706e11dcf2202a1ed28d022f7fe3daa306f06bf5311fee3d20b17f772`  
		Last Modified: Thu, 18 Nov 2021 09:24:19 GMT  
		Size: 9.9 MB (9872912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad345207fbbb28e02d7546fe9ec9b203219b39a7b6fe1a2c55d63e665ce8dd`  
		Last Modified: Thu, 18 Nov 2021 09:24:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d25e541e934fefcd6dcfff4226d06801527c28c5f31506d802ed03121e1320b`  
		Last Modified: Thu, 18 Nov 2021 09:29:28 GMT  
		Size: 13.8 MB (13767299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3459bd8cf29be58005e7ad4da22bdba7402a2d607ca5295fe58bac3d98f3b4`  
		Last Modified: Thu, 18 Nov 2021 09:29:21 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9465b374f5ec3e1d43e6b89b84be958e52aaf49669b4e1bbcb2f7bde6546969`  
		Last Modified: Thu, 18 Nov 2021 20:20:44 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f9e4f806a27273fd0d86a752ec0c68d34f29a4e216ac255ea3b98c2f8dee89`  
		Last Modified: Thu, 18 Nov 2021 20:21:39 GMT  
		Size: 85.6 MB (85589945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c32930c81becf489baf6eb5aa96cbcab402cc72b77824a8d5f3ef1164e827e`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874cebd85eed66ba44ad4ac91fc7a5c904705679507db88675f20541e50a55f5`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd024f80cae41f24e51ccb8fe006e4561cd72d216a72741b11521e70ecc17f`  
		Last Modified: Thu, 18 Nov 2021 20:20:46 GMT  
		Size: 3.1 MB (3063253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ddc84607a7f4665334e4c31b9dd59b1ba40a30a55fb387506edc020bb2c24`  
		Last Modified: Thu, 18 Nov 2021 20:21:06 GMT  
		Size: 54.4 MB (54388903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2cac2bcb44446a910b068386b9b7b82991cd1aed0cea1e34f6e772c6711ba5`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:86d444c24d077794c0c2cc949e49527863c9ca44e518c17e370b02eb4000216a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202113715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42218f16d6dac2e546b0a2281ab4659b776bbf51ec6e4acfbede94911bc9dcdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:41:19 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:41:20 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:41:21 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:43:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:43:17 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:46:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:46:40 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:46:41 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:46:42 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:46:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:46:44 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 19:46:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 19:46:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:49:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:49:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:49:40 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:49:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e74dfb7a4c0fdaf06af6628a5256217d8dc0d66250a1fbc0c123f00b986e22`  
		Last Modified: Wed, 17 Nov 2021 09:53:40 GMT  
		Size: 14.1 MB (14143923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb526ffb8eba3317294cf51375a464a78d261132b6b7491f254cf7a4a156682`  
		Last Modified: Wed, 17 Nov 2021 09:53:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21518ac2e5bab0f6dfc5e5d56cc37c2ddfe56b2be0f94f479a28844eda6b01df`  
		Last Modified: Wed, 17 Nov 2021 19:56:25 GMT  
		Size: 1.6 KB (1626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76248d3153c26ceb5416c50118694725c0c7d4ce7823824bd66101dc2c5a010d`  
		Last Modified: Wed, 17 Nov 2021 19:56:41 GMT  
		Size: 92.6 MB (92614747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31701ff7128027b1906c22a7653245cdb3cfac2d03494df00e25be248e743991`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac4b0eb26c86bcfc93c2657dfbeb8e1d3ef40e8785866c46e13be70741ec74b`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62ad39d6bc57963dc25a1ff3af302f01bf0d29bf1d984b097d829bcef8e71d3`  
		Last Modified: Wed, 17 Nov 2021 19:56:24 GMT  
		Size: 3.1 MB (3063387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c77a0ff1cda155087e0a1fd87440c1fd1f0de88ddcd0f7b027500ca9b1c5df9`  
		Last Modified: Wed, 17 Nov 2021 19:56:31 GMT  
		Size: 55.1 MB (55102701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe9431487572557c36e17868ec1e44d823b725205b047bd9b29f8cb63fea74`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; 386

```console
$ docker pull redmine@sha256:541bbc59f1f2165794af255e943fd64e76f231e68941d6e893fb057442a80b34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201449024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8a65a7d03b8eef85a6b4790bedd723f2249542a83c9e248f86e8bfe4ab2be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 18:58:23 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 19:02:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:02:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:02:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:02:53 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:36:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:36:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:36:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:36:42 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:36:43 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 00:36:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 00:36:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:37:43 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:37:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:37:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:37:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:37:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59002f4fc409c3fdcbd829fcc8f9d9186a49f4b1977b2c959714978bd07c75`  
		Last Modified: Wed, 17 Nov 2021 19:19:42 GMT  
		Size: 14.0 MB (13992752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1a3cc73f29df585791125514b63252077c65f4a1e212d1021c4e3020df3dd8`  
		Last Modified: Wed, 17 Nov 2021 19:19:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cff4a558af0642405c8aec1556aebdbaf4c9a86c0632d964e532934f76466c`  
		Last Modified: Thu, 18 Nov 2021 00:43:12 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700278801433da9ce13b80f7e86e2e5368cccf0e303e9862c537a154f05a540a`  
		Last Modified: Thu, 18 Nov 2021 00:43:36 GMT  
		Size: 95.7 MB (95702657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af28efd287aeb351d175e3c0f5ed184fa551cd1af7172bb7791a60a0537af9de`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8937baf10e23d531e21069ea81323b01572eee4aed6f64640685bb7ffaab8`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eb84ecf78a6f2698456d871cbe794d0bb45a6cece674d3d8251894cb1c1a01`  
		Last Modified: Thu, 18 Nov 2021 00:43:11 GMT  
		Size: 3.1 MB (3063250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676ab58b071fabf24debb26ce72f971b94290b362f51e44b6a19c2fe9b3371a9`  
		Last Modified: Thu, 18 Nov 2021 00:43:18 GMT  
		Size: 43.7 MB (43654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940c5fbe3e6915f01902f8855bf33b917442025553bce6ff1b11353827a7b58`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; ppc64le

```console
$ docker pull redmine@sha256:bc9e80acf291615ffb33dbb7ddbc4a7565d1de7ea50ce44aa4333ba6d433e342
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218955951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cacd26122b566b805c31159146c851de24b306f5db8b8302285459e98d9913b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 03:30:22 GMT
ADD file:c0f8b5d4d419bef7a494df5330ecf7bbea3cbb6462308ca0b2f26771f125dea0 in / 
# Wed, 17 Nov 2021 03:30:29 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:17:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 13:17:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 13:56:53 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 13:56:56 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 13:56:58 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 14:03:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 14:03:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 14:03:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 14:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 14:03:22 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 14:03:24 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 12:26:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 12:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 12:29:27 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 12:29:33 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 12:29:36 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 12:29:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 12:29:46 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 12:29:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 12:29:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 12:33:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 12:34:04 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 12:34:05 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 12:34:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 12:34:08 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 12:34:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:459de0a111d5c931674a5150ef4ae6bb1ffb1685380f4aafdba04a37d556c5de`  
		Last Modified: Wed, 17 Nov 2021 03:58:14 GMT  
		Size: 30.6 MB (30562278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4a8cb8add512175dbaeb682e1d37722eb039847e94d43b2c548f6bf9f4566`  
		Last Modified: Wed, 17 Nov 2021 14:30:35 GMT  
		Size: 12.7 MB (12705482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02accf8c69e0fb54236daa23b1409d80e215845f8d744672e8be1de6353c73f4`  
		Last Modified: Wed, 17 Nov 2021 14:30:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437d94d7e24e0cdbb2879c03363f9b475da2c6828f1d6efd64e6ace62304f455`  
		Last Modified: Wed, 17 Nov 2021 14:34:16 GMT  
		Size: 15.0 MB (14997053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b39e4205e8291bddd16d32f0575a50d2838f1141cdb3dfe1e4502de89dbb1bc`  
		Last Modified: Wed, 17 Nov 2021 14:34:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57265642992f45aec31dcaf12b72927b3e6854aae997a3fd18e7bda9b690b4d`  
		Last Modified: Thu, 18 Nov 2021 12:53:53 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27021a17b8f3615fdf08ab3a986a106ed0d9e0238da2792c9469b5fc2aa38b18`  
		Last Modified: Thu, 18 Nov 2021 12:54:12 GMT  
		Size: 101.3 MB (101327196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9324734dc2a75f7aa6a9f8488945f3181ad665697ef6c85255ff8ab2ebf892f7`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596f052e5e4de085618e67aac634fafdbd606e08d0d7f9f5017875238164e5a8`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c13ff8c3199f6a072a472251f1deeddc585eea60ad17ea7b97b08c06734d2`  
		Last Modified: Thu, 18 Nov 2021 12:53:51 GMT  
		Size: 3.1 MB (3063249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3621788bcdb3caeb1153a2622168e546f76b07dd3cc425b4bb733bbbc94d097`  
		Last Modified: Thu, 18 Nov 2021 12:53:58 GMT  
		Size: 56.3 MB (56296448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5cd3a2223e6188ca96341a558e604ad5bfecb69d6e230c836d280401865d7`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4.2.3` - linux; s390x

```console
$ docker pull redmine@sha256:49a1c1b85f8ccd222764c18d3694feaf0642800543699062e12064d13fecc636
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201879289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd54a6734cf67e04ecc514a8756a628f6b402e434e592dc8d1bf2a75b15627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:37:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:37:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:37:16 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:31:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:32:10 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:32:10 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:32:10 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:32:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 20:32:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:34:07 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:34:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:34:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:34:08 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:34:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa70e45053269d04d1a7217aca754f0b1fd37826bacef60c3e79535af03de7e`  
		Last Modified: Wed, 17 Nov 2021 09:50:18 GMT  
		Size: 14.7 MB (14697150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6665bc1be788124ffa49dc9aca2a874932441c39767aac3628a05b46b7f808`  
		Last Modified: Wed, 17 Nov 2021 09:50:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ad94a5ab88cff035b5e7ab928b3855131115a475ac3f69d13d3b648539b059`  
		Last Modified: Wed, 17 Nov 2021 20:39:22 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef81635c9981af53c3728bbbdf8957635a0b7afccb029ae985a6fe7e6ae527`  
		Last Modified: Wed, 17 Nov 2021 20:39:34 GMT  
		Size: 91.8 MB (91791039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8be6a475176385654d74664b9bc12bade950866233a6eb369175876849a61a9`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d214f8c5411f63986c0d7ee3a9032324738c7b89be0432e0ff9616a27a72485f`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a849b87f96d4317e30bb0352a51b94195d07907f8535be33300f0452e6808655`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05a462fbf41e321955f3c91b6791ba04c37145f855bda5355c75973c4705c2`  
		Last Modified: Wed, 17 Nov 2021 20:39:25 GMT  
		Size: 55.7 MB (55739301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740e646b3a43cb2398040cad7d9e0ed87da62a1457bd92bcc4d0c5a0b8be27c`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2.3-alpine`

```console
$ docker pull redmine@sha256:cf4ec4d559c84d289809ddc6554057e6522d3720200a340c70ba098c12202c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2.3-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:518ba4effd92c427ef19922743eea649ed001436d8a66fe0de469abb2de00949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149044368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a04de41bf1795abeee36effc817551b3de5069209d3ec827816281c81211a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_MAJOR=2.7
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_VERSION=2.7.4
# Sat, 13 Nov 2021 06:44:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Sat, 13 Nov 2021 06:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:47:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:47:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:47:56 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:28:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:29:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:29:07 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:29:08 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:29:08 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_VERSION=4.2.3
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Sat, 13 Nov 2021 14:29:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:29:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:31:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:31:21 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:31:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:31:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:31:22 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:31:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e81c0605571c3961987ae1ce872ebef2b5bcb439010c194e90b47282556c32d`  
		Last Modified: Sat, 13 Nov 2021 06:58:25 GMT  
		Size: 14.0 MB (13994126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2814005984530d27bc89e1c810fb8cb01371038a28bc3d85a1e95b710d9e043e`  
		Last Modified: Sat, 13 Nov 2021 06:58:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171914095295d927972128e1f66156ce389cb697d40fc6d7ea68c919861015e`  
		Last Modified: Sat, 13 Nov 2021 14:36:45 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9802858485f172f49a49aa23ebc2ef97aa9a7dff598d4d6b18f27e107ae24436`  
		Last Modified: Sat, 13 Nov 2021 14:36:55 GMT  
		Size: 69.5 MB (69548252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5b29e3b352df46dbdcf96478507ab2ace06abee4b91e86cea6852a73067d98`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd79647c11e0ebdbaa7b41c71d969403768f7950e69f1b9eda5545fe42e86b3`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20504c29a1f01e91c83c2e1e82a90fb05c118bbf74d44fa621ec588a179bce4b`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 3.1 MB (3064272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7d43b9df6162fdd2b107724ff288c851a49738e7e04fa16cd34fddde661b04`  
		Last Modified: Sat, 13 Nov 2021 14:36:48 GMT  
		Size: 56.0 MB (56029256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561c4b4d66001dcdc5ff09131812075d6a6d4f6430e175565724033921e826f1`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:4.2.3-passenger`

```console
$ docker pull redmine@sha256:1d213433b63a0ead8a70d021a5c132c60e4e748bbc9ca9a924df306b70f3244c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4.2.3-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:e18a6ae0dcfc40dd6410992648ef1012830deff650ee75fe39dbfe061d12a342
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220974188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27853838e5a87da41ee207d9032436259a01c1e6474419f2c9c796931a4c34eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:32:12 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 23:34:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:34:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:35:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:35:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:30:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:31:12 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:31:12 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:31:12 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:31:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:31:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:32:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:01 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:32:01 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:32:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:32:01 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:32:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 18 Nov 2021 20:32:05 GMT
ENV PASSENGER_VERSION=6.0.12
# Thu, 18 Nov 2021 20:32:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:22 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 18 Nov 2021 20:32:23 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 18 Nov 2021 20:32:23 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90b12affd87b4d38a8fcc325810d1d00be3ab2e7bcd8190a9c00b84593c078d`  
		Last Modified: Wed, 17 Nov 2021 23:52:50 GMT  
		Size: 14.5 MB (14510130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8d736be43fd318e714161260dcdb9952dad0c90be69d5376da0b7966ffc5a8`  
		Last Modified: Wed, 17 Nov 2021 23:52:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3019ede46444af81796abfe67c49e2fbabb9db7caeae19ac3c3af640d51440`  
		Last Modified: Thu, 18 Nov 2021 20:37:49 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f459f77e5a0c1928192bf809bbd6e9bb46b6ba4ab21a817e21f49658d9a33d`  
		Last Modified: Thu, 18 Nov 2021 20:38:03 GMT  
		Size: 94.1 MB (94089001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8ef100ec39cd24ccf9e86757ced4ffc4872d201ef840683fa0d01bbd478b2f`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676f59fd8e0144196b1551c4862751c016db7e7bd85d9c5ea7f47fd931c64aa`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d506c2d549b6dae794e30276395ea85c0e257a4c3afb861eee7a80aca20209`  
		Last Modified: Thu, 18 Nov 2021 20:37:47 GMT  
		Size: 3.1 MB (3063251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82700c911def9390d43716a8985c018ac47b62ef650f69a942d86a03fd4510ec`  
		Last Modified: Thu, 18 Nov 2021 20:37:51 GMT  
		Size: 43.4 MB (43425778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0cd4260e9359c26c12c25c14dcf660812c0bd324b62fc86c3f52dca359a33a`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b65724c681012a606e5d41cfbe37546052cd471086212e239e21a5dfbdadaa1`  
		Last Modified: Thu, 18 Nov 2021 20:38:23 GMT  
		Size: 21.2 MB (21238341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916ee64f10c4bd1e7cf1bfcadb56aba80a65c2b1193197e39b1fa3be4829a355`  
		Last Modified: Thu, 18 Nov 2021 20:38:20 GMT  
		Size: 4.9 MB (4924617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:alpine`

```console
$ docker pull redmine@sha256:cf4ec4d559c84d289809ddc6554057e6522d3720200a340c70ba098c12202c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:518ba4effd92c427ef19922743eea649ed001436d8a66fe0de469abb2de00949
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149044368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a04de41bf1795abeee36effc817551b3de5069209d3ec827816281c81211a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:28:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 13 Nov 2021 06:28:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 13 Nov 2021 06:28:18 GMT
ENV LANG=C.UTF-8
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_MAJOR=2.7
# Sat, 13 Nov 2021 06:44:36 GMT
ENV RUBY_VERSION=2.7.4
# Sat, 13 Nov 2021 06:44:37 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Sat, 13 Nov 2021 06:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 13 Nov 2021 06:47:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Nov 2021 06:47:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:47:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 13 Nov 2021 06:47:56 GMT
CMD ["irb"]
# Sat, 13 Nov 2021 14:28:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 13 Nov 2021 14:29:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 13 Nov 2021 14:29:07 GMT
ENV RAILS_ENV=production
# Sat, 13 Nov 2021 14:29:08 GMT
WORKDIR /usr/src/redmine
# Sat, 13 Nov 2021 14:29:08 GMT
ENV HOME=/home/redmine
# Sat, 13 Nov 2021 14:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_VERSION=4.2.3
# Sat, 13 Nov 2021 14:29:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Sat, 13 Nov 2021 14:29:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 13 Nov 2021 14:29:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 13 Nov 2021 14:31:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 13 Nov 2021 14:31:21 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 13 Nov 2021 14:31:22 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 13 Nov 2021 14:31:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 14:31:22 GMT
EXPOSE 3000
# Sat, 13 Nov 2021 14:31:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86e849bc66e37f2d898daa44d76330256a48635f1100e364c0f46206fca7b71`  
		Last Modified: Sat, 13 Nov 2021 06:56:48 GMT  
		Size: 3.6 MB (3582307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a2fc84ba5b32bce31936a6fdf8121f29d2eb485f8525795df7d32046e9f856`  
		Last Modified: Sat, 13 Nov 2021 06:56:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e81c0605571c3961987ae1ce872ebef2b5bcb439010c194e90b47282556c32d`  
		Last Modified: Sat, 13 Nov 2021 06:58:25 GMT  
		Size: 14.0 MB (13994126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2814005984530d27bc89e1c810fb8cb01371038a28bc3d85a1e95b710d9e043e`  
		Last Modified: Sat, 13 Nov 2021 06:58:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e171914095295d927972128e1f66156ce389cb697d40fc6d7ea68c919861015e`  
		Last Modified: Sat, 13 Nov 2021 14:36:45 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9802858485f172f49a49aa23ebc2ef97aa9a7dff598d4d6b18f27e107ae24436`  
		Last Modified: Sat, 13 Nov 2021 14:36:55 GMT  
		Size: 69.5 MB (69548252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5b29e3b352df46dbdcf96478507ab2ace06abee4b91e86cea6852a73067d98`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd79647c11e0ebdbaa7b41c71d969403768f7950e69f1b9eda5545fe42e86b3`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20504c29a1f01e91c83c2e1e82a90fb05c118bbf74d44fa621ec588a179bce4b`  
		Last Modified: Sat, 13 Nov 2021 14:36:43 GMT  
		Size: 3.1 MB (3064272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7d43b9df6162fdd2b107724ff288c851a49738e7e04fa16cd34fddde661b04`  
		Last Modified: Sat, 13 Nov 2021 14:36:48 GMT  
		Size: 56.0 MB (56029256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561c4b4d66001dcdc5ff09131812075d6a6d4f6430e175565724033921e826f1`  
		Last Modified: Sat, 13 Nov 2021 14:36:42 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:latest`

```console
$ docker pull redmine@sha256:6654dea65d5e39a0419ac63df0e0ad6331f5da0f7831043663eca917fb5d3eea
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
$ docker pull redmine@sha256:68e8092f1d13c3e52d3aa807f7c0e5d55239fa8e032135a594f8da178b467623
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194811230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f79246dbb550a5674aad1819a04d406d7df4f3a807a5372f24043786984f50`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:32:12 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 23:34:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:34:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:35:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:35:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:30:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:31:12 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:31:12 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:31:12 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:31:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:31:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:32:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:01 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:32:01 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:32:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:32:01 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:32:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90b12affd87b4d38a8fcc325810d1d00be3ab2e7bcd8190a9c00b84593c078d`  
		Last Modified: Wed, 17 Nov 2021 23:52:50 GMT  
		Size: 14.5 MB (14510130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8d736be43fd318e714161260dcdb9952dad0c90be69d5376da0b7966ffc5a8`  
		Last Modified: Wed, 17 Nov 2021 23:52:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3019ede46444af81796abfe67c49e2fbabb9db7caeae19ac3c3af640d51440`  
		Last Modified: Thu, 18 Nov 2021 20:37:49 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f459f77e5a0c1928192bf809bbd6e9bb46b6ba4ab21a817e21f49658d9a33d`  
		Last Modified: Thu, 18 Nov 2021 20:38:03 GMT  
		Size: 94.1 MB (94089001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8ef100ec39cd24ccf9e86757ced4ffc4872d201ef840683fa0d01bbd478b2f`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676f59fd8e0144196b1551c4862751c016db7e7bd85d9c5ea7f47fd931c64aa`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d506c2d549b6dae794e30276395ea85c0e257a4c3afb861eee7a80aca20209`  
		Last Modified: Thu, 18 Nov 2021 20:37:47 GMT  
		Size: 3.1 MB (3063251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82700c911def9390d43716a8985c018ac47b62ef650f69a942d86a03fd4510ec`  
		Last Modified: Thu, 18 Nov 2021 20:37:51 GMT  
		Size: 43.4 MB (43425778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0cd4260e9359c26c12c25c14dcf660812c0bd324b62fc86c3f52dca359a33a`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:bf6bb00f96a0b12b11262fb56ebe66a814137dca38016393734d0cea84d063f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196300195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f73d796e667ea07abd3855ad0147a9bbbb9beb37276b61162547c05961f5059`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:39 GMT
ADD file:e580d4d2066301375327ea51dd8db3af956e5a465495bf09d69d6deec9b0bfae in / 
# Wed, 17 Nov 2021 02:51:40 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 20:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:53:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 20:53:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:30:49 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 21:30:50 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 21:30:50 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 21:35:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 21:35:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 21:35:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 21:35:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:35:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 21:35:11 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 14:36:38 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 14:37:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 14:37:57 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 14:37:57 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 14:37:58 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 14:37:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 14:38:00 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 14:38:00 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 14:38:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 14:43:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 14:43:45 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 14:43:46 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 14:43:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 14:43:47 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 14:43:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dba255a4b166bb02562ca152d0da236ba8f211de5bf9d79e35ee023b1fce203e`  
		Last Modified: Wed, 17 Nov 2021 03:07:41 GMT  
		Size: 24.9 MB (24886310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58fbebb8e6e22b1601002ddb4252e30c3750edfb93b87424f6c1a971c665bf`  
		Last Modified: Wed, 17 Nov 2021 21:59:40 GMT  
		Size: 10.3 MB (10349405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484eb5c97eceafe50be8deba254566cb365fd68cb0baa2e5418ecece614c2728`  
		Last Modified: Wed, 17 Nov 2021 21:59:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8a3180a4fd6dc5eb70d66bd3e4082e4d6a82432c594b34e550d6feab30b262`  
		Last Modified: Wed, 17 Nov 2021 22:04:27 GMT  
		Size: 13.9 MB (13871351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc80340d626dbcb066ecdc739e235877d725bc16934f56afcf1f9f7a5b1823b`  
		Last Modified: Wed, 17 Nov 2021 22:04:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29e7fbae5e92244d8b1ed80457eecf320d173303fdb99245a84599906c7666`  
		Last Modified: Thu, 18 Nov 2021 14:59:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b55931caf7268bdad6b385d5c79741a8a295c347cfb9fd8f639d1ba7c2a8d8`  
		Last Modified: Thu, 18 Nov 2021 15:00:15 GMT  
		Size: 89.6 MB (89577773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070f8378574f87a9aef84e45e5adeb05df20f39cb6d6d897df940e984084c75`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a18cbf12df5da376627c3bdee43d3813e66f035f637a7c2501f73ad4a1ba60`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2a5a07dcbabe1e7be1e52efada576b24511465600e52c6d7d19effc57d263`  
		Last Modified: Thu, 18 Nov 2021 14:59:15 GMT  
		Size: 3.1 MB (3063252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f00725466b5aef82f5484942c445b1712ba8af31b3158af20834ea48204588`  
		Last Modified: Thu, 18 Nov 2021 14:59:35 GMT  
		Size: 54.5 MB (54547862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49a55ad2f42152245a2269b8f870edac4fcbd328d63a8d72a3da64e94478c59`  
		Last Modified: Thu, 18 Nov 2021 14:59:11 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:c92262d9b7966c7a14f0ca89c5545aa12583798740b923fa82f9025a40c1f246
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189440908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054a0dc932e7b49f5a55f646fb5d28485df4f2de75bff349cec7e7934c0fb639`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:46 GMT
ADD file:4ac0de0d740f0c221cd4f912861a67009942fa5bdad24ac8b62c690dfa15024a in / 
# Wed, 17 Nov 2021 02:00:47 GMT
CMD ["bash"]
# Thu, 18 Nov 2021 08:17:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:17:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 18 Nov 2021 08:17:06 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 08:53:42 GMT
ENV RUBY_MAJOR=2.7
# Thu, 18 Nov 2021 08:53:42 GMT
ENV RUBY_VERSION=2.7.4
# Thu, 18 Nov 2021 08:53:43 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Thu, 18 Nov 2021 08:57:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 18 Nov 2021 08:57:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Nov 2021 08:57:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Nov 2021 08:57:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 08:57:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 18 Nov 2021 08:57:49 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 19:59:23 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:00:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:00:29 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:00:30 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:00:30 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:00:32 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:00:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:00:38 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:05:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:05:55 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:05:56 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:05:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:05:57 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:05:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7bd9e64406c6f3044bd15f89c367f07ec4eaafb1035a5c3ee2f7b138be68017f`  
		Last Modified: Wed, 17 Nov 2021 02:16:39 GMT  
		Size: 22.8 MB (22754359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8e57706e11dcf2202a1ed28d022f7fe3daa306f06bf5311fee3d20b17f772`  
		Last Modified: Thu, 18 Nov 2021 09:24:19 GMT  
		Size: 9.9 MB (9872912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad345207fbbb28e02d7546fe9ec9b203219b39a7b6fe1a2c55d63e665ce8dd`  
		Last Modified: Thu, 18 Nov 2021 09:24:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d25e541e934fefcd6dcfff4226d06801527c28c5f31506d802ed03121e1320b`  
		Last Modified: Thu, 18 Nov 2021 09:29:28 GMT  
		Size: 13.8 MB (13767299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3459bd8cf29be58005e7ad4da22bdba7402a2d607ca5295fe58bac3d98f3b4`  
		Last Modified: Thu, 18 Nov 2021 09:29:21 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9465b374f5ec3e1d43e6b89b84be958e52aaf49669b4e1bbcb2f7bde6546969`  
		Last Modified: Thu, 18 Nov 2021 20:20:44 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f9e4f806a27273fd0d86a752ec0c68d34f29a4e216ac255ea3b98c2f8dee89`  
		Last Modified: Thu, 18 Nov 2021 20:21:39 GMT  
		Size: 85.6 MB (85589945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c32930c81becf489baf6eb5aa96cbcab402cc72b77824a8d5f3ef1164e827e`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874cebd85eed66ba44ad4ac91fc7a5c904705679507db88675f20541e50a55f5`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd024f80cae41f24e51ccb8fe006e4561cd72d216a72741b11521e70ecc17f`  
		Last Modified: Thu, 18 Nov 2021 20:20:46 GMT  
		Size: 3.1 MB (3063253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126ddc84607a7f4665334e4c31b9dd59b1ba40a30a55fb387506edc020bb2c24`  
		Last Modified: Thu, 18 Nov 2021 20:21:06 GMT  
		Size: 54.4 MB (54388903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2cac2bcb44446a910b068386b9b7b82991cd1aed0cea1e34f6e772c6711ba5`  
		Last Modified: Thu, 18 Nov 2021 20:20:42 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:86d444c24d077794c0c2cc949e49527863c9ca44e518c17e370b02eb4000216a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202113715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42218f16d6dac2e546b0a2281ab4659b776bbf51ec6e4acfbede94911bc9dcdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:44 GMT
ADD file:b7921dd77c7620d46a18a4b5952557620210bf7ad9de20fe8e695a371188122a in / 
# Wed, 17 Nov 2021 02:40:44 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:31:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:31:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:41:19 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:41:20 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:41:21 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:43:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:43:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:43:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:43:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:43:17 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 19:46:13 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 19:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:46:40 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 19:46:41 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 19:46:42 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 19:46:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 19:46:44 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 19:46:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 19:46:50 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 19:49:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 19:49:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 19:49:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 19:49:40 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 19:49:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8ccb9871ed7bebcea8889b08e06fe5bd0116711ca7b110429b987475bf4d40e8`  
		Last Modified: Wed, 17 Nov 2021 02:48:07 GMT  
		Size: 25.9 MB (25923117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443a8ec909433d7156b8dcbeaf77f4e53d6a44b253a3f03b95126547154d55`  
		Last Modified: Wed, 17 Nov 2021 09:51:43 GMT  
		Size: 11.3 MB (11261808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f57122fa0ffe176f788d35a4a8f12a76819fa3bab198ac16e26d2961047a1d`  
		Last Modified: Wed, 17 Nov 2021 09:51:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e74dfb7a4c0fdaf06af6628a5256217d8dc0d66250a1fbc0c123f00b986e22`  
		Last Modified: Wed, 17 Nov 2021 09:53:40 GMT  
		Size: 14.1 MB (14143923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb526ffb8eba3317294cf51375a464a78d261132b6b7491f254cf7a4a156682`  
		Last Modified: Wed, 17 Nov 2021 09:53:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21518ac2e5bab0f6dfc5e5d56cc37c2ddfe56b2be0f94f479a28844eda6b01df`  
		Last Modified: Wed, 17 Nov 2021 19:56:25 GMT  
		Size: 1.6 KB (1626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76248d3153c26ceb5416c50118694725c0c7d4ce7823824bd66101dc2c5a010d`  
		Last Modified: Wed, 17 Nov 2021 19:56:41 GMT  
		Size: 92.6 MB (92614747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31701ff7128027b1906c22a7653245cdb3cfac2d03494df00e25be248e743991`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac4b0eb26c86bcfc93c2657dfbeb8e1d3ef40e8785866c46e13be70741ec74b`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62ad39d6bc57963dc25a1ff3af302f01bf0d29bf1d984b097d829bcef8e71d3`  
		Last Modified: Wed, 17 Nov 2021 19:56:24 GMT  
		Size: 3.1 MB (3063387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c77a0ff1cda155087e0a1fd87440c1fd1f0de88ddcd0f7b027500ca9b1c5df9`  
		Last Modified: Wed, 17 Nov 2021 19:56:31 GMT  
		Size: 55.1 MB (55102701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe9431487572557c36e17868ec1e44d823b725205b047bd9b29f8cb63fea74`  
		Last Modified: Wed, 17 Nov 2021 19:56:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:541bbc59f1f2165794af255e943fd64e76f231e68941d6e893fb057442a80b34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201449024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8a65a7d03b8eef85a6b4790bedd723f2249542a83c9e248f86e8bfe4ab2be`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:22 GMT
ADD file:2adea3474b7ebda2bf77361304ee3e6966a9118aafd8220b81c4027be1f4d583 in / 
# Wed, 17 Nov 2021 02:40:22 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 18:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:38:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 18:38:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 18:58:22 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 18:58:23 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 19:02:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 19:02:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 19:02:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 19:02:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 19:02:53 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 00:36:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 00:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 00:36:42 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 00:36:42 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 00:36:42 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 00:36:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 00:36:43 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 00:36:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 00:36:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 00:37:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 00:37:43 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 00:37:43 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 00:37:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 00:37:44 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 00:37:44 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7af5c9e671306e395c50a515c7bbe33d6f418ea08535b01c884457f78114eb08`  
		Last Modified: Wed, 17 Nov 2021 02:48:49 GMT  
		Size: 27.8 MB (27804550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1742b7e5e1e5bca675e7f251c9f6fe8778a1bb1548e5b418f8547277f14e2e33`  
		Last Modified: Wed, 17 Nov 2021 19:17:19 GMT  
		Size: 17.2 MB (17227026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ef5459771b89c49219d5c15641c7215faf156712422f01efee40ad955a52c5`  
		Last Modified: Wed, 17 Nov 2021 19:17:10 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59002f4fc409c3fdcbd829fcc8f9d9186a49f4b1977b2c959714978bd07c75`  
		Last Modified: Wed, 17 Nov 2021 19:19:42 GMT  
		Size: 14.0 MB (13992752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1a3cc73f29df585791125514b63252077c65f4a1e212d1021c4e3020df3dd8`  
		Last Modified: Wed, 17 Nov 2021 19:19:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cff4a558af0642405c8aec1556aebdbaf4c9a86c0632d964e532934f76466c`  
		Last Modified: Thu, 18 Nov 2021 00:43:12 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700278801433da9ce13b80f7e86e2e5368cccf0e303e9862c537a154f05a540a`  
		Last Modified: Thu, 18 Nov 2021 00:43:36 GMT  
		Size: 95.7 MB (95702657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af28efd287aeb351d175e3c0f5ed184fa551cd1af7172bb7791a60a0537af9de`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8937baf10e23d531e21069ea81323b01572eee4aed6f64640685bb7ffaab8`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eb84ecf78a6f2698456d871cbe794d0bb45a6cece674d3d8251894cb1c1a01`  
		Last Modified: Thu, 18 Nov 2021 00:43:11 GMT  
		Size: 3.1 MB (3063250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676ab58b071fabf24debb26ce72f971b94290b362f51e44b6a19c2fe9b3371a9`  
		Last Modified: Thu, 18 Nov 2021 00:43:18 GMT  
		Size: 43.7 MB (43654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940c5fbe3e6915f01902f8855bf33b917442025553bce6ff1b11353827a7b58`  
		Last Modified: Thu, 18 Nov 2021 00:43:09 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:bc9e80acf291615ffb33dbb7ddbc4a7565d1de7ea50ce44aa4333ba6d433e342
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218955951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cacd26122b566b805c31159146c851de24b306f5db8b8302285459e98d9913b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 03:30:22 GMT
ADD file:c0f8b5d4d419bef7a494df5330ecf7bbea3cbb6462308ca0b2f26771f125dea0 in / 
# Wed, 17 Nov 2021 03:30:29 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:17:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:17:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 13:17:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 13:56:53 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 13:56:56 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 13:56:58 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 14:03:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 14:03:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 14:03:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 14:03:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 14:03:22 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 14:03:24 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 12:26:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 12:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 12:29:27 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 12:29:33 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 12:29:36 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 12:29:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 12:29:46 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 12:29:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 12:29:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 12:33:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 12:34:04 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 12:34:05 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 12:34:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 12:34:08 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 12:34:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:459de0a111d5c931674a5150ef4ae6bb1ffb1685380f4aafdba04a37d556c5de`  
		Last Modified: Wed, 17 Nov 2021 03:58:14 GMT  
		Size: 30.6 MB (30562278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e4a8cb8add512175dbaeb682e1d37722eb039847e94d43b2c548f6bf9f4566`  
		Last Modified: Wed, 17 Nov 2021 14:30:35 GMT  
		Size: 12.7 MB (12705482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02accf8c69e0fb54236daa23b1409d80e215845f8d744672e8be1de6353c73f4`  
		Last Modified: Wed, 17 Nov 2021 14:30:32 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437d94d7e24e0cdbb2879c03363f9b475da2c6828f1d6efd64e6ace62304f455`  
		Last Modified: Wed, 17 Nov 2021 14:34:16 GMT  
		Size: 15.0 MB (14997053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b39e4205e8291bddd16d32f0575a50d2838f1141cdb3dfe1e4502de89dbb1bc`  
		Last Modified: Wed, 17 Nov 2021 14:34:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57265642992f45aec31dcaf12b72927b3e6854aae997a3fd18e7bda9b690b4d`  
		Last Modified: Thu, 18 Nov 2021 12:53:53 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27021a17b8f3615fdf08ab3a986a106ed0d9e0238da2792c9469b5fc2aa38b18`  
		Last Modified: Thu, 18 Nov 2021 12:54:12 GMT  
		Size: 101.3 MB (101327196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9324734dc2a75f7aa6a9f8488945f3181ad665697ef6c85255ff8ab2ebf892f7`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596f052e5e4de085618e67aac634fafdbd606e08d0d7f9f5017875238164e5a8`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c13ff8c3199f6a072a472251f1deeddc585eea60ad17ea7b97b08c06734d2`  
		Last Modified: Thu, 18 Nov 2021 12:53:51 GMT  
		Size: 3.1 MB (3063249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3621788bcdb3caeb1153a2622168e546f76b07dd3cc425b4bb733bbbc94d097`  
		Last Modified: Thu, 18 Nov 2021 12:53:58 GMT  
		Size: 56.3 MB (56296448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5cd3a2223e6188ca96341a558e604ad5bfecb69d6e230c836d280401865d7`  
		Last Modified: Thu, 18 Nov 2021 12:53:50 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:49a1c1b85f8ccd222764c18d3694feaf0642800543699062e12064d13fecc636
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201879289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd54a6734cf67e04ecc514a8756a628f6b402e434e592dc8d1bf2a75b15627`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:59 GMT
ADD file:3ff5fbc9c53cf76aad0fe0e1a525cb0bc0d70e8f2a3d5741dfb8b3b8a9448ffd in / 
# Wed, 17 Nov 2021 02:43:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:21:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 09:21:07 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 09:35:52 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 09:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 09:37:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 09:37:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:37:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 09:37:16 GMT
CMD ["irb"]
# Wed, 17 Nov 2021 20:31:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 17 Nov 2021 20:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:32:10 GMT
ENV RAILS_ENV=production
# Wed, 17 Nov 2021 20:32:10 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Nov 2021 20:32:10 GMT
ENV HOME=/home/redmine
# Wed, 17 Nov 2021 20:32:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_VERSION=4.2.3
# Wed, 17 Nov 2021 20:32:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Wed, 17 Nov 2021 20:32:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 17 Nov 2021 20:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Nov 2021 20:34:07 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Nov 2021 20:34:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 17 Nov 2021 20:34:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Nov 2021 20:34:08 GMT
EXPOSE 3000
# Wed, 17 Nov 2021 20:34:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b8b917e61b3be882db10e68210f73caf5cc788bfb07aec0a659e30f4796b476b`  
		Last Modified: Wed, 17 Nov 2021 02:49:01 GMT  
		Size: 25.8 MB (25769063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e574c6d046371657ec033b78bc3df865890056f711b30df7505d0128446e36`  
		Last Modified: Wed, 17 Nov 2021 09:48:11 GMT  
		Size: 10.8 MB (10815243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bfb1613df50da70222f9b1cd395c4b509f6e6631cf6a13ce6c6b9c8c4cf181`  
		Last Modified: Wed, 17 Nov 2021 09:48:09 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa70e45053269d04d1a7217aca754f0b1fd37826bacef60c3e79535af03de7e`  
		Last Modified: Wed, 17 Nov 2021 09:50:18 GMT  
		Size: 14.7 MB (14697150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6665bc1be788124ffa49dc9aca2a874932441c39767aac3628a05b46b7f808`  
		Last Modified: Wed, 17 Nov 2021 09:50:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ad94a5ab88cff035b5e7ab928b3855131115a475ac3f69d13d3b648539b059`  
		Last Modified: Wed, 17 Nov 2021 20:39:22 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef81635c9981af53c3728bbbdf8957635a0b7afccb029ae985a6fe7e6ae527`  
		Last Modified: Wed, 17 Nov 2021 20:39:34 GMT  
		Size: 91.8 MB (91791039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8be6a475176385654d74664b9bc12bade950866233a6eb369175876849a61a9`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d214f8c5411f63986c0d7ee3a9032324738c7b89be0432e0ff9616a27a72485f`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a849b87f96d4317e30bb0352a51b94195d07907f8535be33300f0452e6808655`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 3.1 MB (3063246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05a462fbf41e321955f3c91b6791ba04c37145f855bda5355c75973c4705c2`  
		Last Modified: Wed, 17 Nov 2021 20:39:25 GMT  
		Size: 55.7 MB (55739301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740e646b3a43cb2398040cad7d9e0ed87da62a1457bd92bcc4d0c5a0b8be27c`  
		Last Modified: Wed, 17 Nov 2021 20:39:21 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:passenger`

```console
$ docker pull redmine@sha256:1d213433b63a0ead8a70d021a5c132c60e4e748bbc9ca9a924df306b70f3244c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:passenger` - linux; amd64

```console
$ docker pull redmine@sha256:e18a6ae0dcfc40dd6410992648ef1012830deff650ee75fe39dbfe061d12a342
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220974188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27853838e5a87da41ee207d9032436259a01c1e6474419f2c9c796931a4c34eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 23:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 23:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 17 Nov 2021 23:05:39 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 23:32:12 GMT
ENV RUBY_MAJOR=2.7
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 17 Nov 2021 23:32:13 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 17 Nov 2021 23:34:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 17 Nov 2021 23:34:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Nov 2021 23:35:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 23:35:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 17 Nov 2021 23:35:01 GMT
CMD ["irb"]
# Thu, 18 Nov 2021 20:30:43 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 18 Nov 2021 20:31:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 20:31:12 GMT
ENV RAILS_ENV=production
# Thu, 18 Nov 2021 20:31:12 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Nov 2021 20:31:12 GMT
ENV HOME=/home/redmine
# Thu, 18 Nov 2021 20:31:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_VERSION=4.2.3
# Thu, 18 Nov 2021 20:31:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Thu, 18 Nov 2021 20:31:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 18 Nov 2021 20:32:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:01 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Nov 2021 20:32:01 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 18 Nov 2021 20:32:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Nov 2021 20:32:01 GMT
EXPOSE 3000
# Thu, 18 Nov 2021 20:32:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 18 Nov 2021 20:32:05 GMT
ENV PASSENGER_VERSION=6.0.12
# Thu, 18 Nov 2021 20:32:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 18 Nov 2021 20:32:22 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 18 Nov 2021 20:32:23 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 18 Nov 2021 20:32:23 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d04e01f945ee4b2edd0451f178f17023c43f67737d0372eb309e5c83b9bc3e0`  
		Last Modified: Wed, 17 Nov 2021 23:49:59 GMT  
		Size: 12.6 MB (12565151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8272911037384bdfabca8cbdd7eebb7290e527e81caa0a3f775b71d09b39ca4e`  
		Last Modified: Wed, 17 Nov 2021 23:49:56 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90b12affd87b4d38a8fcc325810d1d00be3ab2e7bcd8190a9c00b84593c078d`  
		Last Modified: Wed, 17 Nov 2021 23:52:50 GMT  
		Size: 14.5 MB (14510130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8d736be43fd318e714161260dcdb9952dad0c90be69d5376da0b7966ffc5a8`  
		Last Modified: Wed, 17 Nov 2021 23:52:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3019ede46444af81796abfe67c49e2fbabb9db7caeae19ac3c3af640d51440`  
		Last Modified: Thu, 18 Nov 2021 20:37:49 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f459f77e5a0c1928192bf809bbd6e9bb46b6ba4ab21a817e21f49658d9a33d`  
		Last Modified: Thu, 18 Nov 2021 20:38:03 GMT  
		Size: 94.1 MB (94089001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8ef100ec39cd24ccf9e86757ced4ffc4872d201ef840683fa0d01bbd478b2f`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676f59fd8e0144196b1551c4862751c016db7e7bd85d9c5ea7f47fd931c64aa`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d506c2d549b6dae794e30276395ea85c0e257a4c3afb861eee7a80aca20209`  
		Last Modified: Thu, 18 Nov 2021 20:37:47 GMT  
		Size: 3.1 MB (3063251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82700c911def9390d43716a8985c018ac47b62ef650f69a942d86a03fd4510ec`  
		Last Modified: Thu, 18 Nov 2021 20:37:51 GMT  
		Size: 43.4 MB (43425778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0cd4260e9359c26c12c25c14dcf660812c0bd324b62fc86c3f52dca359a33a`  
		Last Modified: Thu, 18 Nov 2021 20:37:46 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b65724c681012a606e5d41cfbe37546052cd471086212e239e21a5dfbdadaa1`  
		Last Modified: Thu, 18 Nov 2021 20:38:23 GMT  
		Size: 21.2 MB (21238341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916ee64f10c4bd1e7cf1bfcadb56aba80a65c2b1193197e39b1fa3be4829a355`  
		Last Modified: Thu, 18 Nov 2021 20:38:20 GMT  
		Size: 4.9 MB (4924617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
