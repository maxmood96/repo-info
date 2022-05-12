## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:c8c64107bded5c85658bfdbe3d6698979002889d9754c8aa221b596395f7912d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:37dfa5496482dd878b213146aec9b7f4da564138da04dcdc5e51f4b6c785fb76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232263664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361dcb83a6f2a62d63bc9e77e054592ee88eeac0829d9f6fa4872ed0782cf89f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Wed, 11 May 2022 15:28:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 15:28:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 11 May 2022 15:28:35 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 15:55:59 GMT
ENV RUBY_MAJOR=2.7
# Wed, 11 May 2022 15:55:59 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 11 May 2022 15:56:00 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 11 May 2022 15:57:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 11 May 2022 15:57:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 May 2022 15:57:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 May 2022 15:57:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 15:57:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 11 May 2022 15:57:50 GMT
CMD ["irb"]
# Thu, 12 May 2022 04:33:22 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 12 May 2022 04:33:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 04:33:47 GMT
ENV RAILS_ENV=production
# Thu, 12 May 2022 04:33:48 GMT
WORKDIR /usr/src/redmine
# Thu, 12 May 2022 04:33:48 GMT
ENV HOME=/home/redmine
# Thu, 12 May 2022 04:33:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 12 May 2022 04:33:48 GMT
ENV REDMINE_VERSION=4.2.5
# Thu, 12 May 2022 04:33:48 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.5.tar.gz
# Thu, 12 May 2022 04:33:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=d97084b0eaad7266056814a0c0aec2737f4d23b8f67ce90c01a79b2eb5605984
# Thu, 12 May 2022 04:33:52 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 12 May 2022 04:34:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 12 May 2022 04:34:36 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 12 May 2022 04:34:36 GMT
COPY file:2c807aca5f34a9ab8acfef3c517816547300ed2b18590f703a1c783bdc707ba8 in / 
# Thu, 12 May 2022 04:34:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 May 2022 04:34:36 GMT
EXPOSE 3000
# Thu, 12 May 2022 04:34:36 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 12 May 2022 04:34:44 GMT
ENV PASSENGER_VERSION=6.0.13
# Thu, 12 May 2022 04:35:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 12 May 2022 04:35:04 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 12 May 2022 04:35:04 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 12 May 2022 04:35:04 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78121ab1df602556d61a5738a8a7dab7d0f35b55c9bb280a6a57efa8180e1134`  
		Last Modified: Wed, 11 May 2022 16:03:17 GMT  
		Size: 10.0 MB (9992152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fbe7e8745fe998a64f0cee757d280152f7100acbe9021e34c58123f5821847`  
		Last Modified: Wed, 11 May 2022 16:03:14 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaeabf1ed27ded4eeb23e75032177c47791e670991357ba467cc75642a651df5`  
		Last Modified: Wed, 11 May 2022 16:07:05 GMT  
		Size: 14.6 MB (14582317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fd6aac36e3b90f244d83df2e082210fb10f686c16b1ae2ee733378a7404d15`  
		Last Modified: Wed, 11 May 2022 16:07:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d15d7244971681e68e5622e44c13826bde350a1139df70885240e0a4be5dd0`  
		Last Modified: Thu, 12 May 2022 04:36:31 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d555713ff4bcb324fe36892c6c1446b1bcc8008dc05f7e9669c07d81f5528db3`  
		Last Modified: Thu, 12 May 2022 04:36:46 GMT  
		Size: 102.0 MB (101988701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a9bcc60465c29cc9509a0f731c4517ed2a6d6c9d05afacc5050a2c47add60f`  
		Last Modified: Thu, 12 May 2022 04:36:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275cb51350aff8d57340e394c86fcf568d8e217f858ac0c92d30a45a0fd499aa`  
		Last Modified: Thu, 12 May 2022 04:36:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3a80fdfddeda13e181adb6d7e8a859100cd1cb5cd6123e17d09eaf49d6b045`  
		Last Modified: Thu, 12 May 2022 04:36:29 GMT  
		Size: 3.1 MB (3064896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddfcdd29d7b5151748b08e90eccfde4e1bf734d7861a3e633a80c49b81d659b`  
		Last Modified: Thu, 12 May 2022 04:36:33 GMT  
		Size: 43.9 MB (43932759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592dfde130f59446852fd8acdb3b6ce41438f7d061358756caa0adf994c57bfc`  
		Last Modified: Thu, 12 May 2022 04:36:29 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fe39d5323e306e12356474363288f313d8a86211e9059f1aa95a9a8d7f805c`  
		Last Modified: Thu, 12 May 2022 04:37:11 GMT  
		Size: 21.8 MB (21781944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f0e0d74404b30bf6bf07ff9517e1f3300ce4f009ff9448cbf948d8d39dd0b3`  
		Last Modified: Thu, 12 May 2022 04:37:09 GMT  
		Size: 5.5 MB (5537179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
