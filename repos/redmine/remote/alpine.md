## `redmine:alpine`

```console
$ docker pull redmine@sha256:e6afdbf2cec7bb0cbb72ee8954f76c5926980101d8645b6c4d744b924ffb5529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:481186c596b80bb2bf21c575f9eb2e8a449f911fab69c4e8a4278c27353bfa23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190261381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f53acab2c252122f6977c695f52d1c1f5d606bbde191e0f8c2e44f6356110d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:07:43 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Wed, 20 Jul 2022 02:07:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Jul 2022 02:07:43 GMT
ENV LANG=C.UTF-8
# Wed, 20 Jul 2022 02:10:33 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Jul 2022 02:10:33 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 20 Jul 2022 02:10:33 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 20 Jul 2022 02:13:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 02:13:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 02:13:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 02:13:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 02:13:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 02:13:04 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 05:26:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 05:27:04 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 05:27:05 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 05:27:05 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 05:27:05 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 05:27:06 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 05:27:06 GMT
ENV REDMINE_VERSION=5.0.2
# Wed, 20 Jul 2022 05:27:06 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.2.tar.gz
# Wed, 20 Jul 2022 05:27:06 GMT
ENV REDMINE_DOWNLOAD_SHA256=4e718f44ba33716faf58c8fabf5d5f55b33c93426b7a33a83b5fc1b880585d57
# Wed, 20 Jul 2022 05:27:10 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 05:27:10 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 05:29:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 05:29:02 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 05:29:02 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 05:29:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 05:29:03 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 05:29:03 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378643a654642bcf067c99ea2c7f5e7378c49e8ab1bda31b2e06c68d65f28880`  
		Last Modified: Wed, 20 Jul 2022 02:19:13 GMT  
		Size: 3.7 MB (3683530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8df8816506e489ae2c14cd4f2d0ce6fbbd87b15f8cb4c2bc0a9795359f96456`  
		Last Modified: Wed, 20 Jul 2022 02:19:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6795d9ac512880b81cdfc4c16186f31e94a7f9cc1349b458d40b800ddc483e5`  
		Last Modified: Wed, 20 Jul 2022 02:19:39 GMT  
		Size: 29.5 MB (29529034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1d3fd4592c07536d6a6187b88e7f42002f36d0c098a5159f2c7a798db4b90d`  
		Last Modified: Wed, 20 Jul 2022 02:19:36 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5393a9c7f939afadbeaa16629f36b60d7b54d386c1266fe048cf8cfa8eb99686`  
		Last Modified: Wed, 20 Jul 2022 05:32:32 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124e173a577162fe9d94e3608d1f4b3edce573fc31b0d4b2c4cbdf725fcb003d`  
		Last Modified: Wed, 20 Jul 2022 05:32:44 GMT  
		Size: 82.4 MB (82442545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d09792c5a15a5976930bb7ad7042799e2ec68e7bb22b2798da64a4d1022398`  
		Last Modified: Wed, 20 Jul 2022 05:32:30 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7552a9e0e7d62af19b52a0058b012d970ba56721474db10835e185b7179a1eb5`  
		Last Modified: Wed, 20 Jul 2022 05:32:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91880cdd56722777139a2c7b5a79ffc40b904d39bb00e8fe9749d17487a6e3e`  
		Last Modified: Wed, 20 Jul 2022 05:32:31 GMT  
		Size: 3.1 MB (3130743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c3e90c9196247edbcb8803ab2ad5d4e40596e85a70d7907e248ee4765c76e5`  
		Last Modified: Wed, 20 Jul 2022 05:32:37 GMT  
		Size: 68.7 MB (68657083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1d7b874f42397f1b488351ebe463d5062383ba8b3547c83e40050f12377f03`  
		Last Modified: Wed, 20 Jul 2022 05:32:30 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:dfd4557f46a710534d6da11e0aa3183dfb2c8de1107d157a6abf8565b0274271
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181851275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586291f9fa506c140736effefb52f280fbbf2d1eb27ed77426b2deb6718a74e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 19 Jul 2022 22:49:49 GMT
ADD file:4958b5356608921fe85d83047b74d1cb4a53de78c3465039ac4e60a68329da64 in / 
# Tue, 19 Jul 2022 22:49:50 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 06:10:21 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Wed, 20 Jul 2022 06:10:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Jul 2022 06:10:23 GMT
ENV LANG=C.UTF-8
# Wed, 20 Jul 2022 06:15:25 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Jul 2022 06:15:25 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 20 Jul 2022 06:15:25 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 20 Jul 2022 06:19:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 06:19:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 06:19:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 06:19:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 06:19:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 06:19:52 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 08:26:53 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 08:27:24 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 08:27:26 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 08:27:26 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 08:27:26 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 08:27:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 08:27:28 GMT
ENV REDMINE_VERSION=5.0.2
# Wed, 20 Jul 2022 08:27:29 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.2.tar.gz
# Wed, 20 Jul 2022 08:27:29 GMT
ENV REDMINE_DOWNLOAD_SHA256=4e718f44ba33716faf58c8fabf5d5f55b33c93426b7a33a83b5fc1b880585d57
# Wed, 20 Jul 2022 08:27:36 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 08:27:36 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 08:32:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 08:32:45 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 08:32:46 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 08:32:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 08:32:46 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 08:32:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fcc62ebebb3542c1aad49c3cc072a98cf619f67e914baba1ea7dfeadcb32cbdd`  
		Last Modified: Tue, 19 Jul 2022 22:51:27 GMT  
		Size: 2.6 MB (2622400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9234a34ad73a07c7831af58763d1102235c85855a7573f83eaaca7d39f0e0f1f`  
		Last Modified: Wed, 20 Jul 2022 06:31:35 GMT  
		Size: 3.4 MB (3431626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1b5ff32ceba41ceef2cfa97d497d872f17607295e22dc466b412937ed1b4dd`  
		Last Modified: Wed, 20 Jul 2022 06:31:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c0ad19c8a2b45e1d6f90e00914d59e5e74fe1ea5f99ce7565ec784d55b1faa`  
		Last Modified: Wed, 20 Jul 2022 06:32:23 GMT  
		Size: 28.1 MB (28139920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3325f6c0305168a620032adc55b4502faf02ad29c46b6ddbd16d1d610b7bfc29`  
		Last Modified: Wed, 20 Jul 2022 06:32:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca59c89ba243849214804dd86b533315e5387c4a4aad926a6e6b6b98bcd6eda`  
		Last Modified: Wed, 20 Jul 2022 08:41:17 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab03aa0847e4123145b9acf1099502166a47a2ee7edc119a6813f0cd76ed28fd`  
		Last Modified: Wed, 20 Jul 2022 08:42:10 GMT  
		Size: 77.9 MB (77890051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed75b443d1f42b8b9b68c7fd5dc9e5e205a000d5daa52495fed815aba92e734`  
		Last Modified: Wed, 20 Jul 2022 08:41:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbedb3c9b7b86ee795d16aa612c3af559f295695200a106bdf57d8796a20526`  
		Last Modified: Wed, 20 Jul 2022 08:41:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b04b07f39fdd47fe8b1edc2d0e396e77e03ca091e55f6576a9b06f9c7a0c8`  
		Last Modified: Wed, 20 Jul 2022 08:41:19 GMT  
		Size: 3.1 MB (3130766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf80805e7d99ea1987657575bec5dfd101de931ef57c5cde3c6041ad56b7c68d`  
		Last Modified: Wed, 20 Jul 2022 08:41:48 GMT  
		Size: 66.6 MB (66632708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de00c460fdaf198b36ad9406b21dcb6aa23854287b1cc60c2c2ce6098821a266`  
		Last Modified: Wed, 20 Jul 2022 08:41:15 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:3a0f3f429e285cf9bd4980d66bde200c378505be1f21f5873bdeb612449d53a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178843871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39acc2c1a4e702df9794c4b3ee6ea1ef2808cb18177db53304d505c748ec16f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:14:47 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 05 Apr 2022 03:14:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 05 Apr 2022 03:14:49 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 03:24:54 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 19:20:02 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 19:20:03 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 19:24:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 19:24:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 19:24:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 19:24:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 19:24:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 19:24:14 GMT
CMD ["irb"]
# Wed, 13 Apr 2022 02:40:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Tue, 12 Jul 2022 03:04:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Tue, 12 Jul 2022 03:04:53 GMT
ENV RAILS_ENV=production
# Tue, 12 Jul 2022 03:04:53 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Jul 2022 03:04:54 GMT
ENV HOME=/home/redmine
# Tue, 12 Jul 2022 03:04:55 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Jul 2022 03:04:56 GMT
ENV REDMINE_VERSION=5.0.2
# Tue, 12 Jul 2022 03:04:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.2.tar.gz
# Tue, 12 Jul 2022 03:04:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=4e718f44ba33716faf58c8fabf5d5f55b33c93426b7a33a83b5fc1b880585d57
# Tue, 12 Jul 2022 03:05:03 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Jul 2022 03:05:04 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 12 Jul 2022 03:09:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Tue, 12 Jul 2022 03:09:51 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Jul 2022 03:09:51 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Tue, 12 Jul 2022 03:09:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 03:09:52 GMT
EXPOSE 3000
# Tue, 12 Jul 2022 03:09:53 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf827bdbeb6803ee356377c29e2dc205b1bde74d175f62f1022266f052435ad0`  
		Last Modified: Tue, 05 Apr 2022 04:08:52 GMT  
		Size: 3.3 MB (3301946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a44b4cdfaacd5e37f9bcb3628c53a09ce87fcef30a5a2a3b3cc27d88b6ae81f`  
		Last Modified: Tue, 05 Apr 2022 04:08:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a545f4fcd6303889ed08bb6f56b48e8b906f79c64befc1c34dd95f185f9bd1b7`  
		Last Modified: Tue, 12 Apr 2022 20:58:27 GMT  
		Size: 28.0 MB (28033895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3748643d23db2ff31fb281b7593a55ac7cf53b599ad7bf2bb4ca88ef87fce5a`  
		Last Modified: Tue, 12 Apr 2022 20:58:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95969648f8bbdf35a7bd306b6e088953a6b4424e038a253c13acba81935c204e`  
		Last Modified: Wed, 13 Apr 2022 03:15:57 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0649a56add109aafeb0be45416cff598d7becabf8768099e39a16ed757782d5e`  
		Last Modified: Tue, 12 Jul 2022 03:20:49 GMT  
		Size: 74.4 MB (74427203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345ca64171f6ab54959aa7df4bb0b7ab86eb371d0de8cedcc736fb9d82c01b29`  
		Last Modified: Tue, 12 Jul 2022 03:20:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc8c34ca16d20cca684b95418fa47be01d7763c250c149b5e6a3f915be51086`  
		Last Modified: Tue, 12 Jul 2022 03:20:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd9c04f2abd5d643c9f951a5354af3a9900141ccef217b0fbc06fedbdbe0382`  
		Last Modified: Tue, 12 Jul 2022 03:20:05 GMT  
		Size: 3.1 MB (3130774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2569739971332291a0b81078e0003c4588b37a984b3ed0b459e3682eb9cfdca`  
		Last Modified: Tue, 12 Jul 2022 03:20:32 GMT  
		Size: 67.5 MB (67521923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d47d473e2f34efadaff30b2d859e054b2b2bc6693659d8f4f34feb7502c15e`  
		Last Modified: Tue, 12 Jul 2022 03:20:01 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:70174ada58f2aeefccc99f571e8a554e8faa60d0261e5e09623d3cacf430c5d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186064221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29e2da0765dceb9218d953a2fca981fa3c214295ba2f4662271ed6f4de7f795`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 03:30:16 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Wed, 20 Jul 2022 03:30:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Jul 2022 03:30:18 GMT
ENV LANG=C.UTF-8
# Wed, 20 Jul 2022 03:33:27 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Jul 2022 03:33:28 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 20 Jul 2022 03:33:29 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 20 Jul 2022 03:35:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 03:35:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 03:35:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 03:35:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 03:35:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 03:35:50 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 07:21:01 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 07:21:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 07:21:11 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 07:21:12 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 07:21:13 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 07:21:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 07:21:15 GMT
ENV REDMINE_VERSION=5.0.2
# Wed, 20 Jul 2022 07:21:16 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.2.tar.gz
# Wed, 20 Jul 2022 07:21:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=4e718f44ba33716faf58c8fabf5d5f55b33c93426b7a33a83b5fc1b880585d57
# Wed, 20 Jul 2022 07:21:21 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 07:21:22 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 07:23:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 07:23:28 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 07:23:29 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 07:23:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 07:23:31 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 07:23:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b37fdcefcd8b65714a36f4b653adecc9bd1a4befb2be113eb2570e7c7bf8608`  
		Last Modified: Wed, 20 Jul 2022 03:44:37 GMT  
		Size: 3.6 MB (3646235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6572f69e871a73b48037d51991cac45c53eb603f388aabba322529e005c331`  
		Last Modified: Wed, 20 Jul 2022 03:44:36 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6721de2bed68ec18915720915d3ff4120094a10fa3fd5a578c87e59dc9dba7`  
		Last Modified: Wed, 20 Jul 2022 03:45:16 GMT  
		Size: 28.9 MB (28895676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d0b0ffb190f98a21f1754c87fe92a7868a958d7d8ddabae3f73b0bb070a292`  
		Last Modified: Wed, 20 Jul 2022 03:45:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bf4b063713dc9e2b570ddc48c7e8874e1b2b9e98c57eccba5bd7ad54c88de1`  
		Last Modified: Wed, 20 Jul 2022 07:27:55 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456966711132e791f1ab277a67e462f882b36b07983d16b9ccbba0b6a55e86cb`  
		Last Modified: Wed, 20 Jul 2022 07:28:07 GMT  
		Size: 79.7 MB (79682548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8723c15e3751df5a6c1fd170df1268db0e21fa8d2deee8ae319bcfbb39692d7b`  
		Last Modified: Wed, 20 Jul 2022 07:27:53 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4819c06c03552bbd2054ed4622fbe195bd84833360ddb6c6ef94053828b995d5`  
		Last Modified: Wed, 20 Jul 2022 07:27:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9542673ff52847368adc6cf7a14911630475ed87f8a02902fb921c784895a00`  
		Last Modified: Wed, 20 Jul 2022 07:27:54 GMT  
		Size: 3.1 MB (3130740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbc5da74c881af4ab1f834006a5acfd7cefb0effd801eff2e85b50339d03c8a`  
		Last Modified: Wed, 20 Jul 2022 07:28:01 GMT  
		Size: 68.0 MB (67988455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e4a2712b1290df570507bb1296845b154d5e7777e515ee106dbbc87d5aaf09`  
		Last Modified: Wed, 20 Jul 2022 07:27:53 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine` - linux; 386

```console
$ docker pull redmine@sha256:7256d474d0b145aaa95e8f5b1f8bb0223aae3f69b8d0ff376331cb1e7d17712a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188975903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcd5decdce1acfefd9fd10c81d607f3c3041cbf5414ab3b9b71893b11ef19a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 19 Jul 2022 22:38:32 GMT
ADD file:3c11e12b5c10a13cce2dec1d5ae8d7c6a61e0ccc2b4b44b6cf5b80b97eed9869 in / 
# Tue, 19 Jul 2022 22:38:32 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:05:18 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Wed, 20 Jul 2022 02:05:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Jul 2022 02:05:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 Jul 2022 02:08:29 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Jul 2022 02:08:30 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 20 Jul 2022 02:08:31 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 20 Jul 2022 02:10:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 02:10:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 02:10:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 02:10:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 02:10:55 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 02:10:56 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 03:41:42 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 03:41:55 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 03:41:55 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 03:41:56 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 03:41:57 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 03:41:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 03:41:59 GMT
ENV REDMINE_VERSION=5.0.2
# Wed, 20 Jul 2022 03:42:00 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.2.tar.gz
# Wed, 20 Jul 2022 03:42:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=4e718f44ba33716faf58c8fabf5d5f55b33c93426b7a33a83b5fc1b880585d57
# Wed, 20 Jul 2022 03:42:09 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 03:42:10 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 03:44:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 03:44:06 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 03:44:08 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 03:44:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:44:09 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 03:44:10 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8bbe360ea5d414165050aeceb6ca82ed372606830e0addd5df0d1000146ab250`  
		Last Modified: Tue, 19 Jul 2022 22:39:24 GMT  
		Size: 2.8 MB (2819359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d94f02d592f22610230f5dcb44b92dca88e73aa732b056818d91e034f469c9`  
		Last Modified: Wed, 20 Jul 2022 02:19:44 GMT  
		Size: 3.7 MB (3709287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a454b154e94c87467e55f2e4d7183e9d80f086c70f0f9037d0574ed3085d43`  
		Last Modified: Wed, 20 Jul 2022 02:19:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312c535032253d1f2bfc95a036c7bb02bc094dacdc00e415442dbab8567dd31e`  
		Last Modified: Wed, 20 Jul 2022 02:20:29 GMT  
		Size: 28.1 MB (28143091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3bd80172022273edcd370620b6a4b6c75af9870d80c8bb84aa73aa0071386b`  
		Last Modified: Wed, 20 Jul 2022 02:20:23 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a744d3de780993b9e0c02a225d5f5396220c7b80ab18fddee65a68e5bdcd319`  
		Last Modified: Wed, 20 Jul 2022 03:48:28 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da737ebdd8681c6c4943b08023a204c7fd497980f1b67a39186e46669e8356c9`  
		Last Modified: Wed, 20 Jul 2022 03:48:40 GMT  
		Size: 84.1 MB (84071441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecd92cbb3a435f087aa3c77a846a7f13a7076e7c31db59264112ef90833c9ad`  
		Last Modified: Wed, 20 Jul 2022 03:48:26 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c1a6dcbd7a2d3ae7a3def591f10ea41caaae012e69c446c081bdbac07bc18d`  
		Last Modified: Wed, 20 Jul 2022 03:48:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12ffff806e16a9c4539c96d728b4df8671b03f4933e9faeb467eb2a4b41798c`  
		Last Modified: Wed, 20 Jul 2022 03:48:26 GMT  
		Size: 3.1 MB (3130740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79632e45c426b5612044b0dbb1302dc99a3e532e0ac1036db6b17308ed69e463`  
		Last Modified: Wed, 20 Jul 2022 03:48:32 GMT  
		Size: 67.1 MB (67098309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6137e8a46edb4343943888d376d55239e3a50aecc838f339965e51b637f77ed5`  
		Last Modified: Wed, 20 Jul 2022 03:48:26 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:04a174aebd735633ea260123c65a1f2d71c746f8219153f6d5b55e6dcbdb17a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191008622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110dfd883288af7f26b4908c7b2f57230a22f54f380b2bb7fa668d7599f5f072`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 19 Jul 2022 22:26:26 GMT
ADD file:fee9d1c50a43d2072ff528133302b3e4d565d1853e14a7d56be9f4532a330841 in / 
# Tue, 19 Jul 2022 22:26:28 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 05:48:10 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Wed, 20 Jul 2022 05:48:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Jul 2022 05:48:28 GMT
ENV LANG=C.UTF-8
# Wed, 20 Jul 2022 05:54:09 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Jul 2022 05:54:16 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 20 Jul 2022 05:54:22 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 20 Jul 2022 05:57:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 05:57:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 05:58:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 05:58:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 05:58:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 05:58:39 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 08:44:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 08:47:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 08:47:40 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 08:47:45 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 08:47:52 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 08:48:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 08:48:05 GMT
ENV REDMINE_VERSION=5.0.2
# Wed, 20 Jul 2022 08:48:10 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.2.tar.gz
# Wed, 20 Jul 2022 08:48:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=4e718f44ba33716faf58c8fabf5d5f55b33c93426b7a33a83b5fc1b880585d57
# Wed, 20 Jul 2022 08:48:27 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 08:48:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 08:51:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 08:52:08 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 08:52:10 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 08:52:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 08:52:16 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 08:52:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a340aa0651fe455d7a9f4dba0b2b8048ef90ce173a72ac17cf04b9b6af34a2a9`  
		Last Modified: Tue, 19 Jul 2022 22:27:55 GMT  
		Size: 2.8 MB (2811642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60a235da261b9298e346a6a1b9ecd5db36578485921ba95c6b79873d6cf2495`  
		Last Modified: Wed, 20 Jul 2022 06:12:29 GMT  
		Size: 3.8 MB (3800352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f24e935cfd9617a4ef5e2fd2677162b0b3874d337fe81d023fb8ec44d6b678`  
		Last Modified: Wed, 20 Jul 2022 06:12:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73d8c27db4ddf14c0e1399be1d81323f374daf1bc09b28cfbedecd6dbbb18eb`  
		Last Modified: Wed, 20 Jul 2022 06:13:13 GMT  
		Size: 29.6 MB (29579423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb7d1baa721a0ef344940eefa0c22569e01c7daf5a40c92d1c1b827feaaa87d`  
		Last Modified: Wed, 20 Jul 2022 06:13:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d550350942eb744ee309cb0cf27641b19294c46dcd40627ab77d131fbdc61a92`  
		Last Modified: Wed, 20 Jul 2022 09:01:46 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1ce9e00822e363837e9910c143977fd34d91d9367a0d7faf706d9128a6ff69`  
		Last Modified: Wed, 20 Jul 2022 09:02:01 GMT  
		Size: 82.7 MB (82689916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8562727b1feace177b919e0ce21a4e109c37b3e7ef3e3c97847d3ab84f2831`  
		Last Modified: Wed, 20 Jul 2022 09:01:42 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d17b71e898ac5200026f8151e2c459ad391c15c74c2319fc3754b37db1dee9e`  
		Last Modified: Wed, 20 Jul 2022 09:01:42 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c283653752e31e469970745dc6b898ca40f512683dc4ddf4d77e88b6c581faf`  
		Last Modified: Wed, 20 Jul 2022 09:01:43 GMT  
		Size: 3.1 MB (3130801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19af6a2e7bee862a35b07f318928284f3e9ea91b06882b8a899217e82c7b98f`  
		Last Modified: Wed, 20 Jul 2022 09:01:52 GMT  
		Size: 69.0 MB (68992690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05c65da8d6e70b79bb05c2e8e6e95f8ddc4b0171ef03f6f6d3256af42dadb38`  
		Last Modified: Wed, 20 Jul 2022 09:01:42 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine` - linux; s390x

```console
$ docker pull redmine@sha256:8350e0836766174e70dc51123aefe8dacca75c1bd7e9a4a7fb51ddd509c250f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182322243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817c7ada119ecc202819a407df052e3bfd112924264297924f35c98702c50445`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 19 Jul 2022 22:41:55 GMT
ADD file:9671b14d87fd7602279c1b3d1148babaa2c411e4ab0570d294d95324fa19210c in / 
# Tue, 19 Jul 2022 22:41:56 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 01:13:56 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Wed, 20 Jul 2022 01:14:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 20 Jul 2022 01:14:01 GMT
ENV LANG=C.UTF-8
# Wed, 20 Jul 2022 01:19:32 GMT
ENV RUBY_MAJOR=3.1
# Wed, 20 Jul 2022 01:19:32 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 20 Jul 2022 01:19:33 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 20 Jul 2022 01:23:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 01:23:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 01:23:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 01:24:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 01:24:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 01:24:02 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 06:39:45 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 06:40:13 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 06:40:21 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 06:40:21 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 06:40:22 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 06:40:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 06:40:24 GMT
ENV REDMINE_VERSION=5.0.2
# Wed, 20 Jul 2022 06:40:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.2.tar.gz
# Wed, 20 Jul 2022 06:40:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=4e718f44ba33716faf58c8fabf5d5f55b33c93426b7a33a83b5fc1b880585d57
# Wed, 20 Jul 2022 06:40:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 06:40:33 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 06:42:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 06:43:10 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 06:43:11 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 06:43:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 06:43:12 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 06:43:12 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ef614dc1febe442e84bcc0f287628aea0f6547a0f322d7bed0a46ffabd5e0a50`  
		Last Modified: Tue, 19 Jul 2022 22:43:17 GMT  
		Size: 2.6 MB (2600789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa44453d6ffe65e0d05bd1c9505053c31dcf15490bb55929f29ed5db2049524a`  
		Last Modified: Wed, 20 Jul 2022 01:35:39 GMT  
		Size: 3.7 MB (3746060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4470ea73ed76cd558c5432a49638d18ad57e9e288b8cca26e7520550312b43ab`  
		Last Modified: Wed, 20 Jul 2022 01:35:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949f77c1fe42ead43a4d8774a7ff07a7c4fdcb5dd8a5d36d679acee3f91537ec`  
		Last Modified: Wed, 20 Jul 2022 01:36:18 GMT  
		Size: 29.4 MB (29365542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4696dca923b1c6be8b156717e121d534720ca33e3221ef959422f7654d77746c`  
		Last Modified: Wed, 20 Jul 2022 01:36:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f66a029299ce5ea870e14fcda32eb48dd2317b5a11c1eadf61179553904cd7`  
		Last Modified: Wed, 20 Jul 2022 06:48:29 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10288b48cd889713c389ea658bdec115e57bd7dff4ee9ce235ae8eea10a72f40`  
		Last Modified: Wed, 20 Jul 2022 06:48:39 GMT  
		Size: 74.5 MB (74538155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10729ef5f120180918e8d42758cf286e2ab77831c95fe6af1bc28b85f4b3efd8`  
		Last Modified: Wed, 20 Jul 2022 06:48:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfe964ac7c80a109948819222da1b585a9862c69f127145bfa23043ec5a437c`  
		Last Modified: Wed, 20 Jul 2022 06:48:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f851248dd2f40a63516c0f819c342f14d05e4cbf785ccfd3b24961c154ad21`  
		Last Modified: Wed, 20 Jul 2022 06:48:28 GMT  
		Size: 3.1 MB (3130760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089b1789167406e45c8946169300f32bff25826b8a5c4c21d09c0e5fd54d25c3`  
		Last Modified: Wed, 20 Jul 2022 06:48:34 GMT  
		Size: 68.9 MB (68937135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49330620d21b1815c1f52b451b4b35bf5087e0131d28db5fc1e0e3362202be3d`  
		Last Modified: Wed, 20 Jul 2022 06:48:28 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
