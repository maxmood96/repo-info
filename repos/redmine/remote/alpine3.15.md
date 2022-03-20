## `redmine:alpine3.15`

```console
$ docker pull redmine@sha256:ccb7e4f0772ee87a76d0630f979e4caf9208c550de8420550c2145cb8d84a866
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

### `redmine:alpine3.15` - linux; amd64

```console
$ docker pull redmine@sha256:f7653fa5ae805994cfeb6ad33d9f467c2425e194c9ed9112fa6e6146a8ca44ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161555003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d66b765de5921655cb6ca15e41e4b03de9f3c304ecd03f2b2f6fa98ab867948`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 14:27:00 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 14:27:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 14:27:01 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 14:55:55 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Mar 2022 14:55:55 GMT
ENV RUBY_VERSION=2.7.5
# Thu, 17 Mar 2022 14:55:55 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Thu, 17 Mar 2022 15:00:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 15:00:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 15:00:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 15:00:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 15:00:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 15:00:03 GMT
CMD ["irb"]
# Sat, 19 Mar 2022 00:14:35 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 19 Mar 2022 00:14:44 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 19 Mar 2022 00:14:45 GMT
ENV RAILS_ENV=production
# Sat, 19 Mar 2022 00:14:45 GMT
WORKDIR /usr/src/redmine
# Sat, 19 Mar 2022 00:14:45 GMT
ENV HOME=/home/redmine
# Sat, 19 Mar 2022 00:14:46 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 19 Mar 2022 00:14:46 GMT
ENV REDMINE_VERSION=4.2.4
# Sat, 19 Mar 2022 00:14:46 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.4.tar.gz
# Sat, 19 Mar 2022 00:14:46 GMT
ENV REDMINE_DOWNLOAD_SHA256=cf649f5d4ff783582f82bebd4a5099ef63acb3d5573bbe6b4bf64f293c61c9ce
# Sat, 19 Mar 2022 00:14:49 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 19 Mar 2022 00:14:50 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 19 Mar 2022 00:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 19 Mar 2022 00:17:51 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 19 Mar 2022 00:17:52 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 19 Mar 2022 00:17:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 00:17:52 GMT
EXPOSE 3000
# Sat, 19 Mar 2022 00:17:52 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8acccb3efb020053af541ecf53824003c90cc0e63740f8c9f009137f23050`  
		Last Modified: Thu, 17 Mar 2022 15:15:27 GMT  
		Size: 3.7 MB (3683188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08aefcf7c3b7e112b23c386ac81455ecdcc14c7b9c04ce64cd16409fccc5e01d`  
		Last Modified: Thu, 17 Mar 2022 15:15:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa6e573377981c856fdee2631135d45be73d7035904ab777d2b6acbfe1002cb`  
		Last Modified: Thu, 17 Mar 2022 15:17:30 GMT  
		Size: 14.0 MB (13975360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b292bf0cef779919cdb12e282a57b2671204c6d532dd957d972d2b05ce3b21b`  
		Last Modified: Thu, 17 Mar 2022 15:17:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1a7355b9c6d27d6ead0660b23bb2a61173d5585c7da53d40eb296edb259704`  
		Last Modified: Sat, 19 Mar 2022 00:25:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3146452d548c06790029958197748005e5a56d935171a57b331a8e10f0dd466`  
		Last Modified: Sat, 19 Mar 2022 00:25:38 GMT  
		Size: 82.2 MB (82232437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4ef2ef08e07e620c2369d2b14ddb9aac0e8a8f37b991b7f859fbcd15df85c9`  
		Last Modified: Sat, 19 Mar 2022 00:25:23 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de7a777d86f7471d8e20ce278f552fb7df5a5f6f35687e1709fc6e959ce3543`  
		Last Modified: Sat, 19 Mar 2022 00:25:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a35dd0b8b65b5432460e55984c5ad4704ed9713a3c410fdfb152054c4129fc`  
		Last Modified: Sat, 19 Mar 2022 00:25:24 GMT  
		Size: 3.1 MB (3065423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ee51c08c619ea94c83512b4397d0a670d904b11ac65f2439f43e4877df122f`  
		Last Modified: Sat, 19 Mar 2022 00:25:29 GMT  
		Size: 55.8 MB (55782217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6912cf5680302f8363054ee424471cec794d2740601a5d4a91af4895d45a10`  
		Last Modified: Sat, 19 Mar 2022 00:25:23 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.15` - linux; arm variant v6

```console
$ docker pull redmine@sha256:dd043a493e91358b319b3ce1d5b3f4e3eb0e97ea361aff5e1da7711c4617df7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155159568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400fccc51651b390a2beca7dbb029ecadc20c380e45ee9e4379fa0e4e19a191b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 02:26:45 GMT
ADD file:9c8618405ef54d562132919ffe49c862d014b402e0e4813b87bf01574fa04c0e in / 
# Thu, 17 Mar 2022 02:26:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 10:30:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 10:30:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 10:30:19 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 10:39:50 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Mar 2022 10:39:50 GMT
ENV RUBY_VERSION=2.7.5
# Thu, 17 Mar 2022 10:39:51 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Thu, 17 Mar 2022 10:43:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 10:43:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 10:43:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 10:43:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 10:43:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 10:43:36 GMT
CMD ["irb"]
# Thu, 17 Mar 2022 14:05:02 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Thu, 17 Mar 2022 14:05:34 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Thu, 17 Mar 2022 14:05:35 GMT
ENV RAILS_ENV=production
# Thu, 17 Mar 2022 14:05:36 GMT
WORKDIR /usr/src/redmine
# Thu, 17 Mar 2022 14:05:36 GMT
ENV HOME=/home/redmine
# Thu, 17 Mar 2022 14:05:38 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 17 Mar 2022 14:05:39 GMT
ENV REDMINE_VERSION=4.2.4
# Thu, 17 Mar 2022 14:05:39 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.4.tar.gz
# Thu, 17 Mar 2022 14:05:39 GMT
ENV REDMINE_DOWNLOAD_SHA256=cf649f5d4ff783582f82bebd4a5099ef63acb3d5573bbe6b4bf64f293c61c9ce
# Thu, 17 Mar 2022 14:05:46 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 17 Mar 2022 14:05:47 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 17 Mar 2022 14:11:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 17 Mar 2022 14:11:54 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 17 Mar 2022 14:11:55 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Thu, 17 Mar 2022 14:11:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 17 Mar 2022 14:11:56 GMT
EXPOSE 3000
# Thu, 17 Mar 2022 14:11:56 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:787f016efa9bc7812361be134f731e845b97fba19169cf3615e7048c0412380e`  
		Last Modified: Thu, 17 Mar 2022 02:28:24 GMT  
		Size: 2.6 MB (2624973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d86fb78a99c7d753906b56698b6744862b220df1afa71da7d3136884e3eb5c`  
		Last Modified: Thu, 17 Mar 2022 10:50:41 GMT  
		Size: 3.4 MB (3431374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e167efa5b19ea8438bf77dea2c30de42fd74979c87afffbc36fa4edd5a93d22f`  
		Last Modified: Thu, 17 Mar 2022 10:50:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c04fa4fd83c3a9f870a023715b8ccb8536f1ac770f78725ed2d0cff21044a3b`  
		Last Modified: Thu, 17 Mar 2022 10:52:08 GMT  
		Size: 13.4 MB (13411675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ef5862dcc0eee867a99ab647ab37f443232c4f3eccf126e42ebdfae05b9773`  
		Last Modified: Thu, 17 Mar 2022 10:52:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dbd2ec139009d44a43553bcca78588be3171e5ea72148eada2a6853d36aa44`  
		Last Modified: Thu, 17 Mar 2022 14:20:05 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5c7f502f4b33ac3ab9ab874712d011aa7443ce1e0e08f425016b98d0c3dcd1`  
		Last Modified: Thu, 17 Mar 2022 14:20:57 GMT  
		Size: 77.7 MB (77697029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7992a6c48be5293a1e6f03e42652230e5fd7bae74f24100e2e4ebe3343b72b81`  
		Last Modified: Thu, 17 Mar 2022 14:20:03 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f28fe74484fff9b17d0ecf89b5bca4724da05c5a98f26426be3e2ddd854c5d`  
		Last Modified: Thu, 17 Mar 2022 14:20:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed535d45b1be1af4fa47729755b211a8fe7bf42b6f26244ee7c83ff9c923862`  
		Last Modified: Thu, 17 Mar 2022 14:20:07 GMT  
		Size: 3.1 MB (3065468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505cdce6a91dec93a572074689b8ef510c2b77c4c16229520f9f4032ce6553c9`  
		Last Modified: Thu, 17 Mar 2022 14:20:27 GMT  
		Size: 54.9 MB (54925311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4e8323b249942696f614a7d8e91d898e1357f7c1ab016014cfda4b807aecbc`  
		Last Modified: Thu, 17 Mar 2022 14:20:03 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.15` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0f50093880344bf80c3d1438ade36d91767ebfd3b0204664bade3cba9c5733e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150992884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca45955c416e040fa99cdf3d6c5eb4af8522d81c97551b34100c227de530aa43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 09:26:34 GMT
ADD file:01e87d7f83dfb32fd8a1b7b889b923432c2e0516d79a4196e01ad0ad15e33d68 in / 
# Thu, 17 Mar 2022 09:26:35 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 12:46:45 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 18 Mar 2022 12:46:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 18 Mar 2022 12:46:47 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 13:23:12 GMT
ENV RUBY_MAJOR=2.7
# Fri, 18 Mar 2022 13:23:12 GMT
ENV RUBY_VERSION=2.7.5
# Fri, 18 Mar 2022 13:23:13 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Fri, 18 Mar 2022 13:26:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 18 Mar 2022 13:26:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 18 Mar 2022 13:26:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 18 Mar 2022 13:26:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 13:26:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 18 Mar 2022 13:26:29 GMT
CMD ["irb"]
# Sun, 20 Mar 2022 08:41:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sun, 20 Mar 2022 08:42:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sun, 20 Mar 2022 08:42:08 GMT
ENV RAILS_ENV=production
# Sun, 20 Mar 2022 08:42:08 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Mar 2022 08:42:09 GMT
ENV HOME=/home/redmine
# Sun, 20 Mar 2022 08:42:10 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 20 Mar 2022 08:42:11 GMT
ENV REDMINE_VERSION=4.2.4
# Sun, 20 Mar 2022 08:42:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.4.tar.gz
# Sun, 20 Mar 2022 08:42:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=cf649f5d4ff783582f82bebd4a5099ef63acb3d5573bbe6b4bf64f293c61c9ce
# Sun, 20 Mar 2022 08:42:18 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 20 Mar 2022 08:42:18 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 20 Mar 2022 08:47:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sun, 20 Mar 2022 08:47:52 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Mar 2022 08:47:53 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sun, 20 Mar 2022 08:47:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Mar 2022 08:47:54 GMT
EXPOSE 3000
# Sun, 20 Mar 2022 08:47:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:205cbce5da6d59acc17b2db4c1af7903ca3497b99d4bedb94ef66ace17303808`  
		Last Modified: Thu, 17 Mar 2022 09:28:11 GMT  
		Size: 2.4 MB (2427136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c448fcf852ff74132598a3fc9c1d9062229c9638a868d718658346cd3ea9f`  
		Last Modified: Fri, 18 Mar 2022 13:55:36 GMT  
		Size: 3.3 MB (3301669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a394b09c79da30d9c85a2e6f6cf1d6dd153a2ca93db2860b7092695551417f99`  
		Last Modified: Fri, 18 Mar 2022 13:55:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffacaa21d629e12f842c0b39a328075bc081ff9f9be1362ad24373d4864c3b6`  
		Last Modified: Fri, 18 Mar 2022 13:59:58 GMT  
		Size: 13.3 MB (13296975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e72766d6db30c3b8da3ea8ceea26dada40a5dcaea21df062e7dfbe2e4da6e6`  
		Last Modified: Fri, 18 Mar 2022 13:59:51 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2be221ad9378ee876646aca85104f521383000a6bcc0fd683616942274b1955`  
		Last Modified: Sun, 20 Mar 2022 09:04:55 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00649eda5d25aad94a482e2f7cac40c11576da8e37d6ab2a6954660c5d005b94`  
		Last Modified: Sun, 20 Mar 2022 09:05:43 GMT  
		Size: 74.3 MB (74254952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5f8971006ce8205d675930cdc145a44eac07ba349840bed80439a9dc18fc47`  
		Last Modified: Sun, 20 Mar 2022 09:04:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4e0dcf6947fc28635324d8d03e8df50a661c71d92ee234ee778036fcda01bf`  
		Last Modified: Sun, 20 Mar 2022 09:04:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fecbe42c8e2f625199c4169af5263391d4806e374ca3fe9670e98df7fe1bcd`  
		Last Modified: Sun, 20 Mar 2022 09:04:58 GMT  
		Size: 3.1 MB (3065488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568d476cb2bc3da70a6fefed65e3eab95c58bac706f48f299d969bb0eda790f0`  
		Last Modified: Sun, 20 Mar 2022 09:05:18 GMT  
		Size: 54.6 MB (54642923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40d80b5464967337d294986a9a1bb088f753f62b2c476dd1d94134677230238`  
		Last Modified: Sun, 20 Mar 2022 09:04:54 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:212460f5c127e3a051b360bede2dfedf660e00e849adf54342daa416c1f73834
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158351963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d8d13bdeb86c3fa06d04da3e4f957edeb5218edb432afc9b7128046dce169a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 20:16:28 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 20:16:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 20:16:29 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 20:35:21 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Mar 2022 20:35:22 GMT
ENV RUBY_VERSION=2.7.5
# Thu, 17 Mar 2022 20:35:23 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Thu, 17 Mar 2022 20:37:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 20:37:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 20:37:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 20:37:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 20:37:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 20:37:16 GMT
CMD ["irb"]
# Sat, 19 Mar 2022 02:13:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 19 Mar 2022 02:13:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 19 Mar 2022 02:13:34 GMT
ENV RAILS_ENV=production
# Sat, 19 Mar 2022 02:13:35 GMT
WORKDIR /usr/src/redmine
# Sat, 19 Mar 2022 02:13:36 GMT
ENV HOME=/home/redmine
# Sat, 19 Mar 2022 02:13:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 19 Mar 2022 02:13:38 GMT
ENV REDMINE_VERSION=4.2.4
# Sat, 19 Mar 2022 02:13:39 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.4.tar.gz
# Sat, 19 Mar 2022 02:13:40 GMT
ENV REDMINE_DOWNLOAD_SHA256=cf649f5d4ff783582f82bebd4a5099ef63acb3d5573bbe6b4bf64f293c61c9ce
# Sat, 19 Mar 2022 02:13:44 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 19 Mar 2022 02:13:45 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 19 Mar 2022 02:16:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 19 Mar 2022 02:16:16 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 19 Mar 2022 02:16:17 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 19 Mar 2022 02:16:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 02:16:19 GMT
EXPOSE 3000
# Sat, 19 Mar 2022 02:16:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b561929b98bc2bab1fe6e7d49e11c339a92c2fe7e3548600b5415a886f46c23`  
		Last Modified: Thu, 17 Mar 2022 20:52:20 GMT  
		Size: 3.6 MB (3645712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36a92d636c972c8909b17c81864135482e808fea38542da2d7c0556a246e86e`  
		Last Modified: Thu, 17 Mar 2022 20:52:20 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a896a33f8a4c6e648a2242a339c6c8d52c0cb9535e394c052f51c2e00a3ec39c`  
		Last Modified: Thu, 17 Mar 2022 20:55:15 GMT  
		Size: 13.8 MB (13808110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850bff33e1d86d150e5bdaa9c1238c282becb6310de9b1d32ef019a3d3a2cf02`  
		Last Modified: Thu, 17 Mar 2022 20:55:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c44659d2c3b0297111110beadec18e7a34fc3a77ec80d5ee2b1d187aff19244`  
		Last Modified: Sat, 19 Mar 2022 02:24:04 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0dae3c2a4703830090806c4abb55b47b839b84be7e4648c1f82ebd3bbd4376`  
		Last Modified: Sat, 19 Mar 2022 02:24:15 GMT  
		Size: 79.5 MB (79472727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feabbe143b613583b4c95377db0ed3ad3f69530cfc721518ff129b3551898c30`  
		Last Modified: Sat, 19 Mar 2022 02:24:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fa8bc590dcd42e4280a6a9f0425a9d32404a8a7ac3fd3027e11c87e314c749`  
		Last Modified: Sat, 19 Mar 2022 02:24:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943905590b1306b98fdbff7fba70d6d4dfaf8f80089bb44fa6a75fe5402596d0`  
		Last Modified: Sat, 19 Mar 2022 02:24:02 GMT  
		Size: 3.1 MB (3065449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c789ef68b6f566e0ab0dd749a4cf12d096ef7cbed9dddb1760589dc77225e5`  
		Last Modified: Sat, 19 Mar 2022 02:24:07 GMT  
		Size: 55.6 MB (55641541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ef0e817a59c96f81c9f62339905296c0a7192ad86613729f3279c0d2b442c1`  
		Last Modified: Sat, 19 Mar 2022 02:24:01 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.15` - linux; 386

```console
$ docker pull redmine@sha256:62d39932193e608039b286f18702b0f68c6260748e88d398f52ab851a4d5f23d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161725715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515efd6130e6e6685436de044fa69f6533e0029dd2edc18bb39b99f993f025ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 08:13:03 GMT
ADD file:22216bc654d9177244235f242fa83cae3b283b3c145cad7ccf11c0d29f5f0ff2 in / 
# Thu, 17 Mar 2022 08:13:03 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 20:18:37 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 20:18:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 20:18:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 21:00:05 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Mar 2022 21:00:05 GMT
ENV RUBY_VERSION=2.7.5
# Thu, 17 Mar 2022 21:00:05 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Thu, 17 Mar 2022 21:04:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 21:04:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 21:04:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 21:04:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 21:04:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 21:04:59 GMT
CMD ["irb"]
# Sat, 19 Mar 2022 05:29:54 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sat, 19 Mar 2022 05:30:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sat, 19 Mar 2022 05:30:16 GMT
ENV RAILS_ENV=production
# Sat, 19 Mar 2022 05:30:16 GMT
WORKDIR /usr/src/redmine
# Sat, 19 Mar 2022 05:30:16 GMT
ENV HOME=/home/redmine
# Sat, 19 Mar 2022 05:30:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sat, 19 Mar 2022 05:30:17 GMT
ENV REDMINE_VERSION=4.2.4
# Sat, 19 Mar 2022 05:30:18 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.4.tar.gz
# Sat, 19 Mar 2022 05:30:18 GMT
ENV REDMINE_DOWNLOAD_SHA256=cf649f5d4ff783582f82bebd4a5099ef63acb3d5573bbe6b4bf64f293c61c9ce
# Sat, 19 Mar 2022 05:30:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sat, 19 Mar 2022 05:30:24 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 19 Mar 2022 05:33:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 19 Mar 2022 05:33:54 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 19 Mar 2022 05:33:54 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sat, 19 Mar 2022 05:33:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 19 Mar 2022 05:33:54 GMT
EXPOSE 3000
# Sat, 19 Mar 2022 05:33:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:93317a1f65ec94b67aefe728a598022610246404e3a68d391c76cd0e5244a2a0`  
		Last Modified: Thu, 17 Mar 2022 08:13:56 GMT  
		Size: 2.8 MB (2821789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cb8b0323150199500fcf92274564e6ac0433664bf2287409332e0cf4582283`  
		Last Modified: Thu, 17 Mar 2022 21:32:43 GMT  
		Size: 3.7 MB (3709247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f284056baff163a9aee108f97c5d97638c6c38440b96a2b5cfdb53ecb6d09ca`  
		Last Modified: Thu, 17 Mar 2022 21:32:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce00ed99a92b467aa4688efea203fcfa82cd8775a1b1a5b37ea2d6f29432b9c9`  
		Last Modified: Thu, 17 Mar 2022 21:36:39 GMT  
		Size: 13.3 MB (13287496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25b696d461020b6149a8ba432b326be2308e8bca1f04ab2292098934b3050b0`  
		Last Modified: Thu, 17 Mar 2022 21:36:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdb69ac6c2ceac853b5b47e05c256d4b247080e03deca73b8a2f43234fcae3e`  
		Last Modified: Sat, 19 Mar 2022 05:43:28 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0131c4a68eea1f53b8900120152092fb959b10f2adb488b6ccb5fb1f28195`  
		Last Modified: Sat, 19 Mar 2022 05:44:02 GMT  
		Size: 83.8 MB (83835503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9060a52a6a6a2eaf141539d3fc0bd106be6716295f0de7a3a5ef0e83fdc98dd`  
		Last Modified: Sat, 19 Mar 2022 05:43:26 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5efa3a9dddd7f6dabeda905e137ab29b1757b5d03e61364ecebc1102d51c3f`  
		Last Modified: Sat, 19 Mar 2022 05:43:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dd0a0c3fa3de34c5039b60b831f2d5ee0ede7d98efd7673a61fc975bada3bd`  
		Last Modified: Sat, 19 Mar 2022 05:43:28 GMT  
		Size: 3.1 MB (3065453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381dda4d3b7e1c130fccf79b199d666a62a4622dafaecfd92fa3c8f73d3ff703`  
		Last Modified: Sat, 19 Mar 2022 05:43:43 GMT  
		Size: 55.0 MB (55002482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6e20475f5865a67faa58e7db9bb880d41441ac8a61cae64bcfbc168b4a4517`  
		Last Modified: Sat, 19 Mar 2022 05:43:26 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.15` - linux; ppc64le

```console
$ docker pull redmine@sha256:2a6f541fee806fc75ce2d6f88bb1eb88657cd63bfe313819207eff509be6c745
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163148866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38aa6af04adea9edf5aeb2b0d7407632bd7263a3db3a0b0452c7d8ecf3640bef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 11:14:04 GMT
ADD file:ddc94e1e084c05807db26adcc95b47a137fa47fb391e75998b338ada65e00c1c in / 
# Thu, 17 Mar 2022 11:14:09 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 09:35:25 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 18 Mar 2022 09:35:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 18 Mar 2022 09:35:44 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 10:47:33 GMT
ENV RUBY_MAJOR=2.7
# Fri, 18 Mar 2022 10:47:36 GMT
ENV RUBY_VERSION=2.7.5
# Fri, 18 Mar 2022 10:47:39 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Fri, 18 Mar 2022 10:50:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 18 Mar 2022 10:50:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 18 Mar 2022 10:50:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 18 Mar 2022 10:50:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 10:51:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 18 Mar 2022 10:51:10 GMT
CMD ["irb"]
# Sun, 20 Mar 2022 03:26:43 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Sun, 20 Mar 2022 03:27:58 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Sun, 20 Mar 2022 03:28:04 GMT
ENV RAILS_ENV=production
# Sun, 20 Mar 2022 03:28:07 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Mar 2022 03:28:10 GMT
ENV HOME=/home/redmine
# Sun, 20 Mar 2022 03:28:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Sun, 20 Mar 2022 03:28:20 GMT
ENV REDMINE_VERSION=4.2.4
# Sun, 20 Mar 2022 03:28:23 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.4.tar.gz
# Sun, 20 Mar 2022 03:28:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=cf649f5d4ff783582f82bebd4a5099ef63acb3d5573bbe6b4bf64f293c61c9ce
# Sun, 20 Mar 2022 03:28:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Sun, 20 Mar 2022 03:28:38 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 20 Mar 2022 03:32:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Sun, 20 Mar 2022 03:32:55 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Mar 2022 03:32:57 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Sun, 20 Mar 2022 03:33:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Mar 2022 03:33:09 GMT
EXPOSE 3000
# Sun, 20 Mar 2022 03:33:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eef85fcc847498263d979ef7ec75680d05e90815eb83a9ec4db135b990c0d8b8`  
		Last Modified: Thu, 17 Mar 2022 11:15:15 GMT  
		Size: 2.8 MB (2814051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee6351d0f1b819580a0449d13ddde68a23b1f8d80d0ddb05123494b33393599`  
		Last Modified: Fri, 18 Mar 2022 11:26:42 GMT  
		Size: 3.8 MB (3799991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0975f3c49841ad06a9b9e1ddd6eccf2c10976603b9ceb01c0f334b595112a4c`  
		Last Modified: Fri, 18 Mar 2022 11:26:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a68562c821c732d05035c8760cc57a784dcd30d4a19d28f81b5e7152ae0378`  
		Last Modified: Fri, 18 Mar 2022 11:30:27 GMT  
		Size: 14.4 MB (14416968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4f8000ce9ab19c6af3fb262fd9a26b28e09d51ec1faa0b7ab1f6f5e0415e0f`  
		Last Modified: Fri, 18 Mar 2022 11:30:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aaa4e92363fe1184da6392014dd482567263cd68dbd06ceea21fdac1c4a30b`  
		Last Modified: Sun, 20 Mar 2022 03:55:38 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3373c53b5d43d658e42dcc01e652752df7d6c151a5812eab70658702508f51c9`  
		Last Modified: Sun, 20 Mar 2022 03:55:52 GMT  
		Size: 82.5 MB (82475757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7ce94757aa62ad6f1378eef52b2d1363c53dcd6dd4d4a998296cc597da12c7`  
		Last Modified: Sun, 20 Mar 2022 03:55:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548ba2b5a41606ae50d51990cb576b5cdeeb62de0c1d340df9a5b265c74394a0`  
		Last Modified: Sun, 20 Mar 2022 03:55:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15882f90f125ec5769998518e4960009b05c14498d09641d68e03842d2b55fd7`  
		Last Modified: Sun, 20 Mar 2022 03:55:35 GMT  
		Size: 3.1 MB (3065446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f4a9c52fe3f57cec215192946a1c1ff838a369827b55434c7b05e388d27cdf`  
		Last Modified: Sun, 20 Mar 2022 03:55:41 GMT  
		Size: 56.6 MB (56572900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da73bc53e2039528c503c0e2f1364f6d2824258372a0f7b0b84a71f3848807`  
		Last Modified: Sun, 20 Mar 2022 03:55:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:alpine3.15` - linux; s390x

```console
$ docker pull redmine@sha256:e0ece2988bea1ac01d1ddc6c0b7a862de6e36d2411f12ca2592d5fb4e8418e02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153892282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8431a9dd529029d93784975657193f82f48393f2a635e738575ddff9a48da4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 03:04:28 GMT
ADD file:f623c69acb1859b41ef29e8f20f4e6c7072d9c6d7210d745afc615251bfe418f in / 
# Thu, 17 Mar 2022 03:04:28 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:51:56 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 15:51:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 15:51:57 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 16:08:36 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Mar 2022 16:08:37 GMT
ENV RUBY_VERSION=2.7.5
# Thu, 17 Mar 2022 16:08:37 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Thu, 17 Mar 2022 16:10:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 16:10:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 16:10:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 16:10:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 16:10:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 16:10:05 GMT
CMD ["irb"]
# Fri, 18 Mar 2022 08:07:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Fri, 18 Mar 2022 08:07:21 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Fri, 18 Mar 2022 08:07:25 GMT
ENV RAILS_ENV=production
# Fri, 18 Mar 2022 08:07:25 GMT
WORKDIR /usr/src/redmine
# Fri, 18 Mar 2022 08:07:26 GMT
ENV HOME=/home/redmine
# Fri, 18 Mar 2022 08:07:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 18 Mar 2022 08:07:26 GMT
ENV REDMINE_VERSION=4.2.4
# Fri, 18 Mar 2022 08:07:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.4.tar.gz
# Fri, 18 Mar 2022 08:07:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=cf649f5d4ff783582f82bebd4a5099ef63acb3d5573bbe6b4bf64f293c61c9ce
# Fri, 18 Mar 2022 08:07:29 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 18 Mar 2022 08:07:29 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 18 Mar 2022 08:09:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 18 Mar 2022 08:09:17 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 18 Mar 2022 08:09:17 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Fri, 18 Mar 2022 08:09:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:09:17 GMT
EXPOSE 3000
# Fri, 18 Mar 2022 08:09:18 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d51040c5bfbf434887bfed2557335a411e6ef760d04cc178d455d1c3ec1b721c`  
		Last Modified: Thu, 17 Mar 2022 03:05:26 GMT  
		Size: 2.6 MB (2601715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5aba69d5f11eb8d44cbe17bfaebcf18e7e539956c8cdf1934202b8a63f1132`  
		Last Modified: Thu, 17 Mar 2022 16:23:34 GMT  
		Size: 3.7 MB (3745815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0298f05cda25b4132392139f4cbf431e1c653a4420bdbfbee9f43df5b5fa8d`  
		Last Modified: Thu, 17 Mar 2022 16:23:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0869d961599c4c2e3e274792477754ee425725d022c8a707259d02e372899b19`  
		Last Modified: Thu, 17 Mar 2022 16:26:37 GMT  
		Size: 14.1 MB (14128407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5d358ebaf0d6b7ff5a89a6d6a471e977409d258797863c6297c80e9efe0f2f`  
		Last Modified: Thu, 17 Mar 2022 16:26:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24a423dcd6dd61354d43f92826f28af09da166fe82d0e0f9481360511cdb85e`  
		Last Modified: Fri, 18 Mar 2022 08:13:30 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0cf9bf8405d5d10c06ed6594ce9799f58cd42e127e849ac8888897fba2a7b6`  
		Last Modified: Fri, 18 Mar 2022 08:13:39 GMT  
		Size: 74.3 MB (74318812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee79f19cd326c35507be9c21d4657deff187d3d5a72a709bb4b9c702cc8aa657`  
		Last Modified: Fri, 18 Mar 2022 08:13:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9428627c8ebbbb8d914eecce611820ecfd9310cfeaf0071007902bfb58edb719`  
		Last Modified: Fri, 18 Mar 2022 08:13:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9c9520bf635d9a1c1eb1ec6e2c0ebd9c669948ff255ceda229ab18275a5ca8`  
		Last Modified: Fri, 18 Mar 2022 08:13:29 GMT  
		Size: 3.1 MB (3065448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8fa1818941d5c4b4df5426f27c5a8421d7f2840577bf77b48a5c60103840ba`  
		Last Modified: Fri, 18 Mar 2022 08:13:33 GMT  
		Size: 56.0 MB (56028339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2085b633d5c45ad2002c8ee48dfd01bfde63748661ed43ac71f0a39c84429d73`  
		Last Modified: Fri, 18 Mar 2022 08:13:29 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
