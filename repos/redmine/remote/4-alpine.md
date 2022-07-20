## `redmine:4-alpine`

```console
$ docker pull redmine@sha256:0ae7ddef28872ae953466b763e3a857b061393f1064ee26886380757dc1a4e4b
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

### `redmine:4-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:254452cbafa3ea2a4adbc6eff54872f98f4bf3531ebe1fc1e3f4bb91fe528c37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159675940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8254b8d88f4b9928eb2a467b8530201aa95dc37a8f005fa5fb9eae4f0ce9618d`
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
# Wed, 20 Jul 2022 02:15:55 GMT
ENV RUBY_MAJOR=2.7
# Wed, 20 Jul 2022 02:15:56 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 20 Jul 2022 02:15:56 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 20 Jul 2022 02:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 02:17:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 02:17:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 02:17:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 02:17:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 02:17:44 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 05:29:23 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 05:29:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 05:29:32 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 05:29:33 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 05:29:33 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 05:29:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 05:29:33 GMT
ENV REDMINE_VERSION=4.2.7
# Wed, 20 Jul 2022 05:29:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.7.tar.gz
# Wed, 20 Jul 2022 05:29:34 GMT
ENV REDMINE_DOWNLOAD_SHA256=ed4be03b5ab63c2641a87db8978739dd997c0f646bfa1010ac9e5210c343724e
# Wed, 20 Jul 2022 05:29:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 05:29:37 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 05:31:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 05:31:48 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 05:31:48 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 05:31:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 05:31:49 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 05:31:49 GMT
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
	-	`sha256:dcdc002e1e1823469d20622a0c0aa7288e55eb5216078a426ea263999526e53d`  
		Last Modified: Wed, 20 Jul 2022 02:20:22 GMT  
		Size: 14.0 MB (13981217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e930796d14cfb78c6395cc2432007fcf8514da481cbccf698055892ebdc71b11`  
		Last Modified: Wed, 20 Jul 2022 02:20:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8880a5a49de413e54b32bc436717769c0824ffed545fa346da71a7b27a1f88c8`  
		Last Modified: Wed, 20 Jul 2022 05:33:18 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdc09a753def6246d89eda632ea7e689c448657007a36a29ed0722ea37f74a3`  
		Last Modified: Wed, 20 Jul 2022 05:33:30 GMT  
		Size: 82.4 MB (82408564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f56a713a2226b7a06b1f76574feb66686e3416cc97ae929a27475d1667673b`  
		Last Modified: Wed, 20 Jul 2022 05:33:15 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd64d63e8197d2e7f443a0258ddc73b5006ef76026e04d03c2ab06099f5a31a4`  
		Last Modified: Wed, 20 Jul 2022 05:33:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6542cea3eee64ad0c84a558a474f94a41bf67c719b72cd5d95618b9a9ac842`  
		Last Modified: Wed, 20 Jul 2022 05:33:16 GMT  
		Size: 3.1 MB (3067126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54b15b12587360cc58a1899677dcc8eb5f0fc7cda6ed31fc5bf1f15cd4e2e4a`  
		Last Modified: Wed, 20 Jul 2022 05:33:21 GMT  
		Size: 53.7 MB (53717060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f4f46dd43660b1f924fa6ab03c1ec8f3d0bda3a01aa089762345174b249a28`  
		Last Modified: Wed, 20 Jul 2022 05:33:15 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:a1cad08efec2aa8eee355b7768e391cb0d645cbae337180ea211e9f7aba6c2a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153243416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f65b9c67f187d7d65b319a3ce99ae7e7e06f6f54ae44fe85ea331a1c1e0f41`
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
# Wed, 20 Jul 2022 06:25:08 GMT
ENV RUBY_MAJOR=2.7
# Wed, 20 Jul 2022 06:25:08 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 20 Jul 2022 06:25:09 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 20 Jul 2022 06:28:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 06:28:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 06:28:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 06:28:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 06:28:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 06:28:54 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 08:33:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 08:33:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 08:33:38 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 08:33:38 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 08:33:39 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 08:33:40 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 08:33:41 GMT
ENV REDMINE_VERSION=4.2.7
# Wed, 20 Jul 2022 08:33:41 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.7.tar.gz
# Wed, 20 Jul 2022 08:33:41 GMT
ENV REDMINE_DOWNLOAD_SHA256=ed4be03b5ab63c2641a87db8978739dd997c0f646bfa1010ac9e5210c343724e
# Wed, 20 Jul 2022 08:33:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 08:33:48 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 08:39:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 08:40:00 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 08:40:00 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 08:40:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 08:40:01 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 08:40:02 GMT
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
	-	`sha256:3b778b44587489c732390adf2d36b646867f080b8b59df036daa65592f4b6ffd`  
		Last Modified: Wed, 20 Jul 2022 06:33:25 GMT  
		Size: 13.4 MB (13412317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d26d4eef627c9a4490119a96eb5e6b1fe29921dcef53045c5839d4f5d7bd92`  
		Last Modified: Wed, 20 Jul 2022 06:33:17 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bd7bd42c8c16a9b9031c8588651f1b2c94912f3d44d2de78c2485d50d3a0dd`  
		Last Modified: Wed, 20 Jul 2022 08:42:48 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e9f9f26336788ed99e9d46f075e8374e2358044a4d4032f1a05fb590214039`  
		Last Modified: Wed, 20 Jul 2022 08:43:41 GMT  
		Size: 77.9 MB (77877703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d83d3ef36588dc48d57bae0f55d9df461c47b80515cc8b92e900e3a431707a7`  
		Last Modified: Wed, 20 Jul 2022 08:42:46 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001fd72ecb236ed049187bd8054db53fca59fc4ebdbdb3f55595c6ea42047eb5`  
		Last Modified: Wed, 20 Jul 2022 08:42:46 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0078c67e1fa19ebd524aa3a4eefe72dd49887daf240a39da9e4be3b3e42aca0`  
		Last Modified: Wed, 20 Jul 2022 08:42:50 GMT  
		Size: 3.1 MB (3067038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f49cb7f345d0fcbd7310c30bc810f37de32122f2727bef744f3275562b29df`  
		Last Modified: Wed, 20 Jul 2022 08:43:11 GMT  
		Size: 52.8 MB (52828533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db0fd6532ff3972e3deae2d1fa236877856d153158eb1c9c8f33ef6f2619211`  
		Last Modified: Wed, 20 Jul 2022 08:42:46 GMT  
		Size: 1.9 KB (1855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:6699dc2b28d9f9ae528404de45906d3e5425c3719f9f00fe5db317dc9eeae3fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150199881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af92972ca149a4b5c63f7044f9caf52f8e386212d1adf58fe165366a22e890f`
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
# Tue, 05 Apr 2022 03:43:27 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 20:12:11 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 20:12:11 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 20:15:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 20:15:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 20:15:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 20:15:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 20:15:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 20:15:33 GMT
CMD ["irb"]
# Wed, 13 Apr 2022 02:53:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Tue, 12 Jul 2022 03:11:04 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Tue, 12 Jul 2022 03:11:05 GMT
ENV RAILS_ENV=production
# Tue, 12 Jul 2022 03:11:06 GMT
WORKDIR /usr/src/redmine
# Tue, 12 Jul 2022 03:11:06 GMT
ENV HOME=/home/redmine
# Tue, 12 Jul 2022 03:11:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 12 Jul 2022 03:11:08 GMT
ENV REDMINE_VERSION=4.2.7
# Tue, 12 Jul 2022 03:11:09 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.7.tar.gz
# Tue, 12 Jul 2022 03:11:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=ed4be03b5ab63c2641a87db8978739dd997c0f646bfa1010ac9e5210c343724e
# Tue, 12 Jul 2022 03:11:15 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 12 Jul 2022 03:11:16 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 12 Jul 2022 03:17:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Tue, 12 Jul 2022 03:17:11 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 12 Jul 2022 03:17:12 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Tue, 12 Jul 2022 03:17:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Jul 2022 03:17:13 GMT
EXPOSE 3000
# Tue, 12 Jul 2022 03:17:13 GMT
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
	-	`sha256:db348fdd8eec59ffbf61656974ad18acb6ce5b85f041d971169c15aa99dd304a`  
		Last Modified: Tue, 12 Apr 2022 21:03:58 GMT  
		Size: 13.3 MB (13301907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229623706c6989ddd690cfaf7c87a113158ac019297bd5284d2a8ace7f43ebe6`  
		Last Modified: Tue, 12 Apr 2022 21:03:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e92f223765a01ea367ffe2ff4d1c69a90a65ac2f75189fd1022e02952b3394f`  
		Last Modified: Wed, 13 Apr 2022 03:18:56 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deafdec0190e18521c1ace0998bf0b7990b877ec534d020ade02b89495a906ee`  
		Last Modified: Tue, 12 Jul 2022 03:22:44 GMT  
		Size: 74.4 MB (74416859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433516c307c033d530ca1d75f9a26c5835e33debd9d67135abd5ec92cddb227b`  
		Last Modified: Tue, 12 Jul 2022 03:21:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7e6a0edfa708bf298cb9a36ae99b3a14c7a2fb9521254bb6c7033ce9ab4e58`  
		Last Modified: Tue, 12 Jul 2022 03:21:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb0902bfbc240337b244138ce8ec16abaad254950abfd65e6685d86c95a9b18`  
		Last Modified: Tue, 12 Jul 2022 03:22:00 GMT  
		Size: 3.1 MB (3067185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ed5ed2fc6e773a0bfe90365bdefaf4325fa5e47e24200d2952062f9945c590`  
		Last Modified: Tue, 12 Jul 2022 03:22:20 GMT  
		Size: 53.7 MB (53683856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd64abb235ae215f676d325b89db0bc36082d880577e39b6640f703f95bd28b0`  
		Last Modified: Tue, 12 Jul 2022 03:21:55 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b28d51fe86eafab9bc2ff605cf06c2132c0039ef3c821bd186479dd9c638fb6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156423344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17106fa5a11aff94eee0611318c0b17d143f773650ba93cccd17585a268bc75`
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
# Wed, 20 Jul 2022 03:39:24 GMT
ENV RUBY_MAJOR=2.7
# Wed, 20 Jul 2022 03:39:25 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 20 Jul 2022 03:39:26 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 20 Jul 2022 03:41:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 03:41:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 03:41:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 03:41:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 03:41:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 03:41:17 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 07:23:48 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 07:23:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 07:23:57 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 07:23:57 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 07:23:58 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 07:23:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 07:24:00 GMT
ENV REDMINE_VERSION=4.2.7
# Wed, 20 Jul 2022 07:24:01 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.7.tar.gz
# Wed, 20 Jul 2022 07:24:02 GMT
ENV REDMINE_DOWNLOAD_SHA256=ed4be03b5ab63c2641a87db8978739dd997c0f646bfa1010ac9e5210c343724e
# Wed, 20 Jul 2022 07:24:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 07:24:07 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 07:26:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 07:26:40 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 07:26:41 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 07:26:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 07:26:42 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 07:26:43 GMT
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
	-	`sha256:c0b315d84b71a6d454023a220d15330525a0806f87dd07d5dab6ce57faeed53f`  
		Last Modified: Wed, 20 Jul 2022 03:46:17 GMT  
		Size: 13.8 MB (13814057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a0363bf4d08d735e6edfe7663d4c8801b1d7731edc38455937b8b2fff9cf15`  
		Last Modified: Wed, 20 Jul 2022 03:46:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be59a5770d9be7526cf7aefaf8ed8924f9a437d645b84255cc03afc0026d4a75`  
		Last Modified: Wed, 20 Jul 2022 07:28:46 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b668507668bb530f3b0f6679516580e590f336d4da8d80e6e0aa30e324617adf`  
		Last Modified: Wed, 20 Jul 2022 07:28:57 GMT  
		Size: 79.6 MB (79646504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05bd09b96fd6602bda600cd0c0cb948583d48dd7c719ff67f36434c094b4193`  
		Last Modified: Wed, 20 Jul 2022 07:28:43 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80792acfd6b419b029430fa351214b04a269feea1d4613d2d103c50451a59b4`  
		Last Modified: Wed, 20 Jul 2022 07:28:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123d6365b4e5b58bfaff2136b1c88fb52e84e75f9e5a3c8ce6c850595d93bec9`  
		Last Modified: Wed, 20 Jul 2022 07:28:44 GMT  
		Size: 3.1 MB (3067734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2832098dbba2768d137ad78fb31502c010820b3ebb4def39912e85ad716ed3`  
		Last Modified: Wed, 20 Jul 2022 07:28:50 GMT  
		Size: 53.5 MB (53528245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c19bcc6b19230f42ae2293190cb6ff0668bf71545a48781269b70ab40ea0d9a`  
		Last Modified: Wed, 20 Jul 2022 07:28:43 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine` - linux; 386

```console
$ docker pull redmine@sha256:199a35bfc2f973011aac1333035818a107a3078462fdb90e90e8c29fd52f8b72
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159889826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a6d74c15859a05b644b868410d8a1e50f19c3774e2cb0a4417193bac7d2143`
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
# Wed, 20 Jul 2022 02:14:28 GMT
ENV RUBY_MAJOR=2.7
# Wed, 20 Jul 2022 02:14:29 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 20 Jul 2022 02:14:30 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 20 Jul 2022 02:16:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 02:16:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 02:16:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 02:16:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 02:16:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 02:16:16 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 03:44:29 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 03:44:39 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 03:44:40 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 03:44:41 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 03:44:42 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 03:44:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 03:44:44 GMT
ENV REDMINE_VERSION=4.2.7
# Wed, 20 Jul 2022 03:44:45 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.7.tar.gz
# Wed, 20 Jul 2022 03:44:46 GMT
ENV REDMINE_DOWNLOAD_SHA256=ed4be03b5ab63c2641a87db8978739dd997c0f646bfa1010ac9e5210c343724e
# Wed, 20 Jul 2022 03:44:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 03:44:56 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 03:47:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 03:47:11 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 03:47:12 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 03:47:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 03:47:13 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 03:47:14 GMT
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
	-	`sha256:9e84ce0fec4a347f25b69b6b67a399058fb791bf82b673b3619aa836476e979a`  
		Last Modified: Wed, 20 Jul 2022 02:21:33 GMT  
		Size: 13.3 MB (13292772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd2a6594a9bd92179baea911d07588fbf4923e9bb5b9dcd6bc8032dcaf4be5f`  
		Last Modified: Wed, 20 Jul 2022 02:21:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f49629004b39b7365ff2aef9232845ff59df3bf7e7c819a101251da4101f01`  
		Last Modified: Wed, 20 Jul 2022 03:49:20 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ef4592a38c6bba0adf45871af33c3b69ec11dca5ec696330f21ebbfc2d1297`  
		Last Modified: Wed, 20 Jul 2022 03:49:38 GMT  
		Size: 84.0 MB (84033438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9940a0adbae4f61beca5b2a9e11561a500213907a7d2d71097172ac3f314edf`  
		Last Modified: Wed, 20 Jul 2022 03:49:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a37b72cfddffe1871bb8fd35e358ab0dae7695cdc0e5edfcfa08d56db74bd1`  
		Last Modified: Wed, 20 Jul 2022 03:49:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb552a80874092fc07c8ffce310de183468350d210537b7f125ba92e7b79de8`  
		Last Modified: Wed, 20 Jul 2022 03:49:19 GMT  
		Size: 3.1 MB (3067775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd745bf2b661a52d1e3e2d94ba72c20e24c7648b6f23ccd8f8d7dee5cf79b83`  
		Last Modified: Wed, 20 Jul 2022 03:49:25 GMT  
		Size: 53.0 MB (52963521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2430d669f3e4792e8fc161b4982fd4556a3385cccc2ed5ba986ec5d51a0814`  
		Last Modified: Wed, 20 Jul 2022 03:49:18 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:54fdad8f272560a9c847e38a5c19d3f8a5bfe2768e765852c05aceb1c690fb3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161265977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f00dedaeed18533a7554d15eefd1ce009c985ec3cacf435abafaddcd0ea65ef`
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
# Wed, 20 Jul 2022 06:04:36 GMT
ENV RUBY_MAJOR=2.7
# Wed, 20 Jul 2022 06:04:43 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 20 Jul 2022 06:04:46 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 20 Jul 2022 06:07:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 06:07:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 06:07:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 06:07:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 06:08:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 06:08:13 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 08:52:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 08:54:02 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 08:54:09 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 08:54:13 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 08:54:19 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 08:54:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 08:54:30 GMT
ENV REDMINE_VERSION=4.2.7
# Wed, 20 Jul 2022 08:54:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.7.tar.gz
# Wed, 20 Jul 2022 08:54:35 GMT
ENV REDMINE_DOWNLOAD_SHA256=ed4be03b5ab63c2641a87db8978739dd997c0f646bfa1010ac9e5210c343724e
# Wed, 20 Jul 2022 08:54:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 08:54:58 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 08:59:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 08:59:35 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 08:59:38 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 08:59:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 08:59:47 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 08:59:50 GMT
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
	-	`sha256:e4d7fd4bf29ffffcc583c1782abe94099a499957e64a4077d29212319f8f136b`  
		Last Modified: Wed, 20 Jul 2022 06:14:22 GMT  
		Size: 14.4 MB (14419507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ccbe1e24959b9847745d64a280df57ffc79dcc64e72f7529f11d3570594e7d`  
		Last Modified: Wed, 20 Jul 2022 06:14:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb00ab1bc850073dba3eff7de650a1d4d2c87db6f0f3599587c7ebe82b2e01c`  
		Last Modified: Wed, 20 Jul 2022 09:02:52 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd997e570149a29c7d7adecfcff09280f968fc96888afb79fc3da94098fc3d5`  
		Last Modified: Wed, 20 Jul 2022 09:03:05 GMT  
		Size: 82.7 MB (82657894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd7230f13e90a5ef275f65acc3e4bfa178715d86423e2de5716d7f85695518f`  
		Last Modified: Wed, 20 Jul 2022 09:02:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8417588b78425801dd43a6aac9bb4d9a4904657e7aff503370024825c4ed871c`  
		Last Modified: Wed, 20 Jul 2022 09:02:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44abb01b505fa9254d6ce2a7565a04a9dda70bb0d32540148af2fb71257e7461`  
		Last Modified: Wed, 20 Jul 2022 09:02:48 GMT  
		Size: 3.1 MB (3067303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4de53a957567928fe8e38e70c49d432ccdb74cd0dd64eae1db152c43acd05e`  
		Last Modified: Wed, 20 Jul 2022 09:02:54 GMT  
		Size: 54.5 MB (54505476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112eb457c398c07a7c78fa85f7f2b0aa3c5b8b8d20c77082a00fea62ebe426ea`  
		Last Modified: Wed, 20 Jul 2022 09:02:46 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:4-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:398eb2eaa48f0104cd1b56732c90aed61aea896560290e22dac000de60729434
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152067633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b997b25511173b3a6fb5c447cd084a9a0041000eae1618e32aba5f43d21539bb`
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
# Wed, 20 Jul 2022 01:29:19 GMT
ENV RUBY_MAJOR=2.7
# Wed, 20 Jul 2022 01:29:20 GMT
ENV RUBY_VERSION=2.7.6
# Wed, 20 Jul 2022 01:29:20 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Wed, 20 Jul 2022 01:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 20 Jul 2022 01:31:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 Jul 2022 01:31:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 Jul 2022 01:31:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 01:31:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 20 Jul 2022 01:31:42 GMT
CMD ["irb"]
# Wed, 20 Jul 2022 06:43:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Wed, 20 Jul 2022 06:44:00 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Wed, 20 Jul 2022 06:44:13 GMT
ENV RAILS_ENV=production
# Wed, 20 Jul 2022 06:44:14 GMT
WORKDIR /usr/src/redmine
# Wed, 20 Jul 2022 06:44:15 GMT
ENV HOME=/home/redmine
# Wed, 20 Jul 2022 06:44:16 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 20 Jul 2022 06:44:17 GMT
ENV REDMINE_VERSION=4.2.7
# Wed, 20 Jul 2022 06:44:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.7.tar.gz
# Wed, 20 Jul 2022 06:44:18 GMT
ENV REDMINE_DOWNLOAD_SHA256=ed4be03b5ab63c2641a87db8978739dd997c0f646bfa1010ac9e5210c343724e
# Wed, 20 Jul 2022 06:44:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 20 Jul 2022 06:44:27 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 20 Jul 2022 06:47:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Wed, 20 Jul 2022 06:47:11 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 20 Jul 2022 06:47:12 GMT
COPY file:ec5edc991e6c7f0c678e0703e1db651c89473a4619b1fd7c6e950c773cedccf4 in / 
# Wed, 20 Jul 2022 06:47:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 20 Jul 2022 06:47:13 GMT
EXPOSE 3000
# Wed, 20 Jul 2022 06:47:13 GMT
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
	-	`sha256:c3ff56be72e55d9303d139350f4b646cae995ac3b47a29cd7fc9881581b9ad5e`  
		Last Modified: Wed, 20 Jul 2022 01:37:15 GMT  
		Size: 14.1 MB (14127585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a3759ebe715d91b14df2abd81b26b7beb721b15cbb0f62ed2d204b0d929f7`  
		Last Modified: Wed, 20 Jul 2022 01:37:14 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2367af4600b28242f6f66c5f4159caa158988ba895823d1ef0b5b238cf46e822`  
		Last Modified: Wed, 20 Jul 2022 06:49:06 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531d44382c069f938e2bb0113010e096da37f5303e1df1c2bde62a5e7cd7a735`  
		Last Modified: Wed, 20 Jul 2022 06:49:16 GMT  
		Size: 74.5 MB (74502718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61e0e9c3e7dce509b8ed80a1332e123f8be24153d0eeca2d8af773a179d7905`  
		Last Modified: Wed, 20 Jul 2022 06:49:05 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f6d460052b9b9cda678067a5474f1a48fdda21f8c068beefd376a8f155e285`  
		Last Modified: Wed, 20 Jul 2022 06:49:05 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d220867af84aa2fe3390a2de432a10fb7c8ae06e9392e50739a913c66b5843`  
		Last Modified: Wed, 20 Jul 2022 06:49:06 GMT  
		Size: 3.1 MB (3067246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055bc0ba38f008d72610d58aa2e7a256d312dbef905a17c1230f8cc225f6b802`  
		Last Modified: Wed, 20 Jul 2022 06:49:10 GMT  
		Size: 54.0 MB (54019433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be43f18e2ccaab491990ed012dd231ce80233664809b8cc8abc2eff547609577`  
		Last Modified: Wed, 20 Jul 2022 06:49:05 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
