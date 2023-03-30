## `redmine:4-alpine3.16`

```console
$ docker pull redmine@sha256:fa44cbc9826ca165f6cff4aacfce723bf32835c1fc7657b0e02e113ed1214f59
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

### `redmine:4-alpine3.16` - linux; amd64

```console
$ docker pull redmine@sha256:b76e79f12a512eb99e39e9aba94dc06a6a414a4623d2f4039a03e47a4c285619
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166932944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3b8240b56eb50e472640761f1367a731b221948a8e06e550a002c6c9a9458e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:21:43 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 30 Mar 2023 02:21:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 30 Mar 2023 02:21:44 GMT
ENV LANG=C.UTF-8
# Thu, 30 Mar 2023 02:32:33 GMT
ENV RUBY_MAJOR=2.7
# Thu, 30 Mar 2023 02:32:33 GMT
ENV RUBY_VERSION=2.7.7
# Thu, 30 Mar 2023 02:32:34 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Thu, 30 Mar 2023 02:34:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 02:34:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 02:34:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 02:34:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 02:34:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 02:34:21 GMT
CMD ["irb"]
# Thu, 30 Mar 2023 05:32:47 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Thu, 30 Mar 2023 05:32:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Thu, 30 Mar 2023 05:32:54 GMT
ENV RAILS_ENV=production
# Thu, 30 Mar 2023 05:32:54 GMT
WORKDIR /usr/src/redmine
# Thu, 30 Mar 2023 05:32:55 GMT
ENV HOME=/home/redmine
# Thu, 30 Mar 2023 05:32:55 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 30 Mar 2023 05:32:55 GMT
ENV REDMINE_VERSION=4.2.10
# Thu, 30 Mar 2023 05:32:55 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.10.tar.gz
# Thu, 30 Mar 2023 05:32:55 GMT
ENV REDMINE_DOWNLOAD_SHA256=6f26388c23892962552ca491d5efedabd42dac88861dd9d80bc33458f65be1e9
# Thu, 30 Mar 2023 05:32:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 30 Mar 2023 05:32:59 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 30 Mar 2023 05:35:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 30 Mar 2023 05:35:09 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 30 Mar 2023 05:35:09 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Thu, 30 Mar 2023 05:35:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2023 05:35:10 GMT
EXPOSE 3000
# Thu, 30 Mar 2023 05:35:10 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52a5fbef9a7ca13abdb787ccddf6fb7d2ecad991b7d37fb776cd6d717b4e3d7`  
		Last Modified: Thu, 30 Mar 2023 02:35:25 GMT  
		Size: 3.9 MB (3851499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669ebe35e8508ac4a673ebf6ad67a95e27550896cb835fdd7a80cd80d9c0dc98`  
		Last Modified: Thu, 30 Mar 2023 02:35:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694d9c41b1ccabce285f7817e77acd8409fafeaf10a8c9facb1872a3cdbe90d3`  
		Last Modified: Thu, 30 Mar 2023 02:36:28 GMT  
		Size: 13.9 MB (13898644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568087cb3d200b929576ea8b09ef46d046998117ace0bb508420100fa4b2fdc6`  
		Last Modified: Thu, 30 Mar 2023 02:36:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2426c37c6e899e7fbc8d73c77d1c645077305123844285adb36ea46155e5edf`  
		Last Modified: Thu, 30 Mar 2023 05:36:18 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d832f30d747456fa0228500d417e5b701151f477d342474d0757d5b479832d`  
		Last Modified: Thu, 30 Mar 2023 05:36:30 GMT  
		Size: 90.4 MB (90397375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8b1241b3e28023373cc1b58a3068c392cde7dbc9c975c8b0bb1f5e046f532e`  
		Last Modified: Thu, 30 Mar 2023 05:36:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85b687816c959896c876c53361e7fe3703d051ba95882616c89ab05c9c6f58e`  
		Last Modified: Thu, 30 Mar 2023 05:36:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5411826b04cf9bf7864cdfc29d9bf851138e5b418ea309ef7a7665b44e1f8a1a`  
		Last Modified: Thu, 30 Mar 2023 05:36:17 GMT  
		Size: 3.1 MB (3070550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99524f2c9f84e9e9d36963fa6bdeb0ba3b7ecf383d5c39fb2b407c5275fc9028`  
		Last Modified: Thu, 30 Mar 2023 05:36:21 GMT  
		Size: 52.9 MB (52903138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d609c959e76c5ae4029d6521707b1ec505b705e6c188d6c02ef594ac8bd449a`  
		Last Modified: Thu, 30 Mar 2023 05:36:16 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine3.16` - linux; arm variant v6

```console
$ docker pull redmine@sha256:22b99d45b531ab12293b6a24d44720738b7079a928e3de28af8caed19c0aef5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158778177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef087cf133e3db12923ae1f4526008877fae656480a19e9ba7859057524bc0a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:06:08 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 30 Mar 2023 00:06:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 30 Mar 2023 00:06:09 GMT
ENV LANG=C.UTF-8
# Thu, 30 Mar 2023 00:17:19 GMT
ENV RUBY_MAJOR=2.7
# Thu, 30 Mar 2023 00:17:19 GMT
ENV RUBY_VERSION=2.7.7
# Thu, 30 Mar 2023 00:17:19 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Thu, 30 Mar 2023 00:19:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 00:19:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 00:19:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 00:19:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 00:19:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 00:19:03 GMT
CMD ["irb"]
# Thu, 30 Mar 2023 01:20:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Thu, 30 Mar 2023 01:20:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Thu, 30 Mar 2023 01:20:15 GMT
ENV RAILS_ENV=production
# Thu, 30 Mar 2023 01:20:15 GMT
WORKDIR /usr/src/redmine
# Thu, 30 Mar 2023 01:20:16 GMT
ENV HOME=/home/redmine
# Thu, 30 Mar 2023 01:20:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 30 Mar 2023 01:20:16 GMT
ENV REDMINE_VERSION=4.2.10
# Thu, 30 Mar 2023 01:20:16 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.10.tar.gz
# Thu, 30 Mar 2023 01:20:16 GMT
ENV REDMINE_DOWNLOAD_SHA256=6f26388c23892962552ca491d5efedabd42dac88861dd9d80bc33458f65be1e9
# Thu, 30 Mar 2023 01:20:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 30 Mar 2023 01:20:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 30 Mar 2023 01:22:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 30 Mar 2023 01:22:38 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 30 Mar 2023 01:22:38 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Thu, 30 Mar 2023 01:22:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2023 01:22:38 GMT
EXPOSE 3000
# Thu, 30 Mar 2023 01:22:39 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed94e4dc9ea9eca127e40e4b6b16da2ee175dde29c138fd7a8d5aedf32cf9e29`  
		Last Modified: Thu, 30 Mar 2023 00:20:59 GMT  
		Size: 3.6 MB (3593942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ac9bc6481f90a813d3da1de98c8b35d31e37a7f6e65d3d6bacc4996817175c`  
		Last Modified: Thu, 30 Mar 2023 00:20:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc689eeedcc4436eaeaa718e4e8dbddf3a750c461b8c71d86f2612500d0a559c`  
		Last Modified: Thu, 30 Mar 2023 00:21:56 GMT  
		Size: 13.4 MB (13439863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4d39b84a5207d6a7d885eeb34fa89be48280ac1bb5f6a88e34122baa9064d4`  
		Last Modified: Thu, 30 Mar 2023 00:21:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a981e8e9a4a509ff2f530ac7cd000037199fd78ab9f738e2a81f9302d972e8f9`  
		Last Modified: Thu, 30 Mar 2023 01:25:16 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b24b048780535bb3426b456d3e32c15dbae30d620ea67a949ccdca7efd062`  
		Last Modified: Thu, 30 Mar 2023 01:25:28 GMT  
		Size: 83.9 MB (83909137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb4bcfc9092177a34b70ef09e9d9b31020035625bfdf5015beeb1466cd70721`  
		Last Modified: Thu, 30 Mar 2023 01:25:13 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1bf78218fb5212139052ff6adb9874f833517d8889613abf03f3e1b1628121`  
		Last Modified: Thu, 30 Mar 2023 01:25:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3f680a37a79c61cf2ae71ad44eb65ef559446349920e19816ccb305531c275`  
		Last Modified: Thu, 30 Mar 2023 01:25:14 GMT  
		Size: 3.1 MB (3070581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f3af6bea5389239f93a6d48e6fd4b0632e8a49be7bcf9c08393865d001ab99`  
		Last Modified: Thu, 30 Mar 2023 01:25:19 GMT  
		Size: 52.1 MB (52143873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbfae96d0d2f2b458f7f93256770585437203fe89292cc32ef654caae0a1b2a`  
		Last Modified: Thu, 30 Mar 2023 01:25:13 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine3.16` - linux; arm variant v7

```console
$ docker pull redmine@sha256:6c2e13f3125404a768731b0f15c4f65aa287056ae0e396aff1fe3d3f611325fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156096453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157f0e21347a06b63a7950b401cbbe38c493fbbf0aaa285795abf8a6ded39b19`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:04:21 GMT
ADD file:68992157dbe7c3a454c26656c7bcb497794c1008ead5e078b2928ce165cd65cd in / 
# Wed, 29 Mar 2023 18:04:21 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:37:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 30 Mar 2023 05:37:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 30 Mar 2023 05:37:23 GMT
ENV LANG=C.UTF-8
# Thu, 30 Mar 2023 05:50:23 GMT
ENV RUBY_MAJOR=2.7
# Thu, 30 Mar 2023 05:50:23 GMT
ENV RUBY_VERSION=2.7.7
# Thu, 30 Mar 2023 05:50:23 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Thu, 30 Mar 2023 05:52:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 05:52:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 05:52:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 05:52:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 05:52:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 05:52:02 GMT
CMD ["irb"]
# Thu, 30 Mar 2023 06:49:35 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Thu, 30 Mar 2023 06:49:44 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Thu, 30 Mar 2023 06:49:45 GMT
ENV RAILS_ENV=production
# Thu, 30 Mar 2023 06:49:45 GMT
WORKDIR /usr/src/redmine
# Thu, 30 Mar 2023 06:49:45 GMT
ENV HOME=/home/redmine
# Thu, 30 Mar 2023 06:49:45 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 30 Mar 2023 06:49:45 GMT
ENV REDMINE_VERSION=4.2.10
# Thu, 30 Mar 2023 06:49:45 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.10.tar.gz
# Thu, 30 Mar 2023 06:49:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=6f26388c23892962552ca491d5efedabd42dac88861dd9d80bc33458f65be1e9
# Thu, 30 Mar 2023 06:49:49 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 30 Mar 2023 06:49:49 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 30 Mar 2023 06:52:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 30 Mar 2023 06:52:07 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 30 Mar 2023 06:52:07 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Thu, 30 Mar 2023 06:52:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2023 06:52:07 GMT
EXPOSE 3000
# Thu, 30 Mar 2023 06:52:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d378ffb313542b797defad9ec843de710c353f40e17e124e74f7e874971429ee`  
		Last Modified: Wed, 29 Mar 2023 18:07:08 GMT  
		Size: 2.4 MB (2420546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e2bb5f86e6c76ffc574535478b37638416b94d7f6a24f27d26c3602b3c1b2d`  
		Last Modified: Thu, 30 Mar 2023 05:53:04 GMT  
		Size: 3.5 MB (3461614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72eed43cd068815244c3f42447a9d10d3d14af8cfc72145b264b40c4eabf39`  
		Last Modified: Thu, 30 Mar 2023 05:53:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fc3e0ae85ace4d94f740490249867641a54cc384027fa637da69e8fe2ea338`  
		Last Modified: Thu, 30 Mar 2023 05:54:09 GMT  
		Size: 13.3 MB (13305600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb50c6477c02c384e0dcdb30749a2b71d65c64226e023a9af88b9cc6ecf3efb1`  
		Last Modified: Thu, 30 Mar 2023 05:54:08 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc606bd91c974a88911dbce9afa129939066307ff09d2d96c6b467ec093f422`  
		Last Modified: Thu, 30 Mar 2023 06:54:19 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b0d3e5f566de53dded12e58cdaadcdc461b233f83f0f57aa911990d7f8c061`  
		Last Modified: Thu, 30 Mar 2023 06:54:31 GMT  
		Size: 82.0 MB (82022419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d0c061df7155083df2b69cc2c34a31213284feb8ff97ed64e3efdf27f374f8`  
		Last Modified: Thu, 30 Mar 2023 06:54:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55fa990af0c74a62656843365f9608fe2de1f37ca6b65957df8e1ab5dbc4f59`  
		Last Modified: Thu, 30 Mar 2023 06:54:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13efefebe7fd0e719a4dccbbc11e72aa2e8a5fe20803e9d64a7328a22c53e00`  
		Last Modified: Thu, 30 Mar 2023 06:54:18 GMT  
		Size: 3.1 MB (3070557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bab7796f2f216da9a35d7cb2ce7a709bcde612e13a2bb6916a6d7075076cc0`  
		Last Modified: Thu, 30 Mar 2023 06:54:22 GMT  
		Size: 51.8 MB (51811779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094861834598f894790dec56638503ae286cdcec726108045f07423fad7b3be0`  
		Last Modified: Thu, 30 Mar 2023 06:54:17 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:3a010f52d60ed8135921fdc4eba5715837c1e00c7d51a014f5761adaf0e27da3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163307431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890caea5865cb751dcf6afd62cfabfd90e6f09795db4611649925388a7fe0d8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 05:31:58 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 30 Mar 2023 05:31:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 30 Mar 2023 05:31:58 GMT
ENV LANG=C.UTF-8
# Thu, 30 Mar 2023 05:39:53 GMT
ENV RUBY_MAJOR=2.7
# Thu, 30 Mar 2023 19:23:18 GMT
ENV RUBY_VERSION=2.7.8
# Thu, 30 Mar 2023 19:23:18 GMT
ENV RUBY_DOWNLOAD_SHA256=f22f662da504d49ce2080e446e4bea7008cee11d5ec4858fc69000d0e5b1d7fb
# Thu, 30 Mar 2023 19:24:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 19:24:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 19:24:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 19:24:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 19:24:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 19:24:41 GMT
CMD ["irb"]
# Thu, 30 Mar 2023 19:52:23 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Thu, 30 Mar 2023 19:52:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Thu, 30 Mar 2023 19:52:30 GMT
ENV RAILS_ENV=production
# Thu, 30 Mar 2023 19:52:30 GMT
WORKDIR /usr/src/redmine
# Thu, 30 Mar 2023 19:52:30 GMT
ENV HOME=/home/redmine
# Thu, 30 Mar 2023 19:52:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 30 Mar 2023 19:52:31 GMT
ENV REDMINE_VERSION=4.2.10
# Thu, 30 Mar 2023 19:52:31 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.10.tar.gz
# Thu, 30 Mar 2023 19:52:31 GMT
ENV REDMINE_DOWNLOAD_SHA256=6f26388c23892962552ca491d5efedabd42dac88861dd9d80bc33458f65be1e9
# Thu, 30 Mar 2023 19:52:34 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 30 Mar 2023 19:52:34 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 30 Mar 2023 19:54:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 30 Mar 2023 19:54:32 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 30 Mar 2023 19:54:32 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Thu, 30 Mar 2023 19:54:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2023 19:54:32 GMT
EXPOSE 3000
# Thu, 30 Mar 2023 19:54:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1a9490257ae7ef0e0bc1c83706c2438d863108df9a74d33ad1f5104d50de88`  
		Last Modified: Thu, 30 Mar 2023 05:42:27 GMT  
		Size: 3.8 MB (3821415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12c93e378d0ceba3619afba2196ca86017a31284505e76b9d15780ac1c1d790`  
		Last Modified: Thu, 30 Mar 2023 05:42:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92a0f6419ab163f76a5ffbb8cd835634b6a40f8aa07aad8c56f9edeeb6a79c`  
		Last Modified: Thu, 30 Mar 2023 19:31:07 GMT  
		Size: 13.7 MB (13739013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed88aab55709eefa953cbc514247510e0313b93ceb8482a36d79db68061468d5`  
		Last Modified: Thu, 30 Mar 2023 19:31:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d39497d2b96720e7537b8a0aac09d50c8648f138a28cd74fa79a3dc82daea85`  
		Last Modified: Thu, 30 Mar 2023 19:56:40 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7c20696c4d10098e69ecf74568472d3d05b369cde6953abc900b10ff70d007`  
		Last Modified: Thu, 30 Mar 2023 19:56:50 GMT  
		Size: 87.3 MB (87261600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc41b8e4101809e1d3da0a88f7589182189e50619dcee827d343332c17bffa21`  
		Last Modified: Thu, 30 Mar 2023 19:56:38 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f826d80b4f74ba6ce8516c08aa1f4cd803ee9cf1f55310ada62096a4e85006`  
		Last Modified: Thu, 30 Mar 2023 19:56:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69f96bc5202c516188b543e4a943397cc77c4888beb175e586c688fe9aef0c5`  
		Last Modified: Thu, 30 Mar 2023 19:56:39 GMT  
		Size: 3.1 MB (3070594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53dad1668685980868b97cd01971a2ef8b20210d0867c62fb5e60f5901ea580`  
		Last Modified: Thu, 30 Mar 2023 19:56:42 GMT  
		Size: 52.7 MB (52701530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4610778ae8043d6a5331d9975982f2bbf077fca81fa9349ddb80f66da6c778f6`  
		Last Modified: Thu, 30 Mar 2023 19:56:38 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine3.16` - linux; 386

```console
$ docker pull redmine@sha256:8c62a0c49fe81c6286762b32b0020f58659777c1534a77cf60656ba357e64a4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165593127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853b12790a2192c8c118eeb931f1008f3313da35d1433c37de1e8f292153a900`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:33 GMT
ADD file:c9d37b1a7eee54b1a8c1ebde284829510ec289f7b7db2c16059b26f01b416fe0 in / 
# Wed, 29 Mar 2023 17:38:33 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:09:33 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 30 Mar 2023 01:09:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 30 Mar 2023 01:09:34 GMT
ENV LANG=C.UTF-8
# Thu, 30 Mar 2023 01:27:14 GMT
ENV RUBY_MAJOR=2.7
# Thu, 30 Mar 2023 01:27:14 GMT
ENV RUBY_VERSION=2.7.7
# Thu, 30 Mar 2023 01:27:14 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Thu, 30 Mar 2023 01:30:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 01:30:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 01:30:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 01:30:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 01:30:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 01:30:33 GMT
CMD ["irb"]
# Thu, 30 Mar 2023 03:42:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Thu, 30 Mar 2023 03:42:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Thu, 30 Mar 2023 03:42:22 GMT
ENV RAILS_ENV=production
# Thu, 30 Mar 2023 03:42:22 GMT
WORKDIR /usr/src/redmine
# Thu, 30 Mar 2023 03:42:22 GMT
ENV HOME=/home/redmine
# Thu, 30 Mar 2023 03:42:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 30 Mar 2023 03:42:23 GMT
ENV REDMINE_VERSION=4.2.10
# Thu, 30 Mar 2023 03:42:23 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.10.tar.gz
# Thu, 30 Mar 2023 03:42:23 GMT
ENV REDMINE_DOWNLOAD_SHA256=6f26388c23892962552ca491d5efedabd42dac88861dd9d80bc33458f65be1e9
# Thu, 30 Mar 2023 03:42:27 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 30 Mar 2023 03:42:27 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 30 Mar 2023 03:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 30 Mar 2023 03:45:07 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 30 Mar 2023 03:45:07 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Thu, 30 Mar 2023 03:45:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2023 03:45:07 GMT
EXPOSE 3000
# Thu, 30 Mar 2023 03:45:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dea45757091f21722aec41fb20845e57a04f4bb8c199531491f1dc070480a574`  
		Last Modified: Wed, 29 Mar 2023 17:39:11 GMT  
		Size: 2.8 MB (2810814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec757ac8272e11b5833accc88f85293f1b7b49ba1bdb61dde9025bc0f725cc25`  
		Last Modified: Thu, 30 Mar 2023 01:31:40 GMT  
		Size: 3.9 MB (3886676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3736da23bde1b795da95fc3c284ab996b92cf770d252551bedf5b63943f8483b`  
		Last Modified: Thu, 30 Mar 2023 01:31:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84091fabb0cce93ce2d9475e8466da246dcde912ed6ad27f1d24eae8f294c7c`  
		Last Modified: Thu, 30 Mar 2023 01:32:50 GMT  
		Size: 13.3 MB (13318943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694eb9f0a8198b4a8ab8d7ad092b4a9107ef25d73afe4d1463f21c62a1a1863d`  
		Last Modified: Thu, 30 Mar 2023 01:32:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bfabd210ef494f12b74c1adad0ca84230bb00af4cb3c2688378b15d4f99e4b`  
		Last Modified: Thu, 30 Mar 2023 03:46:19 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3386ce024999182e2604a978915bbc1917f6816ab4cba1bcecd5f2a72a4272c1`  
		Last Modified: Thu, 30 Mar 2023 03:46:37 GMT  
		Size: 90.3 MB (90264359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de71f76ff122a8f662b0e27c4b9f8ec49f363a5b26b09acbe338de426fce14e4`  
		Last Modified: Thu, 30 Mar 2023 03:46:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142e913a355eb276f9bb068765028254938bb49a834a70ebbd06abbf988417a4`  
		Last Modified: Thu, 30 Mar 2023 03:46:17 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f193ab319c7c8792ef908a1f12fdfdcdacb6d78454b243fe9133de93adf621f6`  
		Last Modified: Thu, 30 Mar 2023 03:46:18 GMT  
		Size: 3.1 MB (3070639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789b243d94ead0acb085762f134eef587778aa570c26f590c6d85c138ca1d7d5`  
		Last Modified: Thu, 30 Mar 2023 03:46:25 GMT  
		Size: 52.2 MB (52237761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fb09dfdd1c05ded9b3fdbd38c25fe6a53f0bb91130850b4e1a9ca8413fbb1a`  
		Last Modified: Thu, 30 Mar 2023 03:46:17 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine3.16` - linux; ppc64le

```console
$ docker pull redmine@sha256:05cb9980199b2914bbd3e1c3b6ac221e944ae59a0f8b0a4ac9a1bc689204cd55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174272327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4422c136fa5ed52cc258e9eefb799754f925e254bd668e0bb7e55c7b3ebf65c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:34 GMT
ADD file:00a20a25a46ff8ebd9bc78b5b8c6fc5b1dc8ae73d5a42048fa5769a2b2e717c7 in / 
# Wed, 29 Mar 2023 18:16:34 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 04:10:41 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 30 Mar 2023 04:10:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 30 Mar 2023 04:10:46 GMT
ENV LANG=C.UTF-8
# Thu, 30 Mar 2023 04:26:15 GMT
ENV RUBY_MAJOR=2.7
# Thu, 30 Mar 2023 04:26:17 GMT
ENV RUBY_VERSION=2.7.7
# Thu, 30 Mar 2023 04:26:19 GMT
ENV RUBY_DOWNLOAD_SHA256=b38dff2e1f8ce6e5b7d433f8758752987a6b2adfd9bc7571dbc42ea5d04e3e4c
# Thu, 30 Mar 2023 04:29:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 04:29:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 04:29:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 04:29:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 04:29:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 04:29:31 GMT
CMD ["irb"]
# Thu, 30 Mar 2023 08:20:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Thu, 30 Mar 2023 08:21:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Thu, 30 Mar 2023 08:21:15 GMT
ENV RAILS_ENV=production
# Thu, 30 Mar 2023 08:21:15 GMT
WORKDIR /usr/src/redmine
# Thu, 30 Mar 2023 08:21:15 GMT
ENV HOME=/home/redmine
# Thu, 30 Mar 2023 08:21:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 30 Mar 2023 08:21:16 GMT
ENV REDMINE_VERSION=4.2.10
# Thu, 30 Mar 2023 08:21:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.10.tar.gz
# Thu, 30 Mar 2023 08:21:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=6f26388c23892962552ca491d5efedabd42dac88861dd9d80bc33458f65be1e9
# Thu, 30 Mar 2023 08:21:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 30 Mar 2023 08:21:23 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 30 Mar 2023 08:26:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 30 Mar 2023 08:26:03 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 30 Mar 2023 08:26:03 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Thu, 30 Mar 2023 08:26:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2023 08:26:03 GMT
EXPOSE 3000
# Thu, 30 Mar 2023 08:26:04 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d80736dee7a63492583c90bab1ab07f987ed5e10dfb16fd3f025df3a2d65f1c6`  
		Last Modified: Wed, 29 Mar 2023 18:17:28 GMT  
		Size: 2.8 MB (2804670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98c697220ffba9acde6d37fcb16b5ccfd5f094e8f730ed282a01e7c2d7c2211`  
		Last Modified: Thu, 30 Mar 2023 04:30:46 GMT  
		Size: 4.0 MB (3973663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ec3a3209b2375deda630e78152d62b67aac8d3792af5404c85570ff55ffd2`  
		Last Modified: Thu, 30 Mar 2023 04:30:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc6183c574c8d9baa5b5aa41fff0b6a507ba5a26a0ecd6e94cbf1220d75ef2d`  
		Last Modified: Thu, 30 Mar 2023 04:31:57 GMT  
		Size: 14.4 MB (14399255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe4ac0c5edd4429ad4b613d227f68ebd0c00924456b3f210c6aabdf0d4b305a`  
		Last Modified: Thu, 30 Mar 2023 04:31:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc8c881d678a928477675e12af3af0e72f68e29d1a0836060a988ffcfe8c5e`  
		Last Modified: Thu, 30 Mar 2023 08:27:31 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1befe5ec5aa5c17af2ae537513aed90a0ae3c5a6b772a117c6bc9fd6dcdd0a`  
		Last Modified: Thu, 30 Mar 2023 08:27:56 GMT  
		Size: 96.3 MB (96275989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb124b3280579cac95e49193c2468e7e71c5cfc5b155f22e7b853f5748883fa`  
		Last Modified: Thu, 30 Mar 2023 08:27:29 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0ae81f905b0bbb7f97a5c5064fd32126d1c4edbb03d18095aff04c04e8f284`  
		Last Modified: Thu, 30 Mar 2023 08:27:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5e393a5b062ed9883a77679a8675b4926a92b7219367194f6a41f99b2a2e13`  
		Last Modified: Thu, 30 Mar 2023 08:27:31 GMT  
		Size: 3.1 MB (3070531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644d448725493fa250570129b8eb47dd46bd66f73417e97600ff984a36dacb18`  
		Last Modified: Thu, 30 Mar 2023 08:27:39 GMT  
		Size: 53.7 MB (53744285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510c76b1b00c8cd52fe5c7c3a838f8006b2a36608d3895d6c7893245bc6eb1c3`  
		Last Modified: Thu, 30 Mar 2023 08:27:29 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine3.16` - linux; s390x

```console
$ docker pull redmine@sha256:b3322f7d92f44a8db950ee08764aa48a35751e7b8dbce4edceb0a504641c8d66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157139998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0cf8e50150d9a088f1dcb733737d326b8bacd29e2a1030c49172bc0f6e435d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:18:04 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Wed, 29 Mar 2023 22:18:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 29 Mar 2023 22:18:07 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 22:32:53 GMT
ENV RUBY_MAJOR=2.7
# Thu, 30 Mar 2023 19:08:43 GMT
ENV RUBY_VERSION=2.7.8
# Thu, 30 Mar 2023 19:08:43 GMT
ENV RUBY_DOWNLOAD_SHA256=f22f662da504d49ce2080e446e4bea7008cee11d5ec4858fc69000d0e5b1d7fb
# Thu, 30 Mar 2023 19:10:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 19:10:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 19:10:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 19:10:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 19:10:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 19:10:16 GMT
CMD ["irb"]
# Thu, 30 Mar 2023 19:34:57 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Thu, 30 Mar 2023 19:35:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Thu, 30 Mar 2023 19:35:09 GMT
ENV RAILS_ENV=production
# Thu, 30 Mar 2023 19:35:09 GMT
WORKDIR /usr/src/redmine
# Thu, 30 Mar 2023 19:35:09 GMT
ENV HOME=/home/redmine
# Thu, 30 Mar 2023 19:35:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 30 Mar 2023 19:35:09 GMT
ENV REDMINE_VERSION=4.2.10
# Thu, 30 Mar 2023 19:35:09 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.10.tar.gz
# Thu, 30 Mar 2023 19:35:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=6f26388c23892962552ca491d5efedabd42dac88861dd9d80bc33458f65be1e9
# Thu, 30 Mar 2023 19:35:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 30 Mar 2023 19:35:12 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 30 Mar 2023 19:37:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 30 Mar 2023 19:37:05 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 30 Mar 2023 19:37:05 GMT
COPY file:f2dac8fc10b4b9c85d18ffc54f3822ba7f98c858ad133cc1c0a63d9d52731204 in / 
# Thu, 30 Mar 2023 19:37:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2023 19:37:05 GMT
EXPOSE 3000
# Thu, 30 Mar 2023 19:37:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65ad13b2023bc984343067f4fd6c0e60cb56fa44b7ea6d7d0aeedb5ef6085ae`  
		Last Modified: Wed, 29 Mar 2023 22:36:08 GMT  
		Size: 3.9 MB (3941156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20af8b6ad1ca8f1b69f8e3f0c32270dedb57e35279646158bffcec1b34cc7e59`  
		Last Modified: Wed, 29 Mar 2023 22:36:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5195284bb4f1de2522123c4b314c6942c80c4cab9fcd469569af93d34aef43`  
		Last Modified: Thu, 30 Mar 2023 19:13:24 GMT  
		Size: 13.8 MB (13825544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08ebd3437d4bacbb8de5f28d14c724ffc21b3f62d5dc07740db1b07c2f7fefc`  
		Last Modified: Thu, 30 Mar 2023 19:13:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958e005f6869ccd28c3e26982f5afc061a35216fcc2b5f52cd874bf5486565f4`  
		Last Modified: Thu, 30 Mar 2023 19:38:50 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db1fd666fa8f5cf7fb137a1dd2fd3acbad5209d131cd960e14fa1f7bd144b3a`  
		Last Modified: Thu, 30 Mar 2023 19:39:00 GMT  
		Size: 80.8 MB (80836782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcb767ad4a3a7978724d0bdc443ef4fefe6866f496ed9405c3f48e565dafc2d`  
		Last Modified: Thu, 30 Mar 2023 19:38:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7482c895e97c8644989f98407d4aadb9dfd93d1d19ab66c668fdb64c7ba87a84`  
		Last Modified: Thu, 30 Mar 2023 19:38:48 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d2f8ce52b538ade1490b98cf383220264ad2a91064818013643c5d3f7e71ac`  
		Last Modified: Thu, 30 Mar 2023 19:38:49 GMT  
		Size: 3.1 MB (3070628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091cdef2478f2c2b96b6fcc96d8fe4568c82b3e6aba69b84be36ca7c65b68e0f`  
		Last Modified: Thu, 30 Mar 2023 19:38:53 GMT  
		Size: 52.9 MB (52868556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcd3734a90d534052ad1baa28957267cbb7568feb2935b1a3d96def44e30cd4`  
		Last Modified: Thu, 30 Mar 2023 19:38:49 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
