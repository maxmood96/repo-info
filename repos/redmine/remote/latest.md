## `redmine:latest`

```console
$ docker pull redmine@sha256:55c56109c1415a85983558f6bbfaf421e98b48c04c974a6c0a38b3a88b7f351d
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
$ docker pull redmine@sha256:9892a7bec09254dbb1601176db7f8d4452a08a4e158c78e735ba2498a9566a5d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195474533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45d6d2ff9872cfb76c5a2c368aa5047e15b65f55f8163d7d4e624f9bdd4c3f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 17:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 17:07:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 17:07:37 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 17:14:10 GMT
ENV RUBY_MAJOR=2.7
# Wed, 07 Jul 2021 19:43:10 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 07 Jul 2021 19:43:10 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 07 Jul 2021 19:45:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 07 Jul 2021 19:45:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Jul 2021 19:45:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Jul 2021 19:45:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jul 2021 19:45:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 07 Jul 2021 19:45:43 GMT
CMD ["irb"]
# Wed, 07 Jul 2021 20:39:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 07 Jul 2021 20:40:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Jul 2021 20:40:35 GMT
ENV RAILS_ENV=production
# Wed, 07 Jul 2021 20:40:35 GMT
WORKDIR /usr/src/redmine
# Wed, 07 Jul 2021 20:40:36 GMT
ENV HOME=/home/redmine
# Wed, 07 Jul 2021 20:40:38 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 07 Jul 2021 20:40:39 GMT
ENV REDMINE_VERSION=4.2.1
# Wed, 07 Jul 2021 20:40:39 GMT
ENV REDMINE_DOWNLOAD_SHA256=ad4109c3425f1cfe4c8961f6ae6494c76e20d81ed946caa1e297d9eda13b41b4
# Wed, 07 Jul 2021 20:40:44 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 07 Jul 2021 20:41:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 07 Jul 2021 20:41:45 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 07 Jul 2021 20:41:45 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 07 Jul 2021 20:41:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Jul 2021 20:41:46 GMT
EXPOSE 3000
# Wed, 07 Jul 2021 20:41:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8edb0654f16a0b0dfa9167e58fdc2d00d20e61f18f10d3e848418baf5bef4ab`  
		Last Modified: Wed, 23 Jun 2021 17:42:38 GMT  
		Size: 12.6 MB (12562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523ba211d3249c13e0f844045a38f32ef8cce47229548262f3503816661e9af`  
		Last Modified: Wed, 23 Jun 2021 17:42:36 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733ec198d0e9805569798ab4a23e68f73a18a3ffd651015186eba5dd9a2ca610`  
		Last Modified: Wed, 07 Jul 2021 20:19:35 GMT  
		Size: 14.5 MB (14508799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e12699933c31f935ddd2fa045f7d982334012d6ad88dd44c3fbadf7a73f5a26`  
		Last Modified: Wed, 07 Jul 2021 20:19:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8339bad2aba6e43a929afc7d8b21af91944756bb66ef66a16e5d828ceb796d51`  
		Last Modified: Wed, 07 Jul 2021 20:59:08 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3220f49d0d115b00cb264590dadd864df879aa3258ee8d5f0144a5d6033dacc2`  
		Last Modified: Wed, 07 Jul 2021 20:59:24 GMT  
		Size: 94.1 MB (94088061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a290764a5ae2660fa1cc94e5aa69717c302b3bcb35daab61321ba461f281b0`  
		Last Modified: Wed, 07 Jul 2021 20:59:06 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3920d04b60ae243eed09f0e406abf35b0c554feba46e0d06d50f7ee4d50dd04`  
		Last Modified: Wed, 07 Jul 2021 20:59:06 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b529c84f2b0c85f9568545c17f99282048191e9439079e1218f4feb0326d82`  
		Last Modified: Wed, 07 Jul 2021 20:59:07 GMT  
		Size: 3.1 MB (3058680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81464e83abe2839f8f7dd0aeadc2876201f9769f84c800c495de9add0af0891a`  
		Last Modified: Wed, 07 Jul 2021 20:59:11 GMT  
		Size: 44.1 MB (44106209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be192e9efc951e43743b5d7b6eef8c89f90d2e19f0791fc1d5f04eaf8e6fa2c9`  
		Last Modified: Wed, 07 Jul 2021 20:59:06 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:e043cc3016fe5e7b5a8795cb6610d132846dc8901cc51f2a70ed6ac574e692e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (196971622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50399e07127157e7c6a32ae5766bdf6b3753a9218a54544773f21e2963a2649d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 22 Jun 2021 23:50:09 GMT
ADD file:78d4ced31112d85490c684f350aceeebfc72a804262c7ad3e033257e3894f5c4 in / 
# Tue, 22 Jun 2021 23:50:11 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 13:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 13:06:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 13:06:50 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 13:17:20 GMT
ENV RUBY_MAJOR=2.7
# Wed, 07 Jul 2021 19:05:54 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 07 Jul 2021 19:05:55 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 07 Jul 2021 19:10:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 07 Jul 2021 19:10:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Jul 2021 19:10:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Jul 2021 19:10:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jul 2021 19:11:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 07 Jul 2021 19:11:03 GMT
CMD ["irb"]
# Wed, 07 Jul 2021 20:40:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 07 Jul 2021 20:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Jul 2021 20:41:50 GMT
ENV RAILS_ENV=production
# Wed, 07 Jul 2021 20:41:51 GMT
WORKDIR /usr/src/redmine
# Wed, 07 Jul 2021 20:41:51 GMT
ENV HOME=/home/redmine
# Wed, 07 Jul 2021 20:41:55 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 07 Jul 2021 20:41:56 GMT
ENV REDMINE_VERSION=4.2.1
# Wed, 07 Jul 2021 20:41:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=ad4109c3425f1cfe4c8961f6ae6494c76e20d81ed946caa1e297d9eda13b41b4
# Wed, 07 Jul 2021 20:42:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 07 Jul 2021 20:47:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 07 Jul 2021 20:47:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 07 Jul 2021 20:47:52 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 07 Jul 2021 20:47:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Jul 2021 20:47:53 GMT
EXPOSE 3000
# Wed, 07 Jul 2021 20:47:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:532d6df30af5174ac6e1b379c32b8f464d44651ac060376a560c4a76a87704a7`  
		Last Modified: Wed, 23 Jun 2021 00:01:46 GMT  
		Size: 24.9 MB (24878945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b3ba0f03212caacd2191837bdac2f1a9abf399938b4020b315e4c6ea7ba0c7`  
		Last Modified: Wed, 23 Jun 2021 14:05:28 GMT  
		Size: 10.3 MB (10345811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cfab7796870f80c9db896239384ac194808f4ce5fab9f16ba155559772cc1e`  
		Last Modified: Wed, 23 Jun 2021 14:05:23 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8de71637799be80e8a1d831a7ec0001438221003f1fba2a0048f0890a3b6754`  
		Last Modified: Wed, 07 Jul 2021 19:39:19 GMT  
		Size: 13.9 MB (13870579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e4e01c697d37bebe10233fa0fd663ff0163be38003be3e3d32d5f55ceedb20`  
		Last Modified: Wed, 07 Jul 2021 19:39:14 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38139f957d7a7631e24469625396df547c9666d5d31bc772eae17ba4dd35240`  
		Last Modified: Wed, 07 Jul 2021 21:04:59 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ceb69ff0274b6d1c938eba7f7c3713ee00dd69cfbc01f2ef55d31e86916056d`  
		Last Modified: Wed, 07 Jul 2021 21:06:03 GMT  
		Size: 89.6 MB (89577397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185956eafe4ab555715545f5cb24caaa7e64c1f289f411990d7a7a41f8497cb5`  
		Last Modified: Wed, 07 Jul 2021 21:04:57 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f12a09bb296b85b224a182ffb781cdbd40f773e9ee06db9af2b5ca76e63f86`  
		Last Modified: Wed, 07 Jul 2021 21:04:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792d14f4fae8cdbd96daa88e2e92565bd3e6193341cf38321ec4dc9f05251d14`  
		Last Modified: Wed, 07 Jul 2021 21:05:00 GMT  
		Size: 3.1 MB (3058681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02baaf29281f3ceac925ae34e596e4a164f193dd363f998e603a9f23c0b2ed7`  
		Last Modified: Wed, 07 Jul 2021 21:05:23 GMT  
		Size: 55.2 MB (55235969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0903ff27a1383a9dd50366ccdda7d4c2173d2fa50f94561474aa63d42701f1ef`  
		Last Modified: Wed, 07 Jul 2021 21:04:57 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:e58b6bd9702e642d2456f4b1fe9be543dfc30e114be4ef1b60049faebd4e7307
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207731256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc0b009665b15d4b25d32f2692a8dbf16f91eea71bff8657ef06e3106cde231`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:31 GMT
ADD file:8d200a3bbe985ff355343675c5555852f27550a9e367969df6bc98034efb8fd4 in / 
# Wed, 23 Jun 2021 00:20:31 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 23:18:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 23:18:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 23:18:54 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 23:36:25 GMT
ENV RUBY_MAJOR=2.7
# Wed, 23 Jun 2021 23:36:25 GMT
ENV RUBY_VERSION=2.7.3
# Wed, 23 Jun 2021 23:36:25 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Wed, 23 Jun 2021 23:40:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 23 Jun 2021 23:40:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 23 Jun 2021 23:40:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 23 Jun 2021 23:40:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 23:40:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 23 Jun 2021 23:40:45 GMT
CMD ["irb"]
# Fri, 25 Jun 2021 02:12:24 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 25 Jun 2021 02:13:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 25 Jun 2021 02:13:27 GMT
ENV RAILS_ENV=production
# Fri, 25 Jun 2021 02:13:27 GMT
WORKDIR /usr/src/redmine
# Fri, 25 Jun 2021 02:13:28 GMT
ENV HOME=/home/redmine
# Fri, 25 Jun 2021 02:13:29 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 25 Jun 2021 02:13:30 GMT
ENV REDMINE_VERSION=4.2.1
# Fri, 25 Jun 2021 02:13:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=ad4109c3425f1cfe4c8961f6ae6494c76e20d81ed946caa1e297d9eda13b41b4
# Fri, 25 Jun 2021 02:13:36 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 25 Jun 2021 02:19:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Jun 2021 02:19:04 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 25 Jun 2021 02:19:04 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Fri, 25 Jun 2021 02:19:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 25 Jun 2021 02:19:05 GMT
EXPOSE 3000
# Fri, 25 Jun 2021 02:19:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8452be1adf00f91570fe21a8e61aaf4c12e014daf67d7de65d984f4e8ecca2f1`  
		Last Modified: Wed, 23 Jun 2021 00:31:49 GMT  
		Size: 22.7 MB (22746055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08b763290fb30bc16e505b4aa06ba1c3041182ac9bd8be48df5e94cbbe8545d`  
		Last Modified: Thu, 24 Jun 2021 00:49:52 GMT  
		Size: 9.9 MB (9872206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f611d0cebec7d01271526d00ff39f508174641d4e952ac4954fb89f368bf331`  
		Last Modified: Thu, 24 Jun 2021 00:49:44 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4da7bdd2f783d5659351604a38b16ab259002f7b13ece71efc8d9cf970b1492`  
		Last Modified: Thu, 24 Jun 2021 00:52:44 GMT  
		Size: 22.0 MB (22018875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb46b7c81ac571c1abab7b7616d01e7bb759441a0a43c309de0e22d1fe62b288`  
		Last Modified: Thu, 24 Jun 2021 00:52:34 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b6fb2f5659e2aa0c0326a59f1be429437d55754f2cf2783fb86039cd9bbacf`  
		Last Modified: Fri, 25 Jun 2021 02:33:51 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985c6089bfd724f8f94bcea07e1c9648f361686cfb1d0b8c3eb7763d5f448ec2`  
		Last Modified: Fri, 25 Jun 2021 02:34:48 GMT  
		Size: 85.6 MB (85590069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803c063a360b224062b9d15434ed5d6a70bce9415644f272995848e3d835ab3`  
		Last Modified: Fri, 25 Jun 2021 02:33:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0459cba97fbf587923c10475008e51aabf2e7d2a20f31171d57c4f71c03c4513`  
		Last Modified: Fri, 25 Jun 2021 02:33:49 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d5dd18bfa24f0af741f94c3f75e887eae54794f9572c5ba45eb46c1bc9f654`  
		Last Modified: Fri, 25 Jun 2021 02:33:53 GMT  
		Size: 3.1 MB (3058688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72232f93d8aea7705263bba64bebc4cc6270cb66dc176bf40e2070289144ae1e`  
		Last Modified: Fri, 25 Jun 2021 02:34:20 GMT  
		Size: 64.4 MB (64441123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9436b7855ede48360f8e6ce2ccb529f08d6fa2202b5ea5155eaaf80d897c178`  
		Last Modified: Fri, 25 Jun 2021 02:33:49 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:0b3399b1ce357a87155ba451f97633a2872431e168768795d1304d5037789d55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221522981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42c79c62438c29c7721838deb724df5be1abb50714e72243d59a266df454487`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:40 GMT
ADD file:beee00b59da720f68e12e2ba2a8134207c80c777ddb4ceb03c71e3e4c3f51c93 in / 
# Tue, 22 Jun 2021 23:49:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 03:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 03:53:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 03:53:54 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 03:58:54 GMT
ENV RUBY_MAJOR=2.7
# Wed, 23 Jun 2021 03:58:54 GMT
ENV RUBY_VERSION=2.7.3
# Wed, 23 Jun 2021 03:58:54 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Wed, 23 Jun 2021 04:01:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 23 Jun 2021 04:01:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 23 Jun 2021 04:01:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 23 Jun 2021 04:01:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 04:01:09 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 23 Jun 2021 04:01:09 GMT
CMD ["irb"]
# Wed, 23 Jun 2021 19:29:44 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 23 Jun 2021 19:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 19:30:09 GMT
ENV RAILS_ENV=production
# Wed, 23 Jun 2021 19:30:09 GMT
WORKDIR /usr/src/redmine
# Wed, 23 Jun 2021 19:30:09 GMT
ENV HOME=/home/redmine
# Wed, 23 Jun 2021 19:30:10 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 23 Jun 2021 19:30:10 GMT
ENV REDMINE_VERSION=4.2.1
# Wed, 23 Jun 2021 19:30:10 GMT
ENV REDMINE_DOWNLOAD_SHA256=ad4109c3425f1cfe4c8961f6ae6494c76e20d81ed946caa1e297d9eda13b41b4
# Wed, 23 Jun 2021 19:30:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 23 Jun 2021 19:32:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 23 Jun 2021 19:32:41 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 23 Jun 2021 19:32:41 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 23 Jun 2021 19:32:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Jun 2021 19:32:42 GMT
EXPOSE 3000
# Wed, 23 Jun 2021 19:32:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:448f6bf000e31217a7c202c659b03b7f8ac8d3ae6b03ef7a2f8339be2f00ff4a`  
		Last Modified: Tue, 22 Jun 2021 23:55:25 GMT  
		Size: 25.9 MB (25914993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f276f053f0cad4dbf0c339099f5dd135531eb3ffb0bccc09369e7b7391b18d72`  
		Last Modified: Wed, 23 Jun 2021 04:22:18 GMT  
		Size: 11.3 MB (11263062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863be1d4664c690cf3e71cf9494c9b590ce4781e8008aef05d7cf572b8feddcc`  
		Last Modified: Wed, 23 Jun 2021 04:22:16 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1761cba6c44390fd8053d1b3f075400cd9986d8db31c38aa3fb675f6abccd7`  
		Last Modified: Wed, 23 Jun 2021 04:23:31 GMT  
		Size: 22.7 MB (22732620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b46f965c91a1a933ac1b0083bad34a4cede3afbd3ed37faaa2d9a4251793373`  
		Last Modified: Wed, 23 Jun 2021 04:23:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c6fa52f2d126b732149df3cd8ec399ac1669185daa700bd6a80f3c7f6ecddc`  
		Last Modified: Wed, 23 Jun 2021 19:38:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269815e6a6e27455198510bf52899b1f343db650f9b4430b86069873617eb76d`  
		Last Modified: Wed, 23 Jun 2021 19:39:00 GMT  
		Size: 92.6 MB (92610233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9772df1f2d5ab051c8521b5c9a1ef56e8557afccefb68c849a60bf39c78547ba`  
		Last Modified: Wed, 23 Jun 2021 19:38:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6f932995fc670c1951ee1113e323dae2285b7016d3f94219ba4c0a88dfd51d`  
		Last Modified: Wed, 23 Jun 2021 19:38:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c691511e9755b9197f34b018ac7515372eae19582e53d4884cf1a89bc0cc0473`  
		Last Modified: Wed, 23 Jun 2021 19:38:42 GMT  
		Size: 3.1 MB (3058682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4015733f4deb74514c0e02a85f7c6de62885ebdcc3ff35800fa5663fc02eea3`  
		Last Modified: Wed, 23 Jun 2021 19:38:50 GMT  
		Size: 65.9 MB (65939146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837d0ceedade85f6f32eaf8f5e43f06ad0c8aa96aaabb1a02280a535cd922d36`  
		Last Modified: Wed, 23 Jun 2021 19:38:41 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:d14cc0404d64845fb66089649ec79ee73b9e9f3e4ef69187e9fdb4a20ef1c596
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202115205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24524c63e7690a1872f7249761ba678bf5dcb905231c387af62d8e90381fbe4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 22 Jun 2021 23:39:35 GMT
ADD file:48f656ac6733911048b3de850490438d0233b3badc11861fca62062d4edfaf40 in / 
# Tue, 22 Jun 2021 23:39:35 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 13:33:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 13:33:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 23 Jun 2021 13:33:25 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 13:42:41 GMT
ENV RUBY_MAJOR=2.7
# Wed, 07 Jul 2021 19:08:54 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 07 Jul 2021 19:08:54 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 07 Jul 2021 19:11:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 07 Jul 2021 19:11:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Jul 2021 19:11:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Jul 2021 19:11:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jul 2021 19:11:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 07 Jul 2021 19:11:20 GMT
CMD ["irb"]
# Wed, 07 Jul 2021 20:21:35 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 07 Jul 2021 20:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Jul 2021 20:22:09 GMT
ENV RAILS_ENV=production
# Wed, 07 Jul 2021 20:22:10 GMT
WORKDIR /usr/src/redmine
# Wed, 07 Jul 2021 20:22:10 GMT
ENV HOME=/home/redmine
# Wed, 07 Jul 2021 20:22:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 07 Jul 2021 20:22:11 GMT
ENV REDMINE_VERSION=4.2.1
# Wed, 07 Jul 2021 20:22:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=ad4109c3425f1cfe4c8961f6ae6494c76e20d81ed946caa1e297d9eda13b41b4
# Wed, 07 Jul 2021 20:22:15 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 07 Jul 2021 20:23:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 07 Jul 2021 20:23:11 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 07 Jul 2021 20:23:12 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Wed, 07 Jul 2021 20:23:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Jul 2021 20:23:12 GMT
EXPOSE 3000
# Wed, 07 Jul 2021 20:23:12 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33af2dcb865e65d53cdeb843b67a0ef62151fa32df292293e7c6b0eb728ac5ac`  
		Last Modified: Tue, 22 Jun 2021 23:46:23 GMT  
		Size: 27.8 MB (27797411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2fb2041b26a9335dbdc8e6cc9bd945661b43317eb0de6d4e1e8ce82275cbea6`  
		Last Modified: Wed, 23 Jun 2021 14:14:04 GMT  
		Size: 17.2 MB (17227420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c89206098d37979fca1f31ba315796953128b80660adc5194c5541f0ac3f34`  
		Last Modified: Wed, 23 Jun 2021 14:13:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341faf4b7bacf87146e1cc8f7b16961e331219a753ec3e63ed3aec770fb56230`  
		Last Modified: Wed, 07 Jul 2021 19:47:38 GMT  
		Size: 14.0 MB (13991269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b2c2e2fdb097bf1d8a5b05a91d5ab0071e6b7e5af7d34e75077617ae628e72`  
		Last Modified: Wed, 07 Jul 2021 19:47:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa2bb952ee73a43f057dc181b823d054447af87094d7a9484baefccf3edef0e`  
		Last Modified: Wed, 07 Jul 2021 20:28:31 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f845132b8f1003fea4b7d9fdf68dd66e3b1c204b268e36c93f52c74046529d82`  
		Last Modified: Wed, 07 Jul 2021 20:28:53 GMT  
		Size: 95.7 MB (95702828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09f141a579b3c57f493228a773bb881646da17e03778d09457da7e1e92e1bd5`  
		Last Modified: Wed, 07 Jul 2021 20:28:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd889ad472e775acbc41d92fcfd65017be7cd09ff253c0a00b21c73255f23c7`  
		Last Modified: Wed, 07 Jul 2021 20:28:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762ed7955684d4b3426f8ae5d53122608b4174c1eae34f08ceba7fb8a48f7292`  
		Last Modified: Wed, 07 Jul 2021 20:28:30 GMT  
		Size: 3.1 MB (3058680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d401c7facc82db166eb4944d64075878c9eab1a8eea6359531949c1a329589`  
		Last Modified: Wed, 07 Jul 2021 20:28:40 GMT  
		Size: 44.3 MB (44333357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f2a976375f0dd2450b1d439cdd9a722920034bffb3cf1b62409d80f308a86d`  
		Last Modified: Wed, 07 Jul 2021 20:28:29 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:53bf5393cee0e13919e154eb387f20fd5eac0d0fceddbbf6089dee4636d268ed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 MB (238093005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462fcd46903f2ec2a5a39fc69101f8b9609214a5bcf3db71283581c53395018e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 23 Jun 2021 00:30:38 GMT
ADD file:e599654230c9fe95fe2c591dbe60e8a0a886cd053b6117230fbae47561145731 in / 
# Wed, 23 Jun 2021 00:30:46 GMT
CMD ["bash"]
# Sat, 26 Jun 2021 13:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Jun 2021 13:53:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 26 Jun 2021 13:53:29 GMT
ENV LANG=C.UTF-8
# Sat, 26 Jun 2021 14:23:20 GMT
ENV RUBY_MAJOR=2.7
# Sat, 26 Jun 2021 14:23:28 GMT
ENV RUBY_VERSION=2.7.3
# Sat, 26 Jun 2021 14:23:32 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Sat, 26 Jun 2021 14:34:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 26 Jun 2021 14:34:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 26 Jun 2021 14:34:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 26 Jun 2021 14:34:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Jun 2021 14:34:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 26 Jun 2021 14:34:46 GMT
CMD ["irb"]
# Sun, 27 Jun 2021 18:01:05 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 27 Jun 2021 18:04:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sun, 27 Jun 2021 18:05:08 GMT
ENV RAILS_ENV=production
# Sun, 27 Jun 2021 18:05:14 GMT
WORKDIR /usr/src/redmine
# Sun, 27 Jun 2021 18:05:18 GMT
ENV HOME=/home/redmine
# Sun, 27 Jun 2021 18:05:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 27 Jun 2021 18:05:35 GMT
ENV REDMINE_VERSION=4.2.1
# Sun, 27 Jun 2021 18:05:39 GMT
ENV REDMINE_DOWNLOAD_SHA256=ad4109c3425f1cfe4c8961f6ae6494c76e20d81ed946caa1e297d9eda13b41b4
# Sun, 27 Jun 2021 18:05:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 27 Jun 2021 18:12:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 27 Jun 2021 18:13:07 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 27 Jun 2021 18:13:11 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Sun, 27 Jun 2021 18:13:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 27 Jun 2021 18:13:31 GMT
EXPOSE 3000
# Sun, 27 Jun 2021 18:13:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f9cb1946299ce1824ee44809cd0c8b419528fee2f0f89e86400787a14b666f59`  
		Last Modified: Wed, 23 Jun 2021 00:37:07 GMT  
		Size: 30.6 MB (30553627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac452c4bb6e6395a6c30bf45ae8870373cbafea6e821e1422aa6b41f7b48995b`  
		Last Modified: Sat, 26 Jun 2021 15:15:05 GMT  
		Size: 12.7 MB (12704282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437c9a4f05494f86f197e3420a844fb6306f2d2c2f283974d8d774ee5d6278d7`  
		Last Modified: Sat, 26 Jun 2021 15:15:02 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896383b3f910010635236381fb1f49324d40a4f66509ea569da2189e6f8cea86`  
		Last Modified: Sat, 26 Jun 2021 15:17:30 GMT  
		Size: 23.4 MB (23414433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224e5394956c71c45410cad27852dc195557ecfbfbaee7204439ae13a28b28b9`  
		Last Modified: Sat, 26 Jun 2021 15:17:27 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fd187a264aeae26d9b80b75230370928d91f280d52eaf1844cb20b8ae4aafd`  
		Last Modified: Sun, 27 Jun 2021 18:46:14 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cdf4d4ced69636e0bb872a35dc4f1ea02bb7dece5501cff357ee8d1c7d03a8`  
		Last Modified: Sun, 27 Jun 2021 18:46:35 GMT  
		Size: 101.3 MB (101326554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9a4a54f461f7895823ca1be4388e8b8272e24bf156283e0a1191479372a25e`  
		Last Modified: Sun, 27 Jun 2021 18:46:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c6b33a37ba5992c6da95938d758f1aaed4ff228a21f0f98849591fefc076dc`  
		Last Modified: Sun, 27 Jun 2021 18:46:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8b51a7f7c743120a1f628a20d4e94bf30b73dcc9b461813562c4b3606b86d3`  
		Last Modified: Sun, 27 Jun 2021 18:46:12 GMT  
		Size: 3.1 MB (3058677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f136926b8f899ab02168938ee273590187585fc314ef408d159f63f0db7bc314`  
		Last Modified: Sun, 27 Jun 2021 18:46:20 GMT  
		Size: 67.0 MB (67031176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd77446f817d69b1eeb0f4cbb6cae819a8daeeac512ab319d71d2a2cf513923`  
		Last Modified: Sun, 27 Jun 2021 18:46:10 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:4e78127cd331869a412117d3519aae7444a173cfac7372e94cd50f40b4b75869
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220921110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b4e48f191173377f32d5a03828eb33f6a2a73e6cddcf444a3cb80f0988cba5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 22 Jun 2021 23:42:28 GMT
ADD file:a53e5772eefa4592eeff989f279dcc870986db7207b419dc3ae61cae85fce41f in / 
# Tue, 22 Jun 2021 23:42:29 GMT
CMD ["bash"]
# Fri, 25 Jun 2021 21:50:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 25 Jun 2021 21:50:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 25 Jun 2021 21:50:34 GMT
ENV LANG=C.UTF-8
# Fri, 25 Jun 2021 22:04:32 GMT
ENV RUBY_MAJOR=2.7
# Fri, 25 Jun 2021 22:04:32 GMT
ENV RUBY_VERSION=2.7.3
# Fri, 25 Jun 2021 22:04:32 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Fri, 25 Jun 2021 22:06:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 25 Jun 2021 22:06:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 25 Jun 2021 22:06:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 25 Jun 2021 22:06:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Jun 2021 22:06:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 25 Jun 2021 22:06:27 GMT
CMD ["irb"]
# Sun, 27 Jun 2021 12:01:35 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Sun, 27 Jun 2021 12:02:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Sun, 27 Jun 2021 12:02:47 GMT
ENV RAILS_ENV=production
# Sun, 27 Jun 2021 12:02:48 GMT
WORKDIR /usr/src/redmine
# Sun, 27 Jun 2021 12:02:49 GMT
ENV HOME=/home/redmine
# Sun, 27 Jun 2021 12:02:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 27 Jun 2021 12:02:51 GMT
ENV REDMINE_VERSION=4.2.1
# Sun, 27 Jun 2021 12:02:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=ad4109c3425f1cfe4c8961f6ae6494c76e20d81ed946caa1e297d9eda13b41b4
# Sun, 27 Jun 2021 12:02:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 27 Jun 2021 12:05:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		freetds-dev 		gcc 		libmariadbclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 27 Jun 2021 12:05:24 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 27 Jun 2021 12:05:24 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Sun, 27 Jun 2021 12:05:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 27 Jun 2021 12:05:25 GMT
EXPOSE 3000
# Sun, 27 Jun 2021 12:05:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d08eb187b3111e87e1b138f7b93df64c5470da613a64d0adc804e17e12aed4dc`  
		Last Modified: Tue, 22 Jun 2021 23:45:45 GMT  
		Size: 25.8 MB (25760716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b88cb14f24aaa60825253cd7a9321c503e99fe955e06b03a15e8276583442f`  
		Last Modified: Fri, 25 Jun 2021 22:34:28 GMT  
		Size: 10.8 MB (10814454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff84fb81d6a69bbb6cafd5458556eca4547678d0003d0909a3e9caad36eae81`  
		Last Modified: Fri, 25 Jun 2021 22:34:26 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7117ae025acf757f654160c8ef1b728a361be37405abb3acf8aed82b713f7cf0`  
		Last Modified: Fri, 25 Jun 2021 22:35:06 GMT  
		Size: 23.1 MB (23066462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd38e5aabfe7ef5c9b85b701aefc2597e07ac7f742590cfc9603036cfd12409`  
		Last Modified: Fri, 25 Jun 2021 22:35:04 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2030d9495bf8016a1d1e10dfd25869b8b9310c003a0ea5c8812cdc1adbf0111`  
		Last Modified: Sun, 27 Jun 2021 12:18:38 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74746f7b45a5d3a82e440dd824a98806c8edf532bd7b8e64631a0e92c365907`  
		Last Modified: Sun, 27 Jun 2021 12:18:52 GMT  
		Size: 91.8 MB (91788987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6476da70ba7b206700f3ce8d870f8de15e0eb39957bef4afce6118ad7ea5bcd`  
		Last Modified: Sun, 27 Jun 2021 12:18:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cd128f30f3effed14cc13b831040b88de6d2b9d4cc1e82b71564c1544bcce8`  
		Last Modified: Sun, 27 Jun 2021 12:18:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34705b6ba87f5f2b7c9b6cdfd473cf4c5bc934c5877c5f58fba6970dd9f1fd11`  
		Last Modified: Sun, 27 Jun 2021 12:18:37 GMT  
		Size: 3.1 MB (3058683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cbe1abf3f4d6234d5f2aa535717c5328686bfd856149084b5cdd704d8edd30`  
		Last Modified: Sun, 27 Jun 2021 12:18:43 GMT  
		Size: 66.4 MB (66427559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9a29ae67b371f9ad002e30cedb3ae8628e0991dcfc393dfeeb92dac8a5ab0`  
		Last Modified: Sun, 27 Jun 2021 12:18:37 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
