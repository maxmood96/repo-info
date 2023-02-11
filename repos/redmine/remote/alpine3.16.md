## `redmine:alpine3.16`

```console
$ docker pull redmine@sha256:29fbc3ce1a52d0c2a1c677eadf5111864e4bbd2f8972d0d0a7a3fee0eda5c610
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

### `redmine:alpine3.16` - linux; amd64

```console
$ docker pull redmine@sha256:7720c8e7ac515a40dd724142d71ba9b29623231cd70e7386285620016476d367
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199746361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496b9f7a0908276841e363f8193fc39bbe86a3d995667c032523a0d9135d2332`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:34:26 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 11 Feb 2023 13:34:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 11 Feb 2023 13:34:27 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 13:40:20 GMT
ENV RUBY_MAJOR=3.1
# Sat, 11 Feb 2023 13:40:20 GMT
ENV RUBY_VERSION=3.1.3
# Sat, 11 Feb 2023 13:40:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Sat, 11 Feb 2023 13:42:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 11 Feb 2023 13:42:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 11 Feb 2023 13:42:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 11 Feb 2023 13:42:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 13:42:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 11 Feb 2023 13:42:51 GMT
CMD ["irb"]
# Sat, 11 Feb 2023 17:13:50 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 11 Feb 2023 17:13:58 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 11 Feb 2023 17:13:59 GMT
ENV RAILS_ENV=production
# Sat, 11 Feb 2023 17:13:59 GMT
WORKDIR /usr/src/redmine
# Sat, 11 Feb 2023 17:13:59 GMT
ENV HOME=/home/redmine
# Sat, 11 Feb 2023 17:14:00 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 11 Feb 2023 17:14:00 GMT
ENV REDMINE_VERSION=5.0.4
# Sat, 11 Feb 2023 17:14:00 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.4.tar.gz
# Sat, 11 Feb 2023 17:14:00 GMT
ENV REDMINE_DOWNLOAD_SHA256=39436f5f8d26f5b7ce17e79903a3112e556e924da4f51c05b57f5defbe6f2924
# Sat, 11 Feb 2023 17:14:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 11 Feb 2023 17:14:04 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 11 Feb 2023 17:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 11 Feb 2023 17:15:55 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 11 Feb 2023 17:15:55 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Sat, 11 Feb 2023 17:15:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 17:15:56 GMT
EXPOSE 3000
# Sat, 11 Feb 2023 17:15:56 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4e7d65ccdcf8803658fd95287533dcaeab1267d1c6f5675ba0d3c8ee08148e`  
		Last Modified: Sat, 11 Feb 2023 13:49:20 GMT  
		Size: 3.9 MB (3851507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923958f2c001452ff5d4adb46921384aa6f4e085ca364ec30ca4055fea99eec0`  
		Last Modified: Sat, 11 Feb 2023 13:49:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4255ad62eacbd87e5b5242ba5ae0bbc392244979e1a9bfea966e4aa1f65dea58`  
		Last Modified: Sat, 11 Feb 2023 13:49:59 GMT  
		Size: 29.3 MB (29318962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b0161c835d42b16d6249cf235d0814cadc501abefa302ee8c929cf259c771c`  
		Last Modified: Sat, 11 Feb 2023 13:49:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25812b6945b6e62ba35136b5784ea2eeb52fa25657782b45ac445ce34c3b6604`  
		Last Modified: Sat, 11 Feb 2023 17:19:12 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600d6d21020f13bb31144f05ea85b31f506f5b0669ee20e4a3936c5116a45586`  
		Last Modified: Sat, 11 Feb 2023 17:19:26 GMT  
		Size: 90.4 MB (90427713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462d1612167bc16ac24588a8aded45df27a4159e332114d94891c7a6657419f7`  
		Last Modified: Sat, 11 Feb 2023 17:19:10 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74eacda2c4b5b1fb59a87c84d3a621a83d808dfbae4f8824e058b4187cc5fba`  
		Last Modified: Sat, 11 Feb 2023 17:19:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cba5f51178df2f1b282ba0638cb3d360d0070443c52cd9e3336701afc007a9f`  
		Last Modified: Sat, 11 Feb 2023 17:19:11 GMT  
		Size: 3.1 MB (3143962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0d99239672f04d0aa9aa8b6612c08b1cc17b841c4660333d0bd0a32409040a`  
		Last Modified: Sat, 11 Feb 2023 17:19:17 GMT  
		Size: 70.2 MB (70192520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ef7ae6ad3ed267335b6a01e2b42db7e00152409365ee130bc1cf649057d9b1`  
		Last Modified: Sat, 11 Feb 2023 17:19:10 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.16` - linux; arm variant v6

```console
$ docker pull redmine@sha256:6e617196d84a3642e26d348c1abe8a5effdbd5238f1165733d16af13f08981a6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190027858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189571283146701c48f469a0696ba0edbd8c4bcf0be44bdfb57d244228b39322`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:54:50 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 11 Feb 2023 06:54:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 11 Feb 2023 06:54:51 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 07:01:28 GMT
ENV RUBY_MAJOR=3.1
# Sat, 11 Feb 2023 07:01:28 GMT
ENV RUBY_VERSION=3.1.3
# Sat, 11 Feb 2023 07:01:28 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Sat, 11 Feb 2023 07:04:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 11 Feb 2023 07:04:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 11 Feb 2023 07:04:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 11 Feb 2023 07:04:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 07:04:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 11 Feb 2023 07:04:21 GMT
CMD ["irb"]
# Sat, 11 Feb 2023 10:02:34 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 11 Feb 2023 10:02:49 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 11 Feb 2023 10:02:50 GMT
ENV RAILS_ENV=production
# Sat, 11 Feb 2023 10:02:50 GMT
WORKDIR /usr/src/redmine
# Sat, 11 Feb 2023 10:02:50 GMT
ENV HOME=/home/redmine
# Sat, 11 Feb 2023 10:02:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 11 Feb 2023 10:02:51 GMT
ENV REDMINE_VERSION=5.0.4
# Sat, 11 Feb 2023 10:02:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.4.tar.gz
# Sat, 11 Feb 2023 10:02:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=39436f5f8d26f5b7ce17e79903a3112e556e924da4f51c05b57f5defbe6f2924
# Sat, 11 Feb 2023 10:02:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 11 Feb 2023 10:02:56 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 11 Feb 2023 10:05:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 11 Feb 2023 10:05:34 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 11 Feb 2023 10:05:34 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Sat, 11 Feb 2023 10:05:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 10:05:35 GMT
EXPOSE 3000
# Sat, 11 Feb 2023 10:05:35 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d088b1a6f43566b0657c1a55e6469cc5165dd2c567849208462acae1059c82`  
		Last Modified: Sat, 11 Feb 2023 07:12:17 GMT  
		Size: 3.6 MB (3593789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174cb3777a786b751b7b330c4a84fe5bd3b428c2613f392498d33cf9ac5f6e7d`  
		Last Modified: Sat, 11 Feb 2023 07:12:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4d52722f72392114dbcbeefabb0d800a0f7f972fe2d7829b5aee031f7c3a7f`  
		Last Modified: Sat, 11 Feb 2023 07:13:03 GMT  
		Size: 28.3 MB (28266583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e959f97fd80f4a9195d72d283b16fa85de88d5c6b46a2ce678cb8864c45196df`  
		Last Modified: Sat, 11 Feb 2023 07:12:59 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fba15ae0859e126c6ef736838f5af31dca8553f50f4ad2f189d12e27022fa3a`  
		Last Modified: Sat, 11 Feb 2023 10:10:28 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd4c522d4014bfd39f6434b2fcecbfbe722ce7bf517e360c20502cef83cf654`  
		Last Modified: Sat, 11 Feb 2023 10:10:49 GMT  
		Size: 83.9 MB (83929157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b01776626dd5ba7625f3cc1f55252e8e6310c3047f4a51e36cc6f76d587d7ab`  
		Last Modified: Sat, 11 Feb 2023 10:10:26 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca5b985aaa8fb19ae427903f737521760d4912273fd01c89d0c0eb79280426f`  
		Last Modified: Sat, 11 Feb 2023 10:10:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e724d6161c32cfc3ed8a694462ec8b54c0f5ad8d48052f0b3d184ed3554150af`  
		Last Modified: Sat, 11 Feb 2023 10:10:27 GMT  
		Size: 3.1 MB (3143393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c580e93e9ee6d8a1581e68fc38ba0ec3d405c7db7eb0fff87ba07da82dd24779`  
		Last Modified: Sat, 11 Feb 2023 10:10:40 GMT  
		Size: 68.5 MB (68474345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf34dcd9089fb180a04aa610884ccd893c9ca9365c71d1197b5bc55d2ec54ef`  
		Last Modified: Sat, 11 Feb 2023 10:10:26 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.16` - linux; arm variant v7

```console
$ docker pull redmine@sha256:82ae3857f5be3e6efb13b28dbac4540b189e5dc76a9052c9325d5c8eaf97e8b2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187316200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2632fb9b243a8bdc150f83e995a3bf4b97a51e40ab5a33570d68d133e1e81b58`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:09:35 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 11 Feb 2023 06:09:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 11 Feb 2023 06:09:36 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 06:15:45 GMT
ENV RUBY_MAJOR=3.1
# Sat, 11 Feb 2023 06:15:45 GMT
ENV RUBY_VERSION=3.1.3
# Sat, 11 Feb 2023 06:15:46 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Sat, 11 Feb 2023 06:18:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 11 Feb 2023 06:18:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 11 Feb 2023 06:18:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 11 Feb 2023 06:18:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 06:18:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 11 Feb 2023 06:18:33 GMT
CMD ["irb"]
# Sat, 11 Feb 2023 12:52:58 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 11 Feb 2023 12:53:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 11 Feb 2023 12:53:14 GMT
ENV RAILS_ENV=production
# Sat, 11 Feb 2023 12:53:14 GMT
WORKDIR /usr/src/redmine
# Sat, 11 Feb 2023 12:53:14 GMT
ENV HOME=/home/redmine
# Sat, 11 Feb 2023 12:53:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 11 Feb 2023 12:53:15 GMT
ENV REDMINE_VERSION=5.0.4
# Sat, 11 Feb 2023 12:53:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.4.tar.gz
# Sat, 11 Feb 2023 12:53:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=39436f5f8d26f5b7ce17e79903a3112e556e924da4f51c05b57f5defbe6f2924
# Sat, 11 Feb 2023 12:53:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 11 Feb 2023 12:53:19 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 11 Feb 2023 12:55:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 11 Feb 2023 12:55:29 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 11 Feb 2023 12:55:29 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Sat, 11 Feb 2023 12:55:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 12:55:29 GMT
EXPOSE 3000
# Sat, 11 Feb 2023 12:55:29 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c17e12675e54657e74ed77740bc5fcf47c01af8c5f9127da41284dece4aba4a`  
		Last Modified: Sat, 11 Feb 2023 06:30:38 GMT  
		Size: 3.5 MB (3461472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e1eec83df6cde98507695503ba9324dffc633161c87325ef0b3b24f4037b7`  
		Last Modified: Sat, 11 Feb 2023 06:30:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c3e71af02bd3ac98dc210063a99e13fcaaa8af0ccfa5888c222c457521a510`  
		Last Modified: Sat, 11 Feb 2023 06:31:37 GMT  
		Size: 28.1 MB (28145518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d996569f03d45239f7b2250bee17114ce7a32708fe8b1c87dfa112f60ee73f`  
		Last Modified: Sat, 11 Feb 2023 06:31:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3225dff5f23b3b693f11a9a8233a56789742fec856ee479bbb008529881d44`  
		Last Modified: Sat, 11 Feb 2023 13:00:06 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e113c0612ef377638ad26a1ca2f71e97757315864af495b81aa0c12a108abe`  
		Last Modified: Sat, 11 Feb 2023 13:00:18 GMT  
		Size: 82.1 MB (82056795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62e1f130b77f17993588c32e85a6121f28db022496891034eb5210346ab374b`  
		Last Modified: Sat, 11 Feb 2023 13:00:02 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3edcd1f419c581be61f65a1775f0ac9e4155409fad26c95ac0e76ccf148b5bb`  
		Last Modified: Sat, 11 Feb 2023 13:00:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31656fc11a7405a85d01e0996152c655d839a4b7ac8bb31219a1fc810035ed56`  
		Last Modified: Sat, 11 Feb 2023 13:00:03 GMT  
		Size: 3.1 MB (3143525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aed495d4aa7b57b779ac3f09e3f49b5e0b7a1f30a88748e77870fc80f6da2b1`  
		Last Modified: Sat, 11 Feb 2023 13:00:12 GMT  
		Size: 68.1 MB (68084586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fc1f13ef9fd83e62fa1b7d1eab356afe4e3e353d59ed47735c07019ba3c127`  
		Last Modified: Sat, 11 Feb 2023 13:00:02 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.16` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:8567033f976173da65393fc58febcfa0c4eb0b636f865f392a5aa368be21d7f9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195520342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c3aa7785b6dbc3e7899858c5d69b2c2d16b66a9ff7c35eeb248d2101c8d1ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:24:39 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 11 Feb 2023 05:24:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 11 Feb 2023 05:24:40 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 05:29:01 GMT
ENV RUBY_MAJOR=3.1
# Sat, 11 Feb 2023 05:29:01 GMT
ENV RUBY_VERSION=3.1.3
# Sat, 11 Feb 2023 05:29:01 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Sat, 11 Feb 2023 05:30:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 11 Feb 2023 05:30:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 11 Feb 2023 05:30:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 11 Feb 2023 05:30:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 05:30:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 11 Feb 2023 05:30:47 GMT
CMD ["irb"]
# Sat, 11 Feb 2023 08:47:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 11 Feb 2023 08:47:40 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 11 Feb 2023 08:47:41 GMT
ENV RAILS_ENV=production
# Sat, 11 Feb 2023 08:47:42 GMT
WORKDIR /usr/src/redmine
# Sat, 11 Feb 2023 08:47:42 GMT
ENV HOME=/home/redmine
# Sat, 11 Feb 2023 08:47:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 11 Feb 2023 08:47:42 GMT
ENV REDMINE_VERSION=5.0.4
# Sat, 11 Feb 2023 08:47:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.4.tar.gz
# Sat, 11 Feb 2023 08:47:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=39436f5f8d26f5b7ce17e79903a3112e556e924da4f51c05b57f5defbe6f2924
# Sat, 11 Feb 2023 08:47:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 11 Feb 2023 08:47:46 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 11 Feb 2023 08:49:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 11 Feb 2023 08:49:23 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 11 Feb 2023 08:49:23 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Sat, 11 Feb 2023 08:49:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 08:49:23 GMT
EXPOSE 3000
# Sat, 11 Feb 2023 08:49:23 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ae7b7f5917829253477e9642f2e3c23ec4e6a33f1ae179614c91f494467276`  
		Last Modified: Sat, 11 Feb 2023 05:36:32 GMT  
		Size: 3.8 MB (3821424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b4911b6d1550a57612d9b499d0be2d7a2118c74eb55879e24b81293e1598c`  
		Last Modified: Sat, 11 Feb 2023 05:36:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c51d6d874baf488729dfe61bbdce951d31f6260d36d4ce5daab30a3879ef096`  
		Last Modified: Sat, 11 Feb 2023 05:37:09 GMT  
		Size: 28.7 MB (28704392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b191d91f98afa72d4fbf85fd9f1f589571b0888591d855eaf8e69d7fea41da`  
		Last Modified: Sat, 11 Feb 2023 05:37:06 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0077d6f6189e0c3efbca9d4dc9ad1792ec95dbe3ebb0e34ce017f7595295f`  
		Last Modified: Sat, 11 Feb 2023 08:52:23 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a1b0a2518e1d97c1a12ef83c36f243633e8be64b592c738660d1391530b2a`  
		Last Modified: Sat, 11 Feb 2023 08:52:32 GMT  
		Size: 87.3 MB (87292751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2506857d1f04329a0725a514a747b5f5fce679027a07604cd8de827acd61dc27`  
		Last Modified: Sat, 11 Feb 2023 08:52:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf0dcb764cdac1a39add787f8d3cd6c37fee6869ab688780346777571b858bf`  
		Last Modified: Sat, 11 Feb 2023 08:52:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234a9857ee8b5e57bc0795122d863b867b2144aa744782ef457af676866375dc`  
		Last Modified: Sat, 11 Feb 2023 08:52:22 GMT  
		Size: 3.1 MB (3143918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65e3df86c152caf47a3affe7599fc6b062074180be95af3c16de4f44a151c0d`  
		Last Modified: Sat, 11 Feb 2023 08:52:27 GMT  
		Size: 69.8 MB (69844415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533ceff7ecdf2af62153a48d33fd604f41bcd941cb704377e92aaa543f5ebd5b`  
		Last Modified: Sat, 11 Feb 2023 08:52:21 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.16` - linux; 386

```console
$ docker pull redmine@sha256:9c839dcb91eb004ec21d58c016fcbd94c6eddbebb833d402a7981faa87c0d084
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197024730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9aed0d1f9e33de9ee4652a064a525bfcf12f3998041b64246f0dcca02c9947c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:50:58 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 11 Feb 2023 02:50:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 11 Feb 2023 02:51:00 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 02:56:35 GMT
ENV RUBY_MAJOR=3.1
# Sat, 11 Feb 2023 02:56:36 GMT
ENV RUBY_VERSION=3.1.3
# Sat, 11 Feb 2023 02:56:37 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Sat, 11 Feb 2023 02:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 11 Feb 2023 02:59:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 11 Feb 2023 02:59:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 11 Feb 2023 02:59:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 02:59:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 11 Feb 2023 02:59:18 GMT
CMD ["irb"]
# Sat, 11 Feb 2023 06:13:29 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 11 Feb 2023 06:13:43 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 11 Feb 2023 06:13:43 GMT
ENV RAILS_ENV=production
# Sat, 11 Feb 2023 06:13:44 GMT
WORKDIR /usr/src/redmine
# Sat, 11 Feb 2023 06:13:45 GMT
ENV HOME=/home/redmine
# Sat, 11 Feb 2023 06:13:46 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 11 Feb 2023 06:13:47 GMT
ENV REDMINE_VERSION=5.0.4
# Sat, 11 Feb 2023 06:13:48 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.4.tar.gz
# Sat, 11 Feb 2023 06:13:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=39436f5f8d26f5b7ce17e79903a3112e556e924da4f51c05b57f5defbe6f2924
# Sat, 11 Feb 2023 06:13:53 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 11 Feb 2023 06:13:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 11 Feb 2023 06:16:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 11 Feb 2023 06:16:02 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 11 Feb 2023 06:16:04 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Sat, 11 Feb 2023 06:16:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 06:16:05 GMT
EXPOSE 3000
# Sat, 11 Feb 2023 06:16:06 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1416fc91caee0c7817d833d6739231333235ca13f61b6ad0772c5ef8fdd23956`  
		Last Modified: Sat, 11 Feb 2023 03:08:33 GMT  
		Size: 3.9 MB (3886364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493c0c37c1d6df761dd11dc67d7b213d99cb6a346137f0a196a6c0057cb395e`  
		Last Modified: Sat, 11 Feb 2023 03:08:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e106464e50bc0d9b6a8be13ab22804b94ce8c97f42acf18caa19a20e49d1ad6`  
		Last Modified: Sat, 11 Feb 2023 03:09:22 GMT  
		Size: 28.1 MB (28119653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfb208be063b6fe08494e604ed83ab6553056465137731f0a7b2f7a899d9590`  
		Last Modified: Sat, 11 Feb 2023 03:09:19 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f896a0442252246e34510b45e7fd190a4f180bee6f5a318b1a87ba6158be75ba`  
		Last Modified: Sat, 11 Feb 2023 06:20:13 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d338b207c9d5e5d194d988617f3c1e089fcff7275e46ce2ebee0af2bf5eefa80`  
		Last Modified: Sat, 11 Feb 2023 06:20:26 GMT  
		Size: 90.3 MB (90296113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd3b73572cac52d0c7794167c4273f2bd562267530ad64eab71cf47e28eda78`  
		Last Modified: Sat, 11 Feb 2023 06:20:11 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1838e30da3380d037ef00a0940b9f413e607b8bd95bc0a8a2677daddbeb5055c`  
		Last Modified: Sat, 11 Feb 2023 06:20:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06641c9df9a1677c22afea0c4e2691551685ef49b794e080dbf80aa3e65bda8`  
		Last Modified: Sat, 11 Feb 2023 06:20:12 GMT  
		Size: 3.1 MB (3143760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acb030f54d12c0cb12af792ba1cfa626c87cca7d723a1bcfe68b07c088c1b6d`  
		Last Modified: Sat, 11 Feb 2023 06:20:22 GMT  
		Size: 68.8 MB (68764378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5213b607c59f50c8b8af1290d9c61102266338215436ca38c2670e5c5e52288d`  
		Last Modified: Sat, 11 Feb 2023 06:20:11 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.16` - linux; ppc64le

```console
$ docker pull redmine@sha256:e3b1821074789ae01c59107c9c272e0d069f16472322704f9397b52c5891aab8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206750911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c637ba07733b0d55a573a17473c6e1a67e0fee7e4c329a675e4f5783ff1411`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:07:34 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 11 Feb 2023 05:07:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 11 Feb 2023 05:07:37 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 05:15:47 GMT
ENV RUBY_MAJOR=3.1
# Sat, 11 Feb 2023 05:15:48 GMT
ENV RUBY_VERSION=3.1.3
# Sat, 11 Feb 2023 05:15:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Sat, 11 Feb 2023 05:19:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 11 Feb 2023 05:19:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 11 Feb 2023 05:19:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 11 Feb 2023 05:19:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 05:19:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 11 Feb 2023 05:19:55 GMT
CMD ["irb"]
# Sat, 11 Feb 2023 12:53:49 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 11 Feb 2023 12:54:19 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 11 Feb 2023 12:54:23 GMT
ENV RAILS_ENV=production
# Sat, 11 Feb 2023 12:54:23 GMT
WORKDIR /usr/src/redmine
# Sat, 11 Feb 2023 12:54:24 GMT
ENV HOME=/home/redmine
# Sat, 11 Feb 2023 12:54:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 11 Feb 2023 12:54:26 GMT
ENV REDMINE_VERSION=5.0.4
# Sat, 11 Feb 2023 12:54:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.4.tar.gz
# Sat, 11 Feb 2023 12:54:27 GMT
ENV REDMINE_DOWNLOAD_SHA256=39436f5f8d26f5b7ce17e79903a3112e556e924da4f51c05b57f5defbe6f2924
# Sat, 11 Feb 2023 12:54:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 11 Feb 2023 12:54:34 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 11 Feb 2023 12:58:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 11 Feb 2023 12:58:32 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 11 Feb 2023 12:58:32 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Sat, 11 Feb 2023 12:58:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 12:58:34 GMT
EXPOSE 3000
# Sat, 11 Feb 2023 12:58:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d1835bdc86ca722641491b8c05548ca1f17a52cc1d2d4f0aeb4abcc43cea0`  
		Last Modified: Sat, 11 Feb 2023 05:31:35 GMT  
		Size: 4.0 MB (3973616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1cd4eb351e56ba7e4fbe068d8f88ebb2fa8b6fc8b162f8896fbb12f5baf3dc`  
		Last Modified: Sat, 11 Feb 2023 05:31:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f59468b845721d3f7d411c9ee83aef16b26bc6790535520a5242a0d9ae2c35a`  
		Last Modified: Sat, 11 Feb 2023 05:32:32 GMT  
		Size: 29.5 MB (29517487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45df66a1d71856e3cac53e9e15e404719c6b60f77a9d8fdadf86d1dd30311259`  
		Last Modified: Sat, 11 Feb 2023 05:32:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bcbd47603460add4c7423a07973950c38e2bf2e310a03a74555659a6da5bc3`  
		Last Modified: Sat, 11 Feb 2023 13:05:19 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a33833b9c8729972df1ad4bfe6f3c874e5fc5bf70d19f3cd5ee7bd418986e02`  
		Last Modified: Sat, 11 Feb 2023 13:05:43 GMT  
		Size: 96.3 MB (96318022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69189681e3f0f084375722142f17fcf76da532258cae113d76d965dfe0557771`  
		Last Modified: Sat, 11 Feb 2023 13:05:16 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e5f33d0c40ba5e732d391fad4d05b8ff8b5adf6d716ca1de350ea98c587399`  
		Last Modified: Sat, 11 Feb 2023 13:05:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdd58e09dbb71739fe280a3b680dc7ff5a1b302e1552f1c896f2f7ac7b9038c`  
		Last Modified: Sat, 11 Feb 2023 13:05:18 GMT  
		Size: 3.1 MB (3143931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892b73b40e1b57cc7319089d1a8fc50f582d6ccdaf279b17301cda490dd04972`  
		Last Modified: Sat, 11 Feb 2023 13:05:29 GMT  
		Size: 71.0 MB (70989292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbd0e306095df79ee9d5bc2309cdfc01fabe33ca21e312412348004b10110ba`  
		Last Modified: Sat, 11 Feb 2023 13:05:16 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.16` - linux; s390x

```console
$ docker pull redmine@sha256:bb4515db785032fdb38ea647e19f5a015b74a21571ffb0e5dc6aa2725879930e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189913892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0d4a13af1735e0ff1c4c3f3c422ac224caf2812855a69aff64e63b8e6e93bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 10:50:29 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Sat, 11 Feb 2023 10:50:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 11 Feb 2023 10:50:30 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 10:56:36 GMT
ENV RUBY_MAJOR=3.1
# Sat, 11 Feb 2023 10:56:37 GMT
ENV RUBY_VERSION=3.1.3
# Sat, 11 Feb 2023 10:56:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4ee161939826bcdfdafa757cf8e293a7f14e357f62be7144f040335cc8c7371a
# Sat, 11 Feb 2023 11:00:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 11 Feb 2023 11:00:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 11 Feb 2023 11:00:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 11 Feb 2023 11:00:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 11:00:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 11 Feb 2023 11:00:24 GMT
CMD ["irb"]
# Sat, 11 Feb 2023 12:56:29 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 11 Feb 2023 12:56:40 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 11 Feb 2023 12:56:44 GMT
ENV RAILS_ENV=production
# Sat, 11 Feb 2023 12:56:44 GMT
WORKDIR /usr/src/redmine
# Sat, 11 Feb 2023 12:56:44 GMT
ENV HOME=/home/redmine
# Sat, 11 Feb 2023 12:56:45 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 11 Feb 2023 12:56:45 GMT
ENV REDMINE_VERSION=5.0.4
# Sat, 11 Feb 2023 12:56:45 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.4.tar.gz
# Sat, 11 Feb 2023 12:56:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=39436f5f8d26f5b7ce17e79903a3112e556e924da4f51c05b57f5defbe6f2924
# Sat, 11 Feb 2023 12:56:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 11 Feb 2023 12:56:48 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 11 Feb 2023 12:58:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 11 Feb 2023 12:58:34 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 11 Feb 2023 12:58:34 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Sat, 11 Feb 2023 12:58:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 11 Feb 2023 12:58:34 GMT
EXPOSE 3000
# Sat, 11 Feb 2023 12:58:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdc9ea63066cf1780bbe5fb37efb05fc41715ccf7d1d4ada643b9980615fb10`  
		Last Modified: Sat, 11 Feb 2023 11:08:24 GMT  
		Size: 3.9 MB (3941065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b409ba260ab77b4a8e266f8ecc6dbe5fed29ada1c062c2a6195dd869bbc20e94`  
		Last Modified: Sat, 11 Feb 2023 11:08:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad51e92f4adea8480df38fc926f55cebec15a6449ba559d1a01836c7b02b852`  
		Last Modified: Sat, 11 Feb 2023 11:08:57 GMT  
		Size: 28.9 MB (28925746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c98da3154b547b96cb681e39a11ddb27a6cff8ced0f57908953b380e4b7921`  
		Last Modified: Sat, 11 Feb 2023 11:08:55 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c34610d6737207598e4178243778113f54caf75f86b36628dba2fab68865f7`  
		Last Modified: Sat, 11 Feb 2023 13:02:12 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf55dd28f8bf9d11c98c6dfcb3ad469c476a9fdd30c7b23168af945c1905d1cc`  
		Last Modified: Sat, 11 Feb 2023 13:02:22 GMT  
		Size: 80.9 MB (80872264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f59274ea240b3b09183178abb33cc06452fab76f3155fdad640f7afa7a379`  
		Last Modified: Sat, 11 Feb 2023 13:02:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fe333c8886328846675e7397d427acf7296bb49eb73c8aaf1d03a3bf85c03a`  
		Last Modified: Sat, 11 Feb 2023 13:02:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec242f209e5b2845d696131321f47345533b7454a441401da8ab0d00e9469f6`  
		Last Modified: Sat, 11 Feb 2023 13:02:11 GMT  
		Size: 3.1 MB (3143933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5ae367b34e674c5460a09fe8c6ff95096b89c1efe18aeff1d1fc35686df6a7`  
		Last Modified: Sat, 11 Feb 2023 13:02:17 GMT  
		Size: 70.4 MB (70433364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d7c4da35065c2e26a344f8897c582585bf52f2e930061abdb0b55452c9df39`  
		Last Modified: Sat, 11 Feb 2023 13:02:10 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
