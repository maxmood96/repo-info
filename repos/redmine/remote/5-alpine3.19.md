## `redmine:5-alpine3.19`

```console
$ docker pull redmine@sha256:98d8cc99c84f931f05a5b5b0311621c74126dedd06045f4bdf63469493de5bb0
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

### `redmine:5-alpine3.19` - linux; amd64

```console
$ docker pull redmine@sha256:82922a6af4d2a163ba2ae0a2417d06e957b728d8f2183bd86b58f74e6d8dd79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189059843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069e70a9a266b0020d592d3e1b079f54a29fbe5f125cd933247b2bb8589fb48e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Tue, 23 Apr 2024 15:14:18 GMT
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
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5036043291fc7dcc1a743a9e9ce21bc718b43c2f2df28e665269b29350dec660`  
		Last Modified: Thu, 20 Jun 2024 21:00:06 GMT  
		Size: 6.7 MB (6676568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb8c3a6d1df8037b47bc9786fb5c8023594714f2caa0622c5d84c1c351f5f0b`  
		Last Modified: Thu, 20 Jun 2024 21:00:05 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fd5371d939a5d47fc8ad806ec4a04eb75556b83b554f3fae1ea9e3e988c82f`  
		Last Modified: Thu, 20 Jun 2024 21:00:06 GMT  
		Size: 32.1 MB (32060276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1c6535e6ac28a3dd5b21bc961550ebd09f3f2ff86055f39ee265fe2ccdb9f4`  
		Last Modified: Thu, 20 Jun 2024 21:00:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9157b193416288510ce52e1effcd73c951ecdd3f4e07a7cea443bcc48a7320d4`  
		Last Modified: Mon, 24 Jun 2024 23:00:06 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071b8b361e2b0d0af8b2f4cf485f7b3485cc9351e6c91fbecc3fccd3dd4679f`  
		Last Modified: Mon, 24 Jun 2024 23:00:07 GMT  
		Size: 71.7 MB (71694126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b7e37a658118d693850dffb01b6f90761f552efcdb0cf10c5a72c930d98662`  
		Last Modified: Mon, 24 Jun 2024 23:00:06 GMT  
		Size: 1.2 MB (1205370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb1ab8e6fc35590fa447e201535f85830e27f85bc9b1bc3b32c9139d23afa56`  
		Last Modified: Mon, 24 Jun 2024 23:00:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525745e5ce2b3d5055770bdd69321549c8fca42e7ac4f38d41b5735cb32ddf14`  
		Last Modified: Mon, 24 Jun 2024 23:00:07 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484539732b8f01620dd6ea8a40dc860269eef21296f574e9ad2486b8679a62ef`  
		Last Modified: Mon, 24 Jun 2024 23:00:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730ea6c66a748806c120aeaa0d768719287c408109df186213c05b27d1b50c17`  
		Last Modified: Mon, 24 Jun 2024 23:00:07 GMT  
		Size: 3.2 MB (3243989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b65bfd02e32dd0a755ec4ed4bd8c16ec31542dfe2d861570c7e9f5d74a78e3`  
		Last Modified: Mon, 24 Jun 2024 23:00:09 GMT  
		Size: 70.8 MB (70758192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581ee58da0e8eb9599250155b87f9e424314d0c59a144ea42783ffbc7eed9195`  
		Last Modified: Mon, 24 Jun 2024 23:00:08 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:5d71ea6b43faab031f6e9ea7263a4dcac15bd99477174346dfd834be21147a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d50a9cd68060ac6e7c4f71f0dbfbda87f0341fd46863f094d3a40ef4674842f`

```dockerfile
```

-	Layers:
	-	`sha256:b17505c8b7ca6e62620fdba4245be400de8c15215d98ae0f6730e3ab2f7c90ab`  
		Last Modified: Mon, 24 Jun 2024 23:00:06 GMT  
		Size: 42.2 KB (42180 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.19` - linux; arm variant v6

```console
$ docker pull redmine@sha256:4a2db20a02026701c9eac44b7bb671dd931b25e677cba3c199888fdd10b1ab4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183496094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975e0e22e7f5ea3cb5e6bb85d954ecc31168d55064b396642b5eb38b60221dab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Tue, 23 Apr 2024 15:14:18 GMT
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
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc8857d9ff1dc6741d7fab5a706fcd6480a917cf4100804c7cf60771c3bf8b`  
		Last Modified: Fri, 21 Jun 2024 05:04:25 GMT  
		Size: 6.5 MB (6527571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a424814a663df2c8671d47c80c36496ce6ebe5a3536574d279638b96c611aa42`  
		Last Modified: Fri, 21 Jun 2024 05:04:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4a316bcecf005082a4a0c2f7af0382d2681cfe95fd9befb2c0d9e14bb96583`  
		Last Modified: Fri, 21 Jun 2024 05:14:55 GMT  
		Size: 28.2 MB (28201545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b1bad965522f347c355693176cdef1484315667832f16a2177433ca3b34837`  
		Last Modified: Fri, 21 Jun 2024 05:14:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807f39bed0673a690400b82779c5b9a4e896c308bf7eb172beab754ba48146b0`  
		Last Modified: Mon, 24 Jun 2024 23:51:31 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a855aebbceb4c66a76f8172b036a80c229ab2b0e7462d05742c84edaaaa281`  
		Last Modified: Mon, 24 Jun 2024 23:51:33 GMT  
		Size: 71.1 MB (71077818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef21d13a5a464e583c8f2f62d440e4e1b56fc87faed6f82e0a2b5b8adf12527e`  
		Last Modified: Mon, 24 Jun 2024 23:51:31 GMT  
		Size: 1.2 MB (1173276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fbe418c02664db5ab1023a6b14055b9a31b96cff1b86a86e2b397dc30cec46`  
		Last Modified: Mon, 24 Jun 2024 23:51:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c874d23439111473717e8ddd6d2438896219145b5637c66481d48c729f40e8`  
		Last Modified: Mon, 24 Jun 2024 23:51:32 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dcb7f4974c84e3a00e03c6a108c3f08b418b66ab98f2ebe272b15f3447269b`  
		Last Modified: Mon, 24 Jun 2024 23:51:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3156bb67eb0912a4f47c561353f1743f1f22b95bdedf1badd2e2ea59a21468f`  
		Last Modified: Mon, 24 Jun 2024 23:51:32 GMT  
		Size: 3.2 MB (3243893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bcd9f727970164cdad84a62b5168b61ae0b5fd48fcb0442edcf459d01625d2`  
		Last Modified: Mon, 24 Jun 2024 23:51:35 GMT  
		Size: 70.1 MB (70094097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4133165d3ce45763026d4a7a1cc3cba9925aa6c96593289e05fdfffed6c19867`  
		Last Modified: Mon, 24 Jun 2024 23:51:33 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:b977341223ea9ac30a9b3032aa4881e0fa215bc114d74f53528e9ce176f090a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 KB (42394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf04a2ac58977acd16eea85a8f618c1e5d83ff4ec4c5214dc4785a1303584466`

```dockerfile
```

-	Layers:
	-	`sha256:2ac8a79405746357517935890779f3b36117bc20ab19e8ae580a595912c6a4d0`  
		Last Modified: Mon, 24 Jun 2024 23:51:30 GMT  
		Size: 42.4 KB (42394 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.19` - linux; arm variant v7

```console
$ docker pull redmine@sha256:7d8e5c207737dd5d0422398cc148ac6bf64a6432a668a39db76652fb7a751716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177843199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17815aab1d5af89ff3ccc41e7d88e5c2bca3f689e4d1dd1946647411710df7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Tue, 23 Apr 2024 15:14:18 GMT
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
# Wed, 12 Jun 2024 02:38:54 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV RAILS_ENV=production
# Wed, 12 Jun 2024 02:38:54 GMT
WORKDIR /usr/src/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
ENV HOME=/home/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_VERSION=5.1.3
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 12 Jun 2024 02:38:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 02:38:54 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 12 Jun 2024 02:38:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1360df62f2228269d45e6d089fed7b45aa01b0fd1a2824d268ca5ef88bdf1dcd`  
		Last Modified: Fri, 21 Jun 2024 04:53:30 GMT  
		Size: 6.4 MB (6369577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bde30f430ff98c066f803551b87ffccfd124d186bad36c73944aeb5c84eb58`  
		Last Modified: Fri, 21 Jun 2024 04:53:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b498337d19a05e25b77897dbe2b1ef39f75cef3aa60a8e397aebc40fba55ffa1`  
		Last Modified: Fri, 21 Jun 2024 05:04:46 GMT  
		Size: 28.1 MB (28077438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c098e68a7e3f54665fe478afe316cf9f73dea1361dcbbcffaa6cd3a17529b245`  
		Last Modified: Fri, 21 Jun 2024 05:04:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80138b3b65c319a9d6cf94539b0dd7f56fa560d715437ccd8c21103751aa7592`  
		Last Modified: Fri, 21 Jun 2024 13:49:13 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a46c63f1576148e1a876b0216b9df2f254c1adb35f35a2f6d5d59a649612d3a`  
		Last Modified: Fri, 21 Jun 2024 13:49:16 GMT  
		Size: 68.1 MB (68131428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667cc71c71fb87d6fff46fcc9f167a87de29809426e8bc22af4838f34b4baafc`  
		Last Modified: Fri, 21 Jun 2024 13:49:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f2891bd597ac54fa3758f3580d98a32f9281d2b182b52d581eb495a3987fd9`  
		Last Modified: Fri, 21 Jun 2024 13:49:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25301c80c6d5282ad976ef2f0cb9bd6c15206c467aa47784fe1354ecfbb0d06c`  
		Last Modified: Fri, 21 Jun 2024 13:49:15 GMT  
		Size: 3.2 MB (3243950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7899b485866106aa501aced3c06b034a36d58239183c10956d9557a3e6cb9243`  
		Last Modified: Fri, 21 Jun 2024 13:49:17 GMT  
		Size: 69.1 MB (69090502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28340317c37221d833e0096f93423f5ca24259e6dd34e8ea7a8318934121ec3c`  
		Last Modified: Fri, 21 Jun 2024 13:49:14 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:f14cb3f3fdff5e5583aad157b365d571a7756b0452bbee0a15b00a8e2451763a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490f74a6ab8ffe3686cae684da447528200aaf8fe4d0fe9ec5609761f2f062f2`

```dockerfile
```

-	Layers:
	-	`sha256:2041fb4b8161e4ca58e0deb78e0029869bc058c2dad279a41e9ba8999adead09`  
		Last Modified: Fri, 21 Jun 2024 13:49:13 GMT  
		Size: 33.2 KB (33224 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:60743ee854fd42cfa8808a757b74140dc7c764defd7b657768ee00195c4b38fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189658939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd3ccf8b894e0a4e545d7c77cc708d69142600b08f59169ad19eb04d04f8fec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Tue, 23 Apr 2024 15:14:18 GMT
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
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7e8f5afb5b5470b327eda50caef29241e54c65a809eaaad3e97eb37614bf8`  
		Last Modified: Fri, 21 Jun 2024 06:33:05 GMT  
		Size: 6.7 MB (6741364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bf08af409e25ae1d28671f805e668ee534dcd9a4ec766404cf404df790907d`  
		Last Modified: Fri, 21 Jun 2024 06:33:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf08eb15a42af005ccf1d4e86a65d6c2ba15c9dd9be06366999cb3b31a4b141`  
		Last Modified: Fri, 21 Jun 2024 06:54:27 GMT  
		Size: 32.1 MB (32116928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1c0b65b2135f56b33b67cf4895a4f527c8a839576567af1a3b0d4a4243890a`  
		Last Modified: Fri, 21 Jun 2024 06:54:26 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b8f33a923aae01f1052ecea221c1feafb8adc2492fe5e49fd4e6781c19174e`  
		Last Modified: Mon, 24 Jun 2024 23:18:21 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711847abb4ddfd43328c1ad18f74f4dc670f45f4561e15762e19c56c8fe1628`  
		Last Modified: Mon, 24 Jun 2024 23:18:23 GMT  
		Size: 72.2 MB (72214837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b7446b574a5aae422805c584761a8909d4818223feabbb4fb61f1f9d31428`  
		Last Modified: Mon, 24 Jun 2024 23:18:21 GMT  
		Size: 1.1 MB (1135446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf7678310acb310e143ee3c38182c1755d3fa206b3d43b35f23f74004f12c09`  
		Last Modified: Mon, 24 Jun 2024 23:18:21 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13d402748e8e481cc72b5db6637d62c60da608041841fe5325239469e4d5727`  
		Last Modified: Mon, 24 Jun 2024 23:18:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbf41de416561941eda169b9a582a1d2fb65efc9a9ae89ec4b91b2069f760c8`  
		Last Modified: Mon, 24 Jun 2024 23:18:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c399bc8daa748a7a90c72bfb535f0defb9f0f19492928bd5ce0c8c5986ae3a38`  
		Last Modified: Mon, 24 Jun 2024 23:18:23 GMT  
		Size: 3.2 MB (3243954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd7d974b08a27c17a6ed85882aa8cbb90f68b8f7c6525112b7ac55a9d03b78b`  
		Last Modified: Mon, 24 Jun 2024 23:18:25 GMT  
		Size: 70.8 MB (70845223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcfa2a484b8d16fa3353afc9a09c763a06c39f9a5373d179014c55e0b888524`  
		Last Modified: Mon, 24 Jun 2024 23:18:23 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:03a24478307729b058fb63271ee0643646f18846f20cefe1c49d7782c4564bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 KB (42625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a8857bc79db879758091b59f81330917b1232c78f5d06eeca5a2ef3ec67e94`

```dockerfile
```

-	Layers:
	-	`sha256:c74ff622146b0614cc68efecf6b922b669ea5d0f1e24d168336e0072611f7dd1`  
		Last Modified: Mon, 24 Jun 2024 23:18:21 GMT  
		Size: 42.6 KB (42625 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.19` - linux; 386

```console
$ docker pull redmine@sha256:7e83689484f1a6d0df5c73602cfcbf601190ef60c6d9f38214007ae32df0455b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185585911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb50800408c6dfaa5b1c325c9dc4f73b0522c79f7b3a8b2462922d93ac389ca3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:fef5870f3bb90ed437c0331d7e65e52da6728b66d231aea95a605935fef056d7 in / 
# Tue, 23 Apr 2024 15:14:18 GMT
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
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:e9c6bf0d8f3154c26ee87ffe9feb02c91666069b8cbe0668cfae10922ad80c49`  
		Last Modified: Thu, 20 Jun 2024 17:39:06 GMT  
		Size: 3.3 MB (3250890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc91a9c0336bcb2c42f5feda7c10622a64c1ee93564e6ff565b7535a5fc5a22`  
		Last Modified: Thu, 20 Jun 2024 18:57:59 GMT  
		Size: 6.7 MB (6743144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc172151bb1b209eb4c27505252c51d8a3d19cb0b0fe73b8952ed8777579db58`  
		Last Modified: Thu, 20 Jun 2024 18:57:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3bc569b0d5343109e299c17b3b8862e2fa6e7b7066273582fdef7656017145`  
		Last Modified: Thu, 20 Jun 2024 18:57:59 GMT  
		Size: 28.1 MB (28050873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a3422b877146e41a3c64d4f817b8473415a5c22a6e2d2163cd2607c2e7ea34`  
		Last Modified: Thu, 20 Jun 2024 18:57:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337a67ef1b3314fcee7081a57803d72757f4c11019d9308b4c334c9cf5ce56a5`  
		Last Modified: Mon, 24 Jun 2024 23:00:20 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5666b4f1bd39a31329f3f8cb2a0b9e1857223271d9fc8374456eb5a5a6da749f`  
		Last Modified: Mon, 24 Jun 2024 23:00:21 GMT  
		Size: 72.2 MB (72214532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f522390711dde0e5e31085c2399b5f0dda260868582af9d9b46e72fe2ff9bd`  
		Last Modified: Mon, 24 Jun 2024 23:00:19 GMT  
		Size: 1.2 MB (1182154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2b4e50436140fd8697c225bc23704e5214464879273e1aee71af1d8877573f`  
		Last Modified: Mon, 24 Jun 2024 23:00:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2db5cd44a595e0bf0c000aa2f5a10837c4bfe3193d7d554038ce71c0fed1b41`  
		Last Modified: Mon, 24 Jun 2024 23:00:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93ef5cdfdbe55730d8b6d3ba041a586598a34e23e5cb68c99d6a9001095126e`  
		Last Modified: Mon, 24 Jun 2024 22:59:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d741ada5ae3f203268943b7d2257dd8e5ac1d197c812546405aa9cdd11f0616`  
		Last Modified: Mon, 24 Jun 2024 23:00:21 GMT  
		Size: 3.2 MB (3243522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f1b11ad338c2ed07eb3d7f75058e7d0cc32ca43a5eeb69e8e2e1a335240bd4`  
		Last Modified: Mon, 24 Jun 2024 23:00:23 GMT  
		Size: 70.9 MB (70896809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635e225ba184aee64aeae0a2dbe968d871a7819270095680c49ffafb2ef58ffe`  
		Last Modified: Mon, 24 Jun 2024 22:59:48 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:0b302688309e01e3020f1729637f6fb7c63073644ac91ac1bcf4c1a420678f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 KB (42136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57355229ae8d0110aaf56056cfa39d91baf13bc401efd67f63b3cbd3882333a2`

```dockerfile
```

-	Layers:
	-	`sha256:e2051cd5ea53f125e446bfd263a5b0aef40fa59f497dec64e9bcb109d6ad3b3d`  
		Last Modified: Mon, 24 Jun 2024 23:00:19 GMT  
		Size: 42.1 KB (42136 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.19` - linux; ppc64le

```console
$ docker pull redmine@sha256:fd660f89f2cee46531b4d86a1b92467c315ffb480c25ab20995973a13c0d5309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190034277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ca3675fe6ba05fe1ba7943e2fa92fbc647ae4e65234addd57009f74695685b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Tue, 23 Apr 2024 15:14:18 GMT
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
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25b5453769b463d0fcb4812822a58fd277b4faabc073c984fdf8b94f52a265e`  
		Last Modified: Fri, 21 Jun 2024 03:01:08 GMT  
		Size: 6.9 MB (6903322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee324710311e3d5326002a48755c13bbfa091dd3e550c8a9a12249036d029d1`  
		Last Modified: Fri, 21 Jun 2024 03:01:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280f8ee218b65eb8013458895487091b6897d2afaa5c5f5f0ff2ae5ff7692c54`  
		Last Modified: Fri, 21 Jun 2024 03:12:14 GMT  
		Size: 29.4 MB (29363580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c82c989ced3c7bf3075698c483ea2e021e5474865019107d169d16b02f7ef6`  
		Last Modified: Fri, 21 Jun 2024 03:12:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a41bcce81d3d1123266a9e25fe159d4db601a81e07f70fd39984fbc4eb3b8a2`  
		Last Modified: Mon, 24 Jun 2024 23:27:55 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c40fd051c860e7932e98b6276cfcc8de0b4894d799136a1f787e04e0ce94f97`  
		Last Modified: Mon, 24 Jun 2024 23:27:57 GMT  
		Size: 73.4 MB (73353922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9eab81cc85e98ae14bb60409a731ef8c82996840f6a898d91b0eca88fc64a5d`  
		Last Modified: Mon, 24 Jun 2024 23:27:55 GMT  
		Size: 1.1 MB (1123275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2f99b546dc3445aad03c69b51ace9921179cef20b41e4e662e253e63ff647f`  
		Last Modified: Mon, 24 Jun 2024 23:27:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd25eea23341e9e89c4a67c9027591be43736243fd9c2e053f423f0f410a99e`  
		Last Modified: Mon, 24 Jun 2024 23:27:56 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82ab046d9b057ef422e1ddff6df252f7c0e6fabc7ae1bccb408ca240ee531df`  
		Last Modified: Mon, 24 Jun 2024 23:27:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b8f076a4d4925cd145ca004cd8ba62a24d6efa16223f3614a0bdf499e2a26d`  
		Last Modified: Mon, 24 Jun 2024 23:27:57 GMT  
		Size: 3.2 MB (3243913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8d68d871d8c13be7f93a037b6a6674911517494a71c11da35748c17db7fc75`  
		Last Modified: Mon, 24 Jun 2024 23:28:00 GMT  
		Size: 72.7 MB (72681637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da6aa5c0fdff9d3ad62f566890af322e600d67077e8c6c3119a6ee007a9f977`  
		Last Modified: Mon, 24 Jun 2024 23:27:57 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:0565b3318e1d22850343ed7c111132bc0e78bb0d45bddfa36cfc81e5f2d3de4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 KB (42294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f55e69bd552f19e223ef9fcd9da4d3261333b18ac8625e4ad1ba87b63c6932f`

```dockerfile
```

-	Layers:
	-	`sha256:72afc7e0940a9215eca457b15f6369c835609537a7a683d63891d3669d84bc53`  
		Last Modified: Mon, 24 Jun 2024 23:27:54 GMT  
		Size: 42.3 KB (42294 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.19` - linux; s390x

```console
$ docker pull redmine@sha256:642c2d0821916c344495d89dca9d3db8a80555ae4440d20052cb0f26521af3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188457281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bc567a3123cffda15a3f3dfefa3d5242b311f975ff68ff6e332e6dde84622b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Tue, 23 Apr 2024 15:14:18 GMT
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
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db831eebad83fc6d3f6152ad3be744cba94bcac24a37b7201e28967ff9de2504`  
		Last Modified: Fri, 21 Jun 2024 05:47:21 GMT  
		Size: 7.1 MB (7051931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c4347fe91c06cf6b43b574c7ba5fe8a20134c26db4a87656d20802966fe9c5`  
		Last Modified: Fri, 21 Jun 2024 05:47:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26b6184b20af64694f644fbbe7447605f87c327c5d3cc5fd2465613e2672f38`  
		Last Modified: Fri, 21 Jun 2024 05:59:08 GMT  
		Size: 29.2 MB (29214278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5b54f72c251904caa8d161b0e29389219e07f14a993b72334c870367cf1308`  
		Last Modified: Fri, 21 Jun 2024 05:59:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce27d23e390e4caa8f0de6da219567b34893d8aaeb9da3462bfb0ef76327e9`  
		Last Modified: Mon, 24 Jun 2024 23:47:04 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baac5c97c62919430a7d723d96acb4856334d9b3426c9d8fbd4ce08630df45e2`  
		Last Modified: Mon, 24 Jun 2024 23:47:06 GMT  
		Size: 72.6 MB (72583049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9ee4a5f9db5397532e127fec8ecf5da8f048e77069e6b61f7999728f0b49da`  
		Last Modified: Mon, 24 Jun 2024 23:47:04 GMT  
		Size: 1.2 MB (1172508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827a272778ca441d68eff16f123de921feac9a26fa20c2cae635d55734de6ead`  
		Last Modified: Mon, 24 Jun 2024 23:47:04 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04d3a66c681ae45457c343154cb432fae9aeda478c0a720fedb61c4ce25b653`  
		Last Modified: Mon, 24 Jun 2024 23:47:05 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc73f8d061bff989281e58437bc8876e7b129a085389be666e0e3faf3f9ae05`  
		Last Modified: Mon, 24 Jun 2024 23:47:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746cb0c07fea4ed4cfd0b00314619c76b919b75fa3e21db5d5e108713aaf10f9`  
		Last Modified: Mon, 24 Jun 2024 23:47:05 GMT  
		Size: 3.2 MB (3244077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da052d6db934ed9296637dc536c67e13d1b71711d31cb0b16673931f82a11570`  
		Last Modified: Mon, 24 Jun 2024 23:47:07 GMT  
		Size: 71.9 MB (71934956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6060fab7894fca89d44b0fb03dbc74392ad24cc87857490cfd976ae9a32fde`  
		Last Modified: Mon, 24 Jun 2024 23:47:06 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:e9a58d9c2da52e70777e888c6a9d9ffc367470e5e36e77b93ffa8d5f0addbeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302266224bc05c03f95ebce8338fa6a0f60878c913bd5d204c33c3d7b4734fba`

```dockerfile
```

-	Layers:
	-	`sha256:7e67eba079a8cd4e53b32e573a6a06e6768074982aeed6f75042a752bd4fa59d`  
		Last Modified: Mon, 24 Jun 2024 23:47:04 GMT  
		Size: 42.2 KB (42240 bytes)  
		MIME: application/vnd.in-toto+json
