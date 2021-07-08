## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:f4cb2ae19c38cc46fff7e55b7637e43ff3d520f55f9761af93bd61f35f0868f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:18864e55c008f0ef499790c64ae0c35326403e72700265430a74abe6167b63b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221521668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0c50bd977fa6369b41f342f74e4cbb08de72fd5ba09391a2b5c5e395a1d4d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

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
# Wed, 07 Jul 2021 20:41:55 GMT
ENV PASSENGER_VERSION=6.0.9
# Wed, 07 Jul 2021 20:42:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 07 Jul 2021 20:42:26 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Wed, 07 Jul 2021 20:42:26 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Wed, 07 Jul 2021 20:42:27 GMT
CMD ["passenger" "start"]
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
	-	`sha256:f71a11320b67138cd2a0a1334bfd1756db2e441c02756b81375d40ef6b5662be`  
		Last Modified: Wed, 07 Jul 2021 20:59:44 GMT  
		Size: 21.1 MB (21127786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395d6858c59e57067f4887b7870aa71c24d60c5749d50d10bcc25771eef5eb2d`  
		Last Modified: Wed, 07 Jul 2021 20:59:42 GMT  
		Size: 4.9 MB (4919349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
