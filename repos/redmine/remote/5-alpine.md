## `redmine:5-alpine`

```console
$ docker pull redmine@sha256:300ca2583f79ab601aa2be3a380490d2cbe7e42da70424073ace7ff36cdec624
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redmine:5-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:78fe663a6a036106d1d5e3102912cb2033d859ecbfe15815532bf5caf22e1b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200256432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10f0927f730ef48fdee33a392ba0c29ba51d521fc2cf95e90744bb23181fbc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a8585674a557b74369940cee1c8f3d0023fe67c6dd0abdaf38a29ecbc41be0`  
		Last Modified: Fri, 15 Mar 2024 23:58:25 GMT  
		Size: 4.1 MB (4131288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1075e363b98a5de2fa73dd7c47a09ec63c4139e02056a62d808073fd4611878`  
		Last Modified: Fri, 15 Mar 2024 23:58:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d57ba319366e32ae4a915e19b1391bc4de326abfc74d497d5b63d4d3b0a9f0`  
		Last Modified: Fri, 15 Mar 2024 23:58:26 GMT  
		Size: 32.0 MB (32010704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31f18deb5c70ffc51bc325c1acc0d821db8186af60a10381fad9a3802dab9c4`  
		Last Modified: Fri, 15 Mar 2024 23:58:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542ce807c23e80b9440cb1e180a7394f68ca8d3ec0027d374b17594da7c00e6e`  
		Last Modified: Sat, 16 Mar 2024 00:56:17 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae98ca6120a2fa3178bd5cecf31a3c4c2fdac05bc22d93e35d59fa66604af1`  
		Last Modified: Sat, 16 Mar 2024 00:56:18 GMT  
		Size: 87.4 MB (87360834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0ce8dbef528fa83eff7d927790f0bfb5e986f40fe8aec75d4ecebaee8ceff7`  
		Last Modified: Sat, 16 Mar 2024 00:56:17 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4367fb62afc27741c4be6fac78f4dbb29cbf269f4e30954ef81ed246fa0b55`  
		Last Modified: Sat, 16 Mar 2024 00:56:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9131a56faa2b4900b7b616af6d8fc67f3365fe784965ca918b7f917f41b53af`  
		Last Modified: Sat, 16 Mar 2024 00:56:18 GMT  
		Size: 3.2 MB (3242761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c92cab4af0a6e4f7c88201634e8b7ac02a2c883ba2489627f4987ff3f006f5e`  
		Last Modified: Sat, 16 Mar 2024 00:56:20 GMT  
		Size: 70.1 MB (70104491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817ab9df0b88c8844e1ed5b90230cf384430a0bafb14b80d42f16f41b6f32f62`  
		Last Modified: Sat, 16 Mar 2024 00:56:18 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:daaaa1ebfa559eb842f19982748e64550dbb666db4347ff7d2df35d548b38e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5640828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff1c7447b157716eaae9eeb7236577a351f2e35e7d1a5d083df33416145216b`

```dockerfile
```

-	Layers:
	-	`sha256:85b64ec24419121b15b3fc0269ed5d16845569a79da769ce4a6d9823a805e090`  
		Last Modified: Sat, 16 Mar 2024 00:56:17 GMT  
		Size: 5.6 MB (5605605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dfce568d49fe6ea5ef57cd958cf26de2dce7c71095c16725835be0755acd159`  
		Last Modified: Sat, 16 Mar 2024 00:56:17 GMT  
		Size: 35.2 KB (35223 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:ec37d8a8653ba653e0963842993a19c721a5456d9d83867c703bd699112daa98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 MB (190757827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b9c3500c43ff72d11d52ea038dc972c97c050636cc238ee2fb7b02e2e1b70b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081f948b823705d53f07b08e664a3985f747b9f710e4346a0df21cf52dacf9f5`  
		Last Modified: Tue, 30 Jan 2024 22:34:19 GMT  
		Size: 3.8 MB (3807320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccabb71f26ec4e81e1605fa1f024fa2c68489d1d7da23aca499ee2ed0ee31954`  
		Last Modified: Tue, 30 Jan 2024 22:34:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db36c2ac88b0b4d442702368faa29614da2425dec55999195091fe51ddc052d`  
		Last Modified: Tue, 30 Jan 2024 22:39:05 GMT  
		Size: 28.1 MB (28141618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c99dd01e6c135fd44b73ec8cc25f226513f4219d80c7575629ce050e640120`  
		Last Modified: Tue, 30 Jan 2024 22:39:04 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dab7aae5b943499de8aecbb808e456d1500ba3506149bab4c0e38bdabf7778`  
		Last Modified: Tue, 05 Mar 2024 00:52:18 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501b3cea73840c8c8b39146608f38d49922fc75d4b38b5cae6b287d627d3ce03`  
		Last Modified: Tue, 05 Mar 2024 00:52:21 GMT  
		Size: 82.9 MB (82898019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8754ca302266b063ec50f5c4d8429173803e6e315a5c9336263f29bba5acf200`  
		Last Modified: Tue, 05 Mar 2024 00:52:18 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57512840cdbbae6ded5d1760ff2adc2b0a37bdd09ec38c0805c3f9f6149297eb`  
		Last Modified: Tue, 05 Mar 2024 00:52:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5571b2381f68d44a94781865c2121162af9d5720f1b533a3e7695e4a602ec776`  
		Last Modified: Tue, 05 Mar 2024 00:52:19 GMT  
		Size: 3.2 MB (3242276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754e4eff9d0de54df3929efcee0b22fb3658cd3b53394a4d0ff724d2befffd6b`  
		Last Modified: Tue, 05 Mar 2024 00:52:21 GMT  
		Size: 69.5 MB (69517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc9ce150581d3d67333906d0c344f74e64867f4dac1ded7a10513a1b6be5d9`  
		Last Modified: Tue, 05 Mar 2024 00:52:19 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:030dc5b387e5526f7d1d10c801ad4efeb2cf24cec232d6c26dac0182cc31418e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 KB (35167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc8967349de0b84662ef0f9ffef5eb8f0bd6c3068bc312ac27f9728d3d8a977`

```dockerfile
```

-	Layers:
	-	`sha256:02bd217b57511b1e44a1e1e933b6cc985736349703a1755041dc9cd2107ac893`  
		Last Modified: Tue, 05 Mar 2024 00:52:18 GMT  
		Size: 35.2 KB (35167 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:fa0c207eeaa1186e5ae79e1d6f0405066aab27c45c7f992de262a3fe3620d805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185788626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c37797355eb4ecde91d9f39362426bc920b7326ead058685b0bef0f19d62a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0024e184ce899205e2450f8f2b33be31d0264636f395ec416b756755089189d3`  
		Last Modified: Sat, 16 Mar 2024 18:03:00 GMT  
		Size: 3.7 MB (3717087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d2ff0bc9c4fcf8807846cd7cdeeb2c3a3ed5d647d6e1e9c6b3afa13c0d033`  
		Last Modified: Sat, 16 Mar 2024 18:02:59 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7d782215bb4582a4ff680389fca39b85e737535a6a1dd9285f702a9b3ff93c`  
		Last Modified: Sat, 16 Mar 2024 18:17:49 GMT  
		Size: 28.0 MB (28001162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee680621325d33d2f2308ec6ab1acfbb1843436157d45ee97e2da64a5e74d1ec`  
		Last Modified: Sat, 16 Mar 2024 18:17:48 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48b0b589720322eb9cc32601012ad7ad7a81cd30de9ad1a564aa85b4affb75e`  
		Last Modified: Sat, 16 Mar 2024 22:42:54 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8153a543e3bd234f506d1af0e48bcec95bd67d9c9f01448c5b0305550adbe471`  
		Last Modified: Sat, 16 Mar 2024 22:42:56 GMT  
		Size: 79.4 MB (79383399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551f670703f937de963d05d1ab8de840fe691f6008273504289f3f73dbceda50`  
		Last Modified: Sat, 16 Mar 2024 22:42:54 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7de526667a070a80674bb200415a67fe44c1d57b2ec931abede9d1d9f73e2ec`  
		Last Modified: Sat, 16 Mar 2024 22:42:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7ab07ec0a730328670d895330465a137b80cfb588dcf48e592ba36cb8402d3`  
		Last Modified: Sat, 16 Mar 2024 22:42:55 GMT  
		Size: 3.2 MB (3242742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e129559b40e278367064460a934860845fb16046504b6ec7df55f2d78b55e4f4`  
		Last Modified: Sat, 16 Mar 2024 22:42:57 GMT  
		Size: 68.5 MB (68539024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd30a2deb676186ec1de34032b7327344eafcc4330c84a98b661cf4da63f87f`  
		Last Modified: Sat, 16 Mar 2024 22:42:55 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:780cb9be031a4e8eb4a7fa8ccb4e2f6bedff2ba64984014ed3d297253d39d1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f871968f3a4e76698013b25d60065c28038fd308e1b07f7656dd72ca9c457c77`

```dockerfile
```

-	Layers:
	-	`sha256:abb5a15ff44b4e1c8558ed4d24441a0102c65cad0717ee10957f5f4403af25dd`  
		Last Modified: Sat, 16 Mar 2024 22:42:54 GMT  
		Size: 5.6 MB (5587648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:791b34309e046a0449a5e9c12062f6e361a04629c5f71c96c320bd1546a272dc`  
		Last Modified: Sat, 16 Mar 2024 22:42:54 GMT  
		Size: 35.4 KB (35437 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:efc7c1aa3eecaa9e23bbd704894b65dd330f5e44de52b14929a16169880c2051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199660212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb18dfa91e330d05a31281f877636bc4944868526150a543545fc7421abb0468`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d002cb486864f216503b0e91a5fbfa1d4bff221bedad1208479f784d068c0ca6`  
		Last Modified: Sat, 16 Mar 2024 17:00:31 GMT  
		Size: 4.1 MB (4061386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73f9a3c5db2eccc0dbf307416289b5d4fa59b45ae3ae604086cb3c854fecba`  
		Last Modified: Sat, 16 Mar 2024 17:00:31 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c32f037d50794af3db511d5fad8884f3a2942c0ad141c21541d3e132c9deda2`  
		Last Modified: Sat, 16 Mar 2024 17:04:56 GMT  
		Size: 32.0 MB (32005787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60541ab401691fd91ae4124d22d0de7668be0224ffe2893b110d30ed59cf62e6`  
		Last Modified: Sat, 16 Mar 2024 17:04:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff56792472174a45a85a8d6d63b9f9fe0baa7c5ae1b735bf9e591cf42c24f2e`  
		Last Modified: Sat, 16 Mar 2024 20:29:41 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76f2144c0976cb904a1c011364646f55182629de49e31abb0dcef8385992844`  
		Last Modified: Sat, 16 Mar 2024 20:29:44 GMT  
		Size: 86.8 MB (86807205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6c1ccb0000bb79166a8533858e3852255c4184662c21f68bf2afc9e5ad06ed`  
		Last Modified: Sat, 16 Mar 2024 20:29:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b79301a5192ccf5ef12ead9402fdadac629813b519651597c8f85133ee1949`  
		Last Modified: Sat, 16 Mar 2024 20:29:42 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d849375b6a83def5c5eb05ad9baba2cceb15f410cd257b48c98573fcde26432`  
		Last Modified: Sat, 16 Mar 2024 20:29:43 GMT  
		Size: 3.2 MB (3242756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2889770f75486a90c561163afe132ee67292e54c3702ad81f65340500a94c5a2`  
		Last Modified: Sat, 16 Mar 2024 20:29:45 GMT  
		Size: 70.2 MB (70205910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c269574e5c5b7785c81025e052304c9615b6ed3f54361f6ec43e8987477a5c`  
		Last Modified: Sat, 16 Mar 2024 20:29:43 GMT  
		Size: 2.0 KB (2011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:8699272e8b11192cc97a19ce0b23415353a70ed10ddf5473cd37f09f755d0723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088a93eb1e965667209db264137526876b2fe7e40e4c3e9e91b8caf2867b6d42`

```dockerfile
```

-	Layers:
	-	`sha256:543359b6686cbcccce7671559f3c6e17a0e864e552af7c69d98a77aaa8ff198c`  
		Last Modified: Sat, 16 Mar 2024 20:29:42 GMT  
		Size: 5.6 MB (5588590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd7e55d36bb702c561b0b5e2b18a0b1ef177c6b475f0a54370b1d2c6b35f2a0`  
		Last Modified: Sat, 16 Mar 2024 20:29:42 GMT  
		Size: 35.3 KB (35301 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; 386

```console
$ docker pull redmine@sha256:1bc56169f1136af1cb393275b2c099fce6c037b56135c05dbdad056c290872cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192904452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1a7114f0104c593f385a1394e3e453127370e626deea6527f0ebab084e056a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad518ba2ee4cbf1294f8db55909f325c4da7376ee7b073bf2bac76fe0b5908c`  
		Last Modified: Fri, 15 Mar 2024 23:58:08 GMT  
		Size: 4.1 MB (4135770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba4254d26a289e3e3341e856ba073254dfd7d4eca50f271c707dbad323e6f3e`  
		Last Modified: Fri, 15 Mar 2024 23:58:08 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c96c462ea6f8e49d89d8fa2c3ce5bf47bbbb473fc01f294921c84dabd97e23c`  
		Last Modified: Fri, 15 Mar 2024 23:58:08 GMT  
		Size: 27.9 MB (27932411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3046a937fa02be7cd7c073f93d8a36047fefb67a5fea12976911272a6daa3c`  
		Last Modified: Fri, 15 Mar 2024 23:58:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd95e2c9e5117e4d9fd18af85fa450ac515383bf4054640d9c4b00f39dac6587`  
		Last Modified: Sat, 16 Mar 2024 00:56:34 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a42caa1778ce9da48f63dc11d7436c7af7e84a261ecc8f0bd7cd733572ef172`  
		Last Modified: Sat, 16 Mar 2024 00:56:36 GMT  
		Size: 84.2 MB (84231119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8419207d5d78893770e90658f0ad8bafe4921958c01c712dd52d322b455fb84b`  
		Last Modified: Sat, 16 Mar 2024 00:56:34 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadcdedda8ccdd5179f4a2e686eb23f3e8917299cd087f3ca5d5f038d4a2fa04`  
		Last Modified: Sat, 16 Mar 2024 00:56:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2101b96fb82c83c776374ad1b509be7e2a97515db2835d72a16e4d9698ed0d`  
		Last Modified: Sat, 16 Mar 2024 00:56:35 GMT  
		Size: 3.2 MB (3242382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d754b3dd99147a92bafe4bc09d6dea6a4f9ea80eff3da01c4d865803cdb76df7`  
		Last Modified: Sat, 16 Mar 2024 00:56:37 GMT  
		Size: 70.1 MB (70119892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0e9890b5a4b5b69c533064ce7052f9361bc5e99a8f3614eec4ea367cb91fc2`  
		Last Modified: Sat, 16 Mar 2024 00:56:35 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:7c9cf22ee645e61b86bb7d303e2de12e03cfbf2add1e913df75797209978ae6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5640499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e802a8886e7fe6f4a8079aa914878db5e69bb1d52ef11ef91a20bf289e4ab2`

```dockerfile
```

-	Layers:
	-	`sha256:12472eb609577863463a3d30529c2ac63cff87bcb3a0e6831c7b8d2fde644488`  
		Last Modified: Sat, 16 Mar 2024 00:56:34 GMT  
		Size: 5.6 MB (5605336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5316e7ac99c8ec697b92eac73671322715a601ddf68327c5aa29440669dbba3`  
		Last Modified: Sat, 16 Mar 2024 00:56:34 GMT  
		Size: 35.2 KB (35163 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:553ae64ae3e25dc5017eaeb8cc7f3685dc468bc1e3023236f5d92341f5642392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205459295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d54011d9ebf3de34b854e06b6a1842a09b731f272d7c8b73507fc0517ea3732`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c6ec9fb504c07d1c16c1b449d00bcc19cc9559e9f63e741d265c315636bea`  
		Last Modified: Sat, 16 Mar 2024 11:45:41 GMT  
		Size: 4.3 MB (4279192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f03c40289ce1a749a54c1b09ca1e696aa84b538250c4fe7a36474bb3e3ea06`  
		Last Modified: Sat, 16 Mar 2024 11:45:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543ad82891f1ed6a2a1fa3722d2a3cc7c74a9613c80e687f1b77cd5422494556`  
		Last Modified: Sat, 16 Mar 2024 11:53:35 GMT  
		Size: 29.3 MB (29311082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94b346a4ea0bf5d0f5c0226a13cd3a73a8dff2c03899a8e9dae5608f3672474`  
		Last Modified: Sat, 16 Mar 2024 11:53:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49d9d6c5b8650b7b10f356140ddccb0b1fec61e249e37df7dcf002f93e3d5e9`  
		Last Modified: Sat, 16 Mar 2024 15:48:06 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc1fe303d77da83241c1a03ca16e87d899f3e55ec316dd64a86c5fdb119c3cf`  
		Last Modified: Sat, 16 Mar 2024 15:48:09 GMT  
		Size: 93.0 MB (92986655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422299aeff82daeda1039ce558867efa138064f27190c4c48cb772a7ab3d4fce`  
		Last Modified: Sat, 16 Mar 2024 15:48:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693729a28a15fd9ac44c6eed3f3eed64a603bb06ca6ab2753f95d0c676b6b7c7`  
		Last Modified: Sat, 16 Mar 2024 15:48:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8d1f8943e20ca2173c663075471317e218dd431de69ee3fd1e8ac6abeede52`  
		Last Modified: Sat, 16 Mar 2024 15:48:08 GMT  
		Size: 3.2 MB (3242782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e7c810beb9e0e66ebb1857ef354c72872ea36a3e4f96ba609dbf3b67f64203`  
		Last Modified: Sat, 16 Mar 2024 15:48:10 GMT  
		Size: 72.3 MB (72287283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00352d6c728cd3780ad4b52481804936fd9bdb67cc2509ac07283f3186a38e41`  
		Last Modified: Sat, 16 Mar 2024 15:48:07 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:3bc187f8b43142acf1f3e0121c6ef85d9c5fbbe031cd800e49230aff55b5d7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb920087ea4b5d014a91f32642bdd67a8577f56c0f5c885f5971e63de7eadc37`

```dockerfile
```

-	Layers:
	-	`sha256:2c65645cd7146de780e7bb8fe514a2e1a9be9fbb521ed77d870d4f720fb74d34`  
		Last Modified: Sat, 16 Mar 2024 15:48:06 GMT  
		Size: 5.6 MB (5595075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7cd8b23b9faa64219ea7fbafefc65f7077591d419680e9710bd0e400cc6a31c`  
		Last Modified: Sat, 16 Mar 2024 15:48:06 GMT  
		Size: 35.4 KB (35353 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:deef047abd4f761c2d1171f124154ca695bbcd199be1f95235f459e047339c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196439555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f27464e8eb8de216ea66ff7056047561a3d5f6c3354507e9951d67eba0991d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Jan 2024 12:03:17 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_VERSION=3.2.3
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Thu, 18 Jan 2024 12:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Thu, 18 Jan 2024 12:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Jan 2024 12:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 12:03:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Jan 2024 12:03:17 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905f468590b180ac946384c664e0231f84b310e2c181f704057a1a7e5773269e`  
		Last Modified: Sun, 17 Mar 2024 07:32:37 GMT  
		Size: 4.2 MB (4235217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8485725f7092ce368f351195ee735dbfc7e91f78899505986278d466a47ce5a1`  
		Last Modified: Sun, 17 Mar 2024 07:32:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9630832971aacac01f1535831e733ed216cc46da10e4eec42a66c81b2311c02`  
		Last Modified: Sun, 17 Mar 2024 08:16:18 GMT  
		Size: 28.7 MB (28737862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b532ee250270ce52685df16ce04f4bce2085d5f83c0fb767a428c429ba3da975`  
		Last Modified: Sun, 17 Mar 2024 08:16:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724831a85a8addfd2fc22f36e954ab56f27b6d63d7a187416edfd87bdba79df`  
		Last Modified: Sun, 17 Mar 2024 18:14:57 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07511a3a071f8cc9a68e06451d721bead4fd8ea6e3015154d027b8799f6caa`  
		Last Modified: Sun, 17 Mar 2024 18:14:58 GMT  
		Size: 86.8 MB (86751006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d402f1ce0c0f61f0195ea73c10103b0884ac1b5a6a124ac1a4cdecec6f2846c`  
		Last Modified: Sun, 17 Mar 2024 18:14:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4cf4aa7a918144044f803a237a5e33856e23080782f2d0468ad0b363986f4e`  
		Last Modified: Sun, 17 Mar 2024 18:14:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd89a62aedf37ab00d5b13b9c6b9a3700e3013201d25042cac83a9a18b27c6a`  
		Last Modified: Sun, 17 Mar 2024 18:14:58 GMT  
		Size: 3.2 MB (3242799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1bf0abd334d94022bb5b92f2bde1dda8db473e60a4e3ed6f4ff36a85c92863`  
		Last Modified: Sun, 17 Mar 2024 18:14:59 GMT  
		Size: 70.3 MB (70251325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e75f900841481a2b9dee2e2bfc56a2220f0c789aec388071cb8e931092f0a2b`  
		Last Modified: Sun, 17 Mar 2024 18:14:57 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:8c66b78c903c0201827696aa5deeac4de46072d7e7a5486cf0a2bd4232bfdb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0e84bd9c8e4aca563513b0ee37c063d1c23f7f670f5e54fc41d67367a9a3cc`

```dockerfile
```

-	Layers:
	-	`sha256:7d2425eb8b22c5a254793226aee9d5b495c7d1a17657448acdcadc899a90ccf4`  
		Last Modified: Sun, 17 Mar 2024 18:14:56 GMT  
		Size: 5.6 MB (5595672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142ecafdbbf35c18e30639224639fae191b46b188ca495be1774d94e6826c0e6`  
		Last Modified: Sun, 17 Mar 2024 18:14:56 GMT  
		Size: 35.3 KB (35277 bytes)  
		MIME: application/vnd.in-toto+json
