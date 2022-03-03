## `redmine:passenger`

```console
$ docker pull redmine@sha256:b720f98c313f37f01d87a29c9727fece523411a811435578f911553484d6a0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:passenger` - linux; amd64

```console
$ docker pull redmine@sha256:5946c2418efdb47adc7fe74c6b3f4b7e400bdbf5e534b20a039b65d5f8e1ec6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230433755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561827f209ad4c6669b06569c9dd21db088fb3b6b87bfe6b8a971377fa4bfe34`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 06:30:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 06:30:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 02 Mar 2022 06:30:14 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 06:58:03 GMT
ENV RUBY_MAJOR=2.7
# Wed, 02 Mar 2022 06:58:03 GMT
ENV RUBY_VERSION=2.7.5
# Wed, 02 Mar 2022 06:58:03 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Wed, 02 Mar 2022 07:00:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 02 Mar 2022 07:00:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 02 Mar 2022 07:00:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 02 Mar 2022 07:00:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 07:00:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 02 Mar 2022 07:00:34 GMT
CMD ["irb"]
# Thu, 03 Mar 2022 06:17:20 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 03 Mar 2022 06:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 06:17:47 GMT
ENV RAILS_ENV=production
# Thu, 03 Mar 2022 06:17:47 GMT
WORKDIR /usr/src/redmine
# Thu, 03 Mar 2022 06:17:47 GMT
ENV HOME=/home/redmine
# Thu, 03 Mar 2022 06:17:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 03 Mar 2022 06:17:48 GMT
ENV REDMINE_VERSION=4.2.4
# Thu, 03 Mar 2022 06:17:48 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/attachments/download/28862/redmine-4.2.4.tar.gz
# Thu, 03 Mar 2022 06:17:48 GMT
ENV REDMINE_DOWNLOAD_SHA256=7f50fd4a6cf1c1e48091a87696b813ba264e11f04dec67fb006858a1b49a5c7d
# Thu, 03 Mar 2022 06:17:51 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 03 Mar 2022 06:18:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 03 Mar 2022 06:18:37 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 03 Mar 2022 06:18:38 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 03 Mar 2022 06:18:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 03 Mar 2022 06:18:38 GMT
EXPOSE 3000
# Thu, 03 Mar 2022 06:18:38 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 03 Mar 2022 06:18:42 GMT
ENV PASSENGER_VERSION=6.0.12
# Thu, 03 Mar 2022 06:19:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 03 Mar 2022 06:19:06 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 03 Mar 2022 06:19:06 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 03 Mar 2022 06:19:06 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ee8b5a8513d9fc48151146044e54b603d6f20a1fb3e530001d92b0e9d29a4b`  
		Last Modified: Wed, 02 Mar 2022 07:20:19 GMT  
		Size: 10.0 MB (9987855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32265d5c575d63a63c09278225011d337123544af3a350c87572a47f368d4f11`  
		Last Modified: Wed, 02 Mar 2022 07:20:17 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aec44d89e5112daa66bf1a01bb530a695564062f6935273185056d8321d8677`  
		Last Modified: Wed, 02 Mar 2022 09:04:10 GMT  
		Size: 14.6 MB (14580561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd66888540905d4ee91beeed175a804931f0ae2857a863d03659df7975bb98c`  
		Last Modified: Wed, 02 Mar 2022 09:04:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2005c9c0b38bab14690fb2c0969249c1107315edfe9f18456a9c3c0cdc56074`  
		Last Modified: Thu, 03 Mar 2022 06:21:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1e41b85e49d716d2d34cf7d64cdaa7e0df43982f140674b7f46876ea818466`  
		Last Modified: Thu, 03 Mar 2022 06:22:00 GMT  
		Size: 102.0 MB (101987263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04569d24956e36f7428059ca69411bd27ef9cf7fab34395c75e0ea4a1ccc86f`  
		Last Modified: Thu, 03 Mar 2022 06:21:40 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e3d41969441680ff4c115f81cf24ea4be2bffb2f87a87eaa047867dfe7212f`  
		Last Modified: Thu, 03 Mar 2022 06:21:40 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57288cfa1dc2b7ce125e2e348039eec6c31982dbf3e51fd8974a433ac7ed6a57`  
		Last Modified: Thu, 03 Mar 2022 06:21:41 GMT  
		Size: 3.1 MB (3071333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6145cccb3e6733f1802f11237cd1da5ab00a39edcff4ace6582b6af6ebd6b2`  
		Last Modified: Thu, 03 Mar 2022 06:21:46 GMT  
		Size: 43.3 MB (43279594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8a46a7bab49382a48bab12f529f8f0725b57495d97478863998bdf0e82bec8`  
		Last Modified: Thu, 03 Mar 2022 06:21:40 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ec72e2715771f8724517c80ac87d1e01a9f6fd3743e63e9efbe48ce6569be`  
		Last Modified: Thu, 03 Mar 2022 06:22:32 GMT  
		Size: 21.2 MB (21231859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93f22bb753f77bd2bba6f83395e7796fc490eb6975baed9719a6fd34d930779`  
		Last Modified: Thu, 03 Mar 2022 06:22:30 GMT  
		Size: 4.9 MB (4924655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
