## `redmine:alpine`

```console
$ docker pull redmine@sha256:ca0b18a629a5e414e76848f03ea611afb70fcea36a6e952480a8b20f33ccb0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:077c21637afe6f40bc01e53144e4d29b1ab559347fce7534c68f67e69ca64300
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150053498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313842d3e7f7deacfdfb873ef360b7bee175c2f72c64049ca5a88b81134fd3e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:07:29 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 15 Apr 2021 03:07:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Apr 2021 03:07:31 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 03:16:27 GMT
ENV RUBY_MAJOR=2.7
# Wed, 07 Jul 2021 19:45:51 GMT
ENV RUBY_VERSION=2.7.4
# Wed, 07 Jul 2021 19:45:51 GMT
ENV RUBY_DOWNLOAD_SHA256=2a80824e0ad6100826b69b9890bf55cfc4cf2b61a1e1330fccbcb30c46cef8d7
# Wed, 07 Jul 2021 19:48:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 07 Jul 2021 19:48:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Jul 2021 19:48:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Jul 2021 19:48:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jul 2021 19:48:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 07 Jul 2021 19:48:40 GMT
CMD ["irb"]
# Wed, 07 Jul 2021 20:42:35 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 07 Jul 2021 20:42:49 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 07 Jul 2021 20:42:50 GMT
ENV RAILS_ENV=production
# Wed, 07 Jul 2021 20:42:51 GMT
WORKDIR /usr/src/redmine
# Wed, 07 Jul 2021 20:42:51 GMT
ENV HOME=/home/redmine
# Wed, 07 Jul 2021 20:42:53 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 07 Jul 2021 20:42:54 GMT
ENV REDMINE_VERSION=4.2.1
# Wed, 07 Jul 2021 20:42:54 GMT
ENV REDMINE_DOWNLOAD_SHA256=ad4109c3425f1cfe4c8961f6ae6494c76e20d81ed946caa1e297d9eda13b41b4
# Wed, 07 Jul 2021 20:43:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 07 Jul 2021 20:43:00 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 07 Jul 2021 20:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 07 Jul 2021 20:46:18 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 07 Jul 2021 20:46:18 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Wed, 07 Jul 2021 20:46:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 07 Jul 2021 20:46:19 GMT
EXPOSE 3000
# Wed, 07 Jul 2021 20:46:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a867505730167ce0636f0811cb765ebbde11bf979c1a9839f6915f2fc3b85b`  
		Last Modified: Thu, 15 Apr 2021 03:39:41 GMT  
		Size: 1.2 MB (1218679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c77620f6108dc0610cba72f77d68c271fb1b14cb0800a7a8b6aaeb8950fec9`  
		Last Modified: Thu, 15 Apr 2021 03:39:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea934b6bf2094b677c0efcea21d8dd83f7d08a693dc70f6225655637126c426`  
		Last Modified: Wed, 07 Jul 2021 20:19:57 GMT  
		Size: 16.7 MB (16721809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686808441e8cf9ef056302eb927f0082e5b1982f069e2c30b2b19d6a61c2a2ba`  
		Last Modified: Wed, 07 Jul 2021 20:19:55 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8976df4a5a54a897431b41d52944416dd3f8f810bd6657691c18453f8487742`  
		Last Modified: Wed, 07 Jul 2021 21:00:05 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47efa0102f6e6e0ece259209ca18d6e3d4e11169b4d4f46aba1eba740a613150`  
		Last Modified: Wed, 07 Jul 2021 21:00:15 GMT  
		Size: 69.5 MB (69525641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31feb1eca5d1e845e9715e85cd7a862fd44f1760b6e75121aa5683d8292ae651`  
		Last Modified: Wed, 07 Jul 2021 21:00:01 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad06f01400240338ee40ad58bfca6b7cc4a9a01936123ffe0b9915471107c362`  
		Last Modified: Wed, 07 Jul 2021 21:00:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773f42416bef575288101a1df9d6a5fa2148c53ad0ab570bfbe4f59df70a3de5`  
		Last Modified: Wed, 07 Jul 2021 21:00:03 GMT  
		Size: 3.1 MB (3059999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dc43767f453dd8f05fceda480269b93353a0571cdbcda70dd10ef97bbc6f8a`  
		Last Modified: Wed, 07 Jul 2021 21:00:08 GMT  
		Size: 56.7 MB (56711679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cd8e62dc154735785f51beaabe48d17609389a1a6c0754d076fb36884292b6`  
		Last Modified: Wed, 07 Jul 2021 21:00:01 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
