## `redmine:alpine3.19`

```console
$ docker pull redmine@sha256:5ec9cae5ef9528240d1d8ce29eb7e4dbbb80bb5eb6b76948b2cb17fa64548d13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redmine:alpine3.19` - linux; amd64

```console
$ docker pull redmine@sha256:c5d6420721bd4eff480cb8f3bc0fedbf40ac3b751b8a544a11cb4949f54a47c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192221210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d66edb210b79db12f0ecbc3f4c051e67956c9736f37f9e57dd6f0eea6f1417`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
# Wed, 29 May 2024 20:43:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV RAILS_ENV=production
# Wed, 29 May 2024 20:43:51 GMT
WORKDIR /usr/src/redmine
# Wed, 29 May 2024 20:43:51 GMT
ENV HOME=/home/redmine
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_VERSION=5.1.2
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 May 2024 20:43:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 May 2024 20:43:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 20:43:51 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 May 2024 20:43:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43df776e26ade67d440b1c67ab7a3de807b6d05ac51329501849868366257fce`  
		Last Modified: Tue, 23 Apr 2024 16:55:13 GMT  
		Size: 6.7 MB (6676579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14332fdfab7fe54dd2807d4e399da596d9f533f8f40c0014d3d99b7581cd4cc0`  
		Last Modified: Tue, 23 Apr 2024 16:55:12 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c247c39d7b0ddfe61bdc9a30c801cdd72422bedf6fc0b57da978566199a07e8a`  
		Last Modified: Tue, 23 Apr 2024 16:55:13 GMT  
		Size: 34.3 MB (34253180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2810796b8b97b6ee57092452ba105465a85be3a3c6fd128279bf3ae1971b2a57`  
		Last Modified: Tue, 23 Apr 2024 16:55:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21420248cd794462641e240ef1903310416a0d3fad1ccd1267d5a8ab96a5383d`  
		Last Modified: Thu, 30 May 2024 01:01:58 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc7d9fb160a95c3a25dbc2b79f6a7f0d074d0132d2493360173c12e1dbffc17`  
		Last Modified: Thu, 30 May 2024 01:02:00 GMT  
		Size: 71.7 MB (71692559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f02125f3aa00e0d9758b5d887781a193248e23ffd3fd0634eefbf61cd198f`  
		Last Modified: Thu, 30 May 2024 01:01:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719cefccdf7076b2d9258447f5038f2342d818e3be883efd13a513d1f0f859e5`  
		Last Modified: Thu, 30 May 2024 01:01:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09b2b56cf274e44c3f649863dba9ba60f613ff750fa0ab9ea3795ce85547df`  
		Last Modified: Thu, 30 May 2024 01:01:59 GMT  
		Size: 3.2 MB (3243030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9bf83cfca95de18eaaa41a21238fc4b582c894c6c97ab5254072e1623ef834`  
		Last Modified: Thu, 30 May 2024 01:02:01 GMT  
		Size: 72.9 MB (72943318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a9a02c8df0b504c0b482e674b349d2c00938337b65313b5b2bc8b212cb5028`  
		Last Modified: Thu, 30 May 2024 01:02:00 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:120c899e3ca81c92d60b3f2656e6a570ad13b7dd3e8e123493bf616490f0c3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (32998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda041bfebff4d2e54f39206588bbb113f488883b88d15bd20e792d66364b2da`

```dockerfile
```

-	Layers:
	-	`sha256:36df65e45f6c1c18020abeba2e69479f27102f6893165c7a4cf814028dbe9bf6`  
		Last Modified: Thu, 30 May 2024 01:01:58 GMT  
		Size: 33.0 KB (32998 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; arm variant v6

```console
$ docker pull redmine@sha256:dfaa117fdef3ed1ca6bca7796a696f544f06a07957551d88031337f793fdbf02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186057856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb5a6ecada1036d4d68f3d3418beba39f1b68d975d01eba3855c71af48d077d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
# Wed, 29 May 2024 20:43:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV RAILS_ENV=production
# Wed, 29 May 2024 20:43:51 GMT
WORKDIR /usr/src/redmine
# Wed, 29 May 2024 20:43:51 GMT
ENV HOME=/home/redmine
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_VERSION=5.1.2
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 May 2024 20:43:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 May 2024 20:43:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 20:43:51 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 May 2024 20:43:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f8c6c0c6aa88fd99f6786a1c791821d9aea036391577e6f2d658784d63f1b5`  
		Last Modified: Tue, 23 Apr 2024 16:57:39 GMT  
		Size: 6.5 MB (6527591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ddb5de675276eafcbbd223d249fd6a95d47daf5aa86d8f92d51691ec9fe624`  
		Last Modified: Tue, 23 Apr 2024 16:57:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd914934fec755dd84e2b41994de1dadb96c6da55c54e68c1989358df0c44706`  
		Last Modified: Tue, 23 Apr 2024 17:03:37 GMT  
		Size: 30.1 MB (30075394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce2831225336e2fb4a80a1b1b91fb67e0cd534fb5453f1f99e9329914ca6870`  
		Last Modified: Tue, 23 Apr 2024 17:03:36 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b39aeb7928e7cafb608d570f5caac5b97b9cca0a7a897e2038bdc405897a2bd`  
		Last Modified: Thu, 30 May 2024 01:18:41 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bcb947e78ce9dd4be0286fc724e0b5c95589e06aeeda7e17bedc6cbf87c176`  
		Last Modified: Thu, 30 May 2024 01:18:43 GMT  
		Size: 71.1 MB (71076485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d86890f6406776aa237a32bb2419197d7364faf87f21315c9b740687bba3350`  
		Last Modified: Thu, 30 May 2024 01:18:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b1f6e204c25276741112b01a9931493a0b0fb6d10fbf9bb9601c7372fbe9e9`  
		Last Modified: Thu, 30 May 2024 01:18:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e42da5bc0f4be576bb6b38c8871969dbc37a2b8200d92ede3825f771e9d3203`  
		Last Modified: Thu, 30 May 2024 01:18:42 GMT  
		Size: 3.2 MB (3242839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ede3736d742e08645d34fb34ab6aafe1ebb9b9dc5de020ac35ea8123fb65938`  
		Last Modified: Thu, 30 May 2024 01:18:44 GMT  
		Size: 72.0 MB (71966334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4461b9746e949d6015537c1826f87172cf3f73162307498e135e704405465d`  
		Last Modified: Thu, 30 May 2024 01:18:42 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:324159cbe941f78220565933576e640652248f286e21bdb90eef668af9419b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f671e9f1882480b7b8b9cf35f937be2de72826e6d988df4efe8da7b031cc27`

```dockerfile
```

-	Layers:
	-	`sha256:0beb8d3bbcf4f92ea2933ba3b3750a13d7643ee06d226b49942bc07cfd7c9ecd`  
		Last Modified: Thu, 30 May 2024 01:18:40 GMT  
		Size: 33.2 KB (33173 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; 386

```console
$ docker pull redmine@sha256:43bb004fac9300d570769b93ab512b44c81979aed264acd5642403f0a42004c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188427432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6450d2ec446a5b8bb5787d7772c811d14db0b36fda3e13c55f4fee36d0a1214b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
# Wed, 29 May 2024 20:43:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV RAILS_ENV=production
# Wed, 29 May 2024 20:43:51 GMT
WORKDIR /usr/src/redmine
# Wed, 29 May 2024 20:43:51 GMT
ENV HOME=/home/redmine
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_VERSION=5.1.2
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 May 2024 20:43:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 May 2024 20:43:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 20:43:51 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 May 2024 20:43:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be11e62a35be538a866e7a4e22a18be1605065ec12380dcb83e44921ba3f6cdb`  
		Last Modified: Tue, 23 Apr 2024 16:55:38 GMT  
		Size: 6.7 MB (6743174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206e791ffb16f6d00aae50efeef4ff25cf3af70fa0ac902cb6689ce89381a3bf`  
		Last Modified: Tue, 23 Apr 2024 16:55:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93229ebbecf6b198ed398e078ad455b353e7bbc77840d46c3ce0d38ec53a21c0`  
		Last Modified: Tue, 23 Apr 2024 16:55:39 GMT  
		Size: 30.1 MB (30073693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f341b647d9a299fed64834a958a8360086d9178ddfedc6924a52077b4c468ec4`  
		Last Modified: Tue, 23 Apr 2024 16:55:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1575f0e9c072970cc48ba7f8a08e51a0fe520e8b34707d31528653073b373379`  
		Last Modified: Thu, 30 May 2024 01:02:19 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1129880302ddb0e1452685255c44aaa59e5218efdd4d37d003e77ff428ebdda`  
		Last Modified: Thu, 30 May 2024 01:02:22 GMT  
		Size: 72.2 MB (72212970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c39231b9a51865bb5884efc5c4dcdb83d254ba97972c68cb8892b60097a57`  
		Last Modified: Thu, 30 May 2024 01:02:19 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8345d88784b976fcb3626249afc69021d8dc669ad7e96f95d971830bd8dd88fa`  
		Last Modified: Thu, 30 May 2024 01:02:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6dd31fe5290c4913d0dbb8bc448dfc837f4d4d408ffbfe418a6413e4887ecb`  
		Last Modified: Thu, 30 May 2024 01:02:20 GMT  
		Size: 3.2 MB (3243044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b32bb65c2e46676050185b45840e22d7a0d9108d73729dd39b76eaff61d5884`  
		Last Modified: Thu, 30 May 2024 01:02:23 GMT  
		Size: 72.9 MB (72906648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25224a0aaffd359e9d6a18dacb56f13165d38f2e29826c8e6955ea5695caf1fa`  
		Last Modified: Thu, 30 May 2024 01:02:20 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:638114aaf2b20ca5d0437d2019b6a25c7e32a3ae08f9dafcd865ddb3fd46d19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (32959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a64fe81e22a8a8e6c4d74f9189cb8e6812fe97b8f04c09db8a472831dddcf8`

```dockerfile
```

-	Layers:
	-	`sha256:db03c3fd211abab20c57857f97b6bca89e94ec752f110fbc5c1b0a9358befbb2`  
		Last Modified: Thu, 30 May 2024 01:02:19 GMT  
		Size: 33.0 KB (32959 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; s390x

```console
$ docker pull redmine@sha256:487d48dd5d0bd969a2e10610f2723fbfef6f0f49d923953ab316631a658aa43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191147308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf95661539754dfd03490ca660b019b27eaec441b1c8db3461b2d5c69d72217`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
# Wed, 29 May 2024 20:43:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV RAILS_ENV=production
# Wed, 29 May 2024 20:43:51 GMT
WORKDIR /usr/src/redmine
# Wed, 29 May 2024 20:43:51 GMT
ENV HOME=/home/redmine
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_VERSION=5.1.2
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 May 2024 20:43:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 May 2024 20:43:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 20:43:51 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 May 2024 20:43:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c2942d69cd5ff55a03ea14a7eafe7d5ae276592c51e7ef6e0f216195dee137`  
		Last Modified: Sun, 17 Mar 2024 07:25:20 GMT  
		Size: 7.0 MB (7045027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee87adbc3010b909338452c5525a361efacd7aaa932883d320d27b136da4183`  
		Last Modified: Sun, 17 Mar 2024 07:25:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc785ce781b2e6a2827b9b966f2c7b978dac907b715bb1678c85af84ecea5972`  
		Last Modified: Tue, 23 Apr 2024 21:01:35 GMT  
		Size: 31.2 MB (31152164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d60a27bc31c8d35875bc1713b6e26a0b189888e194b1cd5e8c4f280501528`  
		Last Modified: Tue, 23 Apr 2024 21:01:35 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963623ce2b3fc95dd8e37de9aa55d7b9d0b42d65b259ed192de07a22310ad2bd`  
		Last Modified: Thu, 30 May 2024 01:58:31 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6746f720627a1eb40b4b54ad6f496141912c53bd2bb86888625527fd43b2b489`  
		Last Modified: Thu, 30 May 2024 01:58:33 GMT  
		Size: 72.6 MB (72583013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec0bd4ed134fdc56806535c627384ca02b2184ebeb95c35ab72daa5789f0933`  
		Last Modified: Thu, 30 May 2024 01:58:31 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884856f8a1ae10f57afdc0702134d0b43f5473b7e4fe69f9436659d284d82cde`  
		Last Modified: Thu, 30 May 2024 01:58:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6833c72f8cc759771cad544eb136ea8b6d3b3caa9723d8c2ea18df86867b100`  
		Last Modified: Thu, 30 May 2024 01:58:32 GMT  
		Size: 3.2 MB (3242907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3d8656a32901b974fa700bca4aa8fc5c407150c6dc92b74de3a18a132cc302`  
		Last Modified: Thu, 30 May 2024 01:58:34 GMT  
		Size: 73.9 MB (73877749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd2d7822aeb27a7f267b2a5bca3d6575e625127f0fd54cbd21beaccf83f6cfb`  
		Last Modified: Thu, 30 May 2024 01:58:33 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:a0093c61ed6df02fe92c94e244f14d0b2a1bc4366cd5b8ef8404b8fd0aa35101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 KB (33047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308788fdaf6938b06d97bacd26032b7ca1c71b933253a13336b887d761220cd3`

```dockerfile
```

-	Layers:
	-	`sha256:2aa753219775d49653ef8c8cb4e60189bf99d15849bbd7a0787003f9534424e3`  
		Last Modified: Thu, 30 May 2024 01:58:31 GMT  
		Size: 33.0 KB (33047 bytes)  
		MIME: application/vnd.in-toto+json
