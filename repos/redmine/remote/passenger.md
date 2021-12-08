## `redmine:passenger`

```console
$ docker pull redmine@sha256:c16430463bbdc38ecd843c90f5e1ee1512f24ab956e523287c7b3efdd021a4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:passenger` - linux; amd64

```console
$ docker pull redmine@sha256:e60771cd8639a31c790236c81b30c890aecf8aff222754d6e86ae705d63d7225
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230421972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea800e981b8b080d39e57e12db7ebc162e7f7ea98d00cc6b7642c302ce76b59c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 16:23:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 16:23:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 02 Dec 2021 16:23:59 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 17:02:15 GMT
ENV RUBY_MAJOR=2.7
# Thu, 02 Dec 2021 17:02:16 GMT
ENV RUBY_VERSION=2.7.5
# Thu, 02 Dec 2021 17:02:16 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Thu, 02 Dec 2021 17:05:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 02 Dec 2021 17:05:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 02 Dec 2021 17:05:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 02 Dec 2021 17:05:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 17:05:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 02 Dec 2021 17:05:44 GMT
CMD ["irb"]
# Tue, 07 Dec 2021 23:28:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 07 Dec 2021 23:29:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 Dec 2021 23:29:18 GMT
ENV RAILS_ENV=production
# Tue, 07 Dec 2021 23:29:18 GMT
WORKDIR /usr/src/redmine
# Tue, 07 Dec 2021 23:29:18 GMT
ENV HOME=/home/redmine
# Tue, 07 Dec 2021 23:29:19 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 07 Dec 2021 23:29:19 GMT
ENV REDMINE_VERSION=4.2.3
# Tue, 07 Dec 2021 23:29:19 GMT
ENV REDMINE_DOWNLOAD_SHA256=72f633dc954217948558889ca85325fe6410cd18a2d8b39358e5d75932a47a0c
# Tue, 07 Dec 2021 23:29:23 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 07 Dec 2021 23:30:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 07 Dec 2021 23:30:07 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 07 Dec 2021 23:30:08 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Tue, 07 Dec 2021 23:30:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Dec 2021 23:30:08 GMT
EXPOSE 3000
# Tue, 07 Dec 2021 23:30:08 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Tue, 07 Dec 2021 23:30:24 GMT
ENV PASSENGER_VERSION=6.0.12
# Tue, 07 Dec 2021 23:30:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 07 Dec 2021 23:30:45 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Tue, 07 Dec 2021 23:30:45 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Tue, 07 Dec 2021 23:30:45 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2105ef7734bfb3176fb1731301dc8cba11560cb6f4560767dc010c7ec24bcb8a`  
		Last Modified: Thu, 02 Dec 2021 17:30:52 GMT  
		Size: 10.0 MB (9987818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6199182c39ff93c01c5170e9f8d2c667f9062af9c04ac8b7600d2f3a94ad9d19`  
		Last Modified: Thu, 02 Dec 2021 17:30:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f69a929beab6ba04c52122eed9e1335d65815eda3676c4c4a319a566e9830`  
		Last Modified: Thu, 02 Dec 2021 17:34:04 GMT  
		Size: 14.6 MB (14580702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaba5cbfae12f8f33df99daefd16c0f88de25db24eb353cb4d9143c851668472`  
		Last Modified: Thu, 02 Dec 2021 17:34:02 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd921c101c390c89285c21cf700e5b640a2cf7aa816776c892aed70e89af7533`  
		Last Modified: Tue, 07 Dec 2021 23:44:07 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1ee860a627b5bf3e830e01fa52c90601e8eb063c9feeaaccbf059af7f01ab3`  
		Last Modified: Tue, 07 Dec 2021 23:44:23 GMT  
		Size: 102.0 MB (101981060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b293ad377e748c413cf71de53fa72f879e0612ca43df2ceeeebe43ea57dfe4`  
		Last Modified: Tue, 07 Dec 2021 23:44:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b1ea2b0d2b4be0939db30a97ff26c5e18f0be4d1eea29bb5a1521e37a4a7f0`  
		Last Modified: Tue, 07 Dec 2021 23:44:04 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edf4253ca0eb7ecbf24118c36d1104bace72c0b19a2e39bb13946034fe58bf0`  
		Last Modified: Tue, 07 Dec 2021 23:44:05 GMT  
		Size: 3.1 MB (3063253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101b9fd05b8ae297806a8052171aa6df59d9182492d174bf4fb3b1b0c42c2a20`  
		Last Modified: Tue, 07 Dec 2021 23:44:10 GMT  
		Size: 43.3 MB (43278040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8e94c8d21a8068167344955651afe55841d01e6ebb97a348e7f54740e4450f`  
		Last Modified: Tue, 07 Dec 2021 23:44:04 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adeec1ef60275c0015e61cd7ebb666ce87935c46cec4cc3bb1213430623733b`  
		Last Modified: Tue, 07 Dec 2021 23:44:54 GMT  
		Size: 21.2 MB (21231995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847fc8aef6908e4c2a385acb541724094991eac96212c03f1dcbff72e165dee5`  
		Last Modified: Tue, 07 Dec 2021 23:44:52 GMT  
		Size: 4.9 MB (4924641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
