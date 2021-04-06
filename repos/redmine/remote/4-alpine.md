## `redmine:4-alpine`

```console
$ docker pull redmine@sha256:29454a31d1cebcdc33cd50b35495532b6756e6608a036133c68263de8089b9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:4-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:9d1c434ac62026273ff39820aad3eb9e532678a54012152712ab1a76311a8139
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164260126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5aa389f0b143c0ea7e350e485f5936594d02e5f31ee239353156b2609330376`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 10:39:43 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 01 Apr 2021 10:39:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 01 Apr 2021 10:39:45 GMT
ENV LANG=C.UTF-8
# Thu, 01 Apr 2021 10:47:42 GMT
ENV RUBY_MAJOR=2.7
# Mon, 05 Apr 2021 19:16:34 GMT
ENV RUBY_VERSION=2.7.3
# Mon, 05 Apr 2021 19:16:34 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Mon, 05 Apr 2021 19:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 05 Apr 2021 19:20:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 05 Apr 2021 19:20:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 05 Apr 2021 19:20:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Apr 2021 19:21:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 05 Apr 2021 19:21:02 GMT
CMD ["irb"]
# Mon, 05 Apr 2021 20:44:40 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine
# Mon, 05 Apr 2021 20:44:48 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		su-exec 		tini 		tzdata 		wget 				git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	;
# Mon, 05 Apr 2021 20:44:49 GMT
ENV RAILS_ENV=production
# Mon, 05 Apr 2021 20:44:49 GMT
WORKDIR /usr/src/redmine
# Mon, 05 Apr 2021 20:44:49 GMT
ENV HOME=/home/redmine
# Mon, 05 Apr 2021 20:44:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Mon, 05 Apr 2021 20:44:51 GMT
ENV REDMINE_VERSION=4.2.0
# Mon, 05 Apr 2021 20:44:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=295864c580afa2a926e7a17f2ad10693f9b7a6d9f1ef523edb96b2368e7f07e5
# Mon, 05 Apr 2021 20:44:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Mon, 05 Apr 2021 20:44:55 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 05 Apr 2021 20:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps
# Mon, 05 Apr 2021 20:47:14 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 05 Apr 2021 20:47:14 GMT
COPY file:d7d49d1509d97205d05405670ad206509bb871741a17d5270a1b8842b05afc0f in / 
# Mon, 05 Apr 2021 20:47:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 05 Apr 2021 20:47:15 GMT
EXPOSE 3000
# Mon, 05 Apr 2021 20:47:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9df2de4dab84e51acacca9e65a3d9f7c9fa2f038bc11c2830bd9a97980823a0`  
		Last Modified: Thu, 01 Apr 2021 11:09:32 GMT  
		Size: 1.2 MB (1218696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc339b259bb6448a756fb9b42044f3450a7dcd6fc3bc0102a3cb6b7594daca19`  
		Last Modified: Thu, 01 Apr 2021 11:09:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bf4c0832c8a73d79344879220b7a99ed4ecccf6eb758384bec64d8719c63b8`  
		Last Modified: Mon, 05 Apr 2021 20:15:04 GMT  
		Size: 23.2 MB (23207724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0141082ecc3e69444f52c2c25989a96c26e3f1db52ed818a2415be78f134a`  
		Last Modified: Mon, 05 Apr 2021 20:15:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed39d01534357156db6127eb2e8773b4392a8e1f7eeda26f6ee1e2a8e546bab7`  
		Last Modified: Mon, 05 Apr 2021 20:58:52 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a15e47cfeac0ace560ab1a638fc48e9778fd707f93c1e1f0f5ce10485c02ff`  
		Last Modified: Mon, 05 Apr 2021 20:59:04 GMT  
		Size: 69.4 MB (69428125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e444a04c0290dbedcaf3c8c2b51834f611b133a5d3972177b6cf6e8a7a8bd26`  
		Last Modified: Mon, 05 Apr 2021 20:58:49 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d2998285fcc9b3ccd853c688ece46d699af9032ff15b3ce80d713c179b9ca2`  
		Last Modified: Mon, 05 Apr 2021 20:58:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0bf3df829a8a10618bbfe5772d98aeda38ab59effc18261703062cb5ade296`  
		Last Modified: Mon, 05 Apr 2021 20:58:50 GMT  
		Size: 3.1 MB (3058322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c7fbf7457fdf8ee116d68493251899d90f8b5d5f7ae60fbcdb6f2580965ec`  
		Last Modified: Mon, 05 Apr 2021 20:58:56 GMT  
		Size: 64.5 MB (64531585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ebb1f89b905c30adc636a07475d0f7e1720a4b3cc15d4ea8e30ab637c91b7e`  
		Last Modified: Mon, 05 Apr 2021 20:58:49 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
