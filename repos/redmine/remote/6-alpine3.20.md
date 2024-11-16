## `redmine:6-alpine3.20`

```console
$ docker pull redmine@sha256:fa66e0569ea1288cd936b49b65c79f10698b61163528a624fbf33e72e0020106
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redmine:6-alpine3.20` - linux; amd64

```console
$ docker pull redmine@sha256:1efe6c83effcc21cd22b42677ac2326a9534a7e0627ef34e5b0c4c5b889bf091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196832231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a116420dd10d381852a36f46afb21a901472aafd567da8038314e8b543a2bfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RAILS_ENV=production
# Fri, 15 Nov 2024 17:24:07 GMT
WORKDIR /usr/src/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
ENV HOME=/home/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_VERSION=6.0.1
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.1.tar.gz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_SHA256=dcee3f15e3c15b9dbefba1fa9d8dfa12e89a7d40b3f3ed82da903d80d2548030
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 15 Nov 2024 17:24:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 15 Nov 2024 17:24:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c5a8736043f8d86d5255a3a9eceeeb403a1d5104e00e1f165bf0ffd468e8bb`  
		Last Modified: Tue, 12 Nov 2024 02:50:51 GMT  
		Size: 6.7 MB (6684082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3088a8390a746d5a7a82f355f5332f0c2e0534f7e2a7f6ba00082b63b50144`  
		Last Modified: Tue, 12 Nov 2024 02:50:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3265fd5b7fd95868d7acca175bd2cc99ccd961fb699928c5dceac498f0528b`  
		Last Modified: Tue, 12 Nov 2024 02:50:51 GMT  
		Size: 37.5 MB (37454335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e095f7ca6ffc6054fda50ae023096e0d09b3dbf96df9e99fc57666a76133d0cb`  
		Last Modified: Tue, 12 Nov 2024 02:50:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51962bea5997bbfd1d8ccd176be34c058db741f7f86fc743bbceb9462a74b488`  
		Last Modified: Sat, 16 Nov 2024 02:11:43 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6508882cbb481475ce8b32bfc9cc7a4ae6cc70d07321eed7d7b34a848ae0a6`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 69.1 MB (69126779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8965d45fb0e39b582782a69289cc24e8370526d3ed89506518433a4bf75db996`  
		Last Modified: Sat, 16 Nov 2024 02:11:43 GMT  
		Size: 1.2 MB (1195319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e77edc5097fc6fca68467ca31ff07c1ca7a174e81e2001b81e1e81e5350877`  
		Last Modified: Sat, 16 Nov 2024 02:11:43 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02889c03ecd363d06ffa5147f5d5b40ab1a1f17d0448560c7d5376c7e8a4ef94`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1a893abcf57b254c776d6c20de6f8f224d025c2e41b973c4b7df024970a9e6`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 5.4 MB (5357028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e3f646b5234c0069b1cdbf160a002acec681d394a460e0ae6d3e758fe60158`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 73.4 MB (73387300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33982d2c7320f9f56d8c0978b3c987ee290b0d3987859e750b88fe3adcd632a1`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:a356c0174753e8bb95fcd1525d1e240bfcf93161603753d00d601cefbf274730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fdf8ae4de540868cb9b61e291d84bbc529296966b39a19d491af7e16c00c7c`

```dockerfile
```

-	Layers:
	-	`sha256:f37e77ffd90a9933699147298e09ff1d4072a3c6aa171c5a8c46fcc0f488ad44`  
		Last Modified: Sat, 16 Nov 2024 02:11:43 GMT  
		Size: 40.1 KB (40124 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:befcb32fc4a13b64dec3ff7ff9f0368df538784876eff80dbb5a6efe1f7e94f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188531420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb11b7a09d0a907b8a0bb41258177e57cebfba3d49fc4a7c0673cf2dcad00d75`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RAILS_ENV=production
# Fri, 15 Nov 2024 17:24:07 GMT
WORKDIR /usr/src/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
ENV HOME=/home/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_VERSION=6.0.1
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.1.tar.gz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_SHA256=dcee3f15e3c15b9dbefba1fa9d8dfa12e89a7d40b3f3ed82da903d80d2548030
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 15 Nov 2024 17:24:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 15 Nov 2024 17:24:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e74324e51ce19a75da9165a75626c579a3efec23f5b36ebba466c3ed3af76`  
		Last Modified: Tue, 12 Nov 2024 15:07:33 GMT  
		Size: 6.5 MB (6531476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c239d6b8daf0f8121638fdd8bdc13bc144408d8b544581018f24d277269ded`  
		Last Modified: Tue, 12 Nov 2024 15:07:32 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040da31c96ff137564648cab0afdf54ba4d9934e38d299bec7bc608183e11d73`  
		Last Modified: Tue, 12 Nov 2024 15:14:48 GMT  
		Size: 33.5 MB (33481904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a57b3d31315d88e5a78c61b13e3b6ef6017cf8ce1d28c2e9da823dd44616d0`  
		Last Modified: Tue, 12 Nov 2024 15:14:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595c0ed16dec17ff982627f3d9b4e5003fdc4a5e047937316e2c047a22b13bad`  
		Last Modified: Sat, 16 Nov 2024 02:16:55 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9680f22a9130a958657c2a6bc582dbfcec9701ac306f62309e028f330cb990a1`  
		Last Modified: Sat, 16 Nov 2024 02:16:58 GMT  
		Size: 65.9 MB (65941955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991454ca2a868c1bed135f31eb835ebb05fbf219dd1fb52c3c77d8605f6ec33c`  
		Last Modified: Sat, 16 Nov 2024 02:16:56 GMT  
		Size: 1.2 MB (1162097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1790208c7cadeff794eab004a2ac17454ed9af6cdafbd37f9e217955d06d6be1`  
		Last Modified: Sat, 16 Nov 2024 02:16:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c096a5110c4047c924dfb67987546d49b45b6ac30c6572a0c48e923036e675f8`  
		Last Modified: Sat, 16 Nov 2024 02:16:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d521c50f68c96c85a1c3ffd4063501b27c207ff4184def2bef72f278e493abf2`  
		Last Modified: Sat, 16 Nov 2024 02:16:58 GMT  
		Size: 5.4 MB (5357105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80c72f403190b523751280ebf1fc4ec888a06a07925d8e243d980dedf17b14`  
		Last Modified: Sat, 16 Nov 2024 02:16:59 GMT  
		Size: 72.7 MB (72686795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b066ad4d1525120055083897d0bf0d19eb2179ff01e36de288edbf72e3ac72`  
		Last Modified: Sat, 16 Nov 2024 02:16:57 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:119a35de98e02cfded9e695cce811e0fc61aace94d31fa72fb9789253752bae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5388d7bcea8f3ef72fd835a0f6e11b3a02cac2ac541ae196a186406bb705ed`

```dockerfile
```

-	Layers:
	-	`sha256:b15a26f8011586e80f82ad3a0883c7deeec1f55ac4cc543b0a44a324b419514b`  
		Last Modified: Sat, 16 Nov 2024 02:16:55 GMT  
		Size: 40.3 KB (40297 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:561545b1cf09ade1e86301303f24ea94aaf7130195a7f48ac6411f5a79df097a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.0 MB (184012811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c01faba624eb2013a2fcce515c004a0514d987cf87a22d8fbe3305a220efd21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RAILS_ENV=production
# Fri, 15 Nov 2024 17:24:07 GMT
WORKDIR /usr/src/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
ENV HOME=/home/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_VERSION=6.0.1
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.1.tar.gz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_SHA256=dcee3f15e3c15b9dbefba1fa9d8dfa12e89a7d40b3f3ed82da903d80d2548030
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 15 Nov 2024 17:24:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 15 Nov 2024 17:24:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c198b2a44d959ce599e9d13f63182f1af9d83a1da7969e6a07c1e6fec36024`  
		Last Modified: Wed, 13 Nov 2024 06:10:56 GMT  
		Size: 6.4 MB (6375777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac846abd9ce06960ddfb86ef68aad526544ff79feed0ec4bc6cc948085c35832`  
		Last Modified: Wed, 13 Nov 2024 06:10:55 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd049fb09b21b1990a751142be15258ce2cbdb9ea73315fe5f7f84767a5988a`  
		Last Modified: Wed, 13 Nov 2024 06:21:32 GMT  
		Size: 33.2 MB (33176676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f89090a722fcfa055145ecd7ab2a74e55ae819a818402a3166fc7cdf463c14a`  
		Last Modified: Wed, 13 Nov 2024 06:21:31 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b74f60961128e80056eb661dfa4b0b5ef6434f746c753db4e95df3f08fbac3`  
		Last Modified: Sat, 16 Nov 2024 02:22:06 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce50f71beecd462857b916e9fd6a6f7cc391021ac30bad9809f620f9c3ad86`  
		Last Modified: Sat, 16 Nov 2024 02:22:08 GMT  
		Size: 63.2 MB (63169745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead6ca2f6d0b436902adacf7713ab13a83ac9bf06d4b61cbe4eeb20d0e22701`  
		Last Modified: Sat, 16 Nov 2024 02:22:06 GMT  
		Size: 1.2 MB (1162098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c6d1e8e4099248a3e22a6c6634ddd7cd52376e976744ab58f21445cbe94e1a`  
		Last Modified: Sat, 16 Nov 2024 02:22:06 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052913d8e12f6fdeaed4288054ff3b825b1bb5f8481f82599f0e03ff154a41f8`  
		Last Modified: Sat, 16 Nov 2024 02:22:07 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0875f6208178eef0125966769accc0e262c9ed155e8b9adfeb454c7feff66107`  
		Last Modified: Sat, 16 Nov 2024 02:22:08 GMT  
		Size: 5.4 MB (5357058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98874daac82807e09fbbc72ad6554b8f8028e7b83371615fe92e3f8318cbcc5`  
		Last Modified: Sat, 16 Nov 2024 02:22:10 GMT  
		Size: 71.7 MB (71672488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd811a15e4261e4e36e775f5c11369bb8955ed40797df1e6187c0afbfb1dd7f`  
		Last Modified: Sat, 16 Nov 2024 02:22:08 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:8ee27db34c62335514d201731753766ce0f9238d48d3485999f82c8fd842b84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d6582788d44911520d2f75b63cefb769a58ed927fe0423671696112a8dc64a`

```dockerfile
```

-	Layers:
	-	`sha256:0bc5ce864a7ff6701c981eefa8e8af0e76f2d33261dc297a9ed3e73344086e1f`  
		Last Modified: Sat, 16 Nov 2024 02:22:06 GMT  
		Size: 40.3 KB (40297 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:987255acac5f693bce16c0aeaa39c5fd78c50c3b924105ced10c548a8fb36c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198344681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51645ec6137caa8c6a720c9b6d6e20f872f217af80adb78d4ddffad610b0d4a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RAILS_ENV=production
# Fri, 15 Nov 2024 17:24:07 GMT
WORKDIR /usr/src/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
ENV HOME=/home/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_VERSION=6.0.1
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.1.tar.gz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_SHA256=dcee3f15e3c15b9dbefba1fa9d8dfa12e89a7d40b3f3ed82da903d80d2548030
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 15 Nov 2024 17:24:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 15 Nov 2024 17:24:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786b223eb281a04bbf0c1fead8ad47010a09c4f7988fa0a3fc674e521e9f094`  
		Last Modified: Wed, 13 Nov 2024 00:00:45 GMT  
		Size: 6.8 MB (6750669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004be50b369a396f6f477b6b7b56b8a67d5d4ca04bae891b5f358f12999583ce`  
		Last Modified: Wed, 13 Nov 2024 00:00:45 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3866e93a21229d1a8429ecc4bc78ac8c0ad8195e7eeb0fedd03dfb54466353e`  
		Last Modified: Wed, 13 Nov 2024 00:11:39 GMT  
		Size: 38.0 MB (37961643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5fbb38ac9d2d3b5a604fad57f0d2c37c29ba7da439edec80c1c1ad2e0007a5`  
		Last Modified: Wed, 13 Nov 2024 00:11:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb50b1f03d6c5724024c0f7ec4478ef9284ca24920837d988af324f270859e9`  
		Last Modified: Sat, 16 Nov 2024 03:01:03 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f50d7ea57abdfadc94ae6e2685f70fb729aa4ef5cc4cd16f0000275cc34a058`  
		Last Modified: Sat, 16 Nov 2024 03:01:05 GMT  
		Size: 69.6 MB (69624035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554eba07cde29019d4a4df1f812fa37eafac49431002adc7fdc0056a36b2084a`  
		Last Modified: Sat, 16 Nov 2024 03:01:03 GMT  
		Size: 1.1 MB (1121083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae1dca19674affc51069b2b67ea0a5174af9cd3081df47c63969a6bc35639e5`  
		Last Modified: Sat, 16 Nov 2024 03:01:03 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36e56c557658b909a54ca1a017759b0d1f0f035795f6b39ec98e481b16e2b74`  
		Last Modified: Sat, 16 Nov 2024 03:01:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b69e32b6dd34b8cf82805ca7988c026f0052313f23c7be3669e408dd98541fa`  
		Last Modified: Sat, 16 Nov 2024 03:01:04 GMT  
		Size: 5.4 MB (5356894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d838224beea5fb69d83745d67e533b95950b52941b0634cfacfe4bc11b731ed7`  
		Last Modified: Sat, 16 Nov 2024 03:01:07 GMT  
		Size: 73.4 MB (73439144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5d946b71a6fb0b03e8e7a0a5d608da3caa3f4e554daf0c72607f113b4084e1`  
		Last Modified: Sat, 16 Nov 2024 03:01:05 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:21ed4b5bf5c5514882d1a0a757773dcc0b5a4629afef80619d9edc86612846cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c92fc8f69a15a0eac3fb030d3566ca47c902d3ced5b935d8fe9e683582e44c`

```dockerfile
```

-	Layers:
	-	`sha256:626727828caa69cb8ae37534f8eb228abaf0d4cc72a984366e944334023c8a3e`  
		Last Modified: Sat, 16 Nov 2024 03:01:03 GMT  
		Size: 40.4 KB (40351 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:1d2206c32a08ba39ea39b924d79c77564a9152d3c739449a3c91f10789c5d5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193528622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90a2fa920cbf603924bd50f3bf78f2f6246b32f5d3cf8fe67999abc93c3f1fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RAILS_ENV=production
# Fri, 15 Nov 2024 17:24:07 GMT
WORKDIR /usr/src/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
ENV HOME=/home/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_VERSION=6.0.1
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.1.tar.gz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_SHA256=dcee3f15e3c15b9dbefba1fa9d8dfa12e89a7d40b3f3ed82da903d80d2548030
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 15 Nov 2024 17:24:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 15 Nov 2024 17:24:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa9a49a5f89c4c0e8403d5095c8c6e4e2f03fac865bf7fb01f1be7b82b0e7f9`  
		Last Modified: Tue, 12 Nov 2024 02:50:36 GMT  
		Size: 6.7 MB (6749332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870e016f29b3d9c95f54321277437f726c76e36370ccfd2c82e90b877f524bcd`  
		Last Modified: Tue, 12 Nov 2024 02:50:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc44221b896c55091db90a82ea7c06b6783de4b0c9a8b193bb9c82e86e6124e8`  
		Last Modified: Tue, 12 Nov 2024 02:50:37 GMT  
		Size: 33.5 MB (33531964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c74e2b5ee6b96803125cca6d7bc78ed44ad4e9531412562f67247a43c70076`  
		Last Modified: Tue, 12 Nov 2024 02:50:35 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ba08f6b17cb8b0478e9f8575f9982fe8b5ce4cf40bfc7269f212863fd18e8a`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514de40171ed708ae5d78f80ddc1c352454805543694ba773382d27cf39c5942`  
		Last Modified: Sat, 16 Nov 2024 02:11:46 GMT  
		Size: 69.7 MB (69708252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcb5147b941bc991b23783572f93670eea58922dcfba63bb3cffb3f79561b4f`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 1.2 MB (1170570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb18a2e7c1aee5de692cbb18299573717a06a176e7c337aac04898d4116c70`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae31e34cbff5ed257ff05cf9cd134ec58abe9b7ba83994ac442cd97bc6f7c72`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61094e4de03a2a39441e83fe6e1a92f11111a8897366e1f301be1727ff0dbaa`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 5.4 MB (5357077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b36bfff503baf518c7e02270864922e2a794ee2a688b60c9a40e239db4595bc`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 73.5 MB (73538720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4a110164f6f26a85235fa31e8157575877da19f3dcb490c587719277ee2c24`  
		Last Modified: Sat, 16 Nov 2024 02:10:57 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:a2a3760c270f4992b1dceb35fdab34908c2e8158b6cc84cd29790610e1d1e594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d1f32b3feaf774dd8d17abe7a24dab721f8dd151df3c2196afe238c7ae29ce`

```dockerfile
```

-	Layers:
	-	`sha256:88fe8ef1a2e6a2bfdd60ff468814c64f2590f93b6e847f42003ec8cbc3133471`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 40.1 KB (40061 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:068d93fe9a6aae8d8c4235a0ecb8670bf74e6ab1010e98db1730cfc380a0bad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (198035447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b61ae806714c85054a65c25e3a8efadfde4c93ce39d5917aa949b29b4e7881`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RAILS_ENV=production
# Fri, 15 Nov 2024 17:24:07 GMT
WORKDIR /usr/src/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
ENV HOME=/home/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_VERSION=6.0.1
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.1.tar.gz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_SHA256=dcee3f15e3c15b9dbefba1fa9d8dfa12e89a7d40b3f3ed82da903d80d2548030
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 15 Nov 2024 17:24:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 15 Nov 2024 17:24:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a072d5592b3b588e99a3a052ff5ee414af9c1d636e408faa116c12d7fd46fc2a`  
		Last Modified: Tue, 12 Nov 2024 14:13:39 GMT  
		Size: 6.9 MB (6911689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34dd9d8cfa8476d8db9162f8984d90bef8d472c30fe399e84428e60c16cdab5`  
		Last Modified: Tue, 12 Nov 2024 14:13:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25640d0d72651c2a527b339197f330f67821819d10116f5e564594e1f26708b9`  
		Last Modified: Tue, 12 Nov 2024 14:23:26 GMT  
		Size: 35.0 MB (35014771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab5772b32d769c43dfcd035ab309e4591fddd5d59d67605ff7707bd8c8d3eb9`  
		Last Modified: Tue, 12 Nov 2024 14:23:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370fc700d56b2d07871368933318c770530f7114a70f1fce9c37477c2741430d`  
		Last Modified: Sat, 16 Nov 2024 02:43:53 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ab262e24b5a056e8ad2aec51c541f6b1cde835ae4a6b7c5799e3cc9a299dd9`  
		Last Modified: Sat, 16 Nov 2024 02:43:56 GMT  
		Size: 70.7 MB (70741075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3082b05437e4b4d5d365eff3284c736f9dce7ac906b028032d70959628441d`  
		Last Modified: Sat, 16 Nov 2024 02:43:54 GMT  
		Size: 1.1 MB (1111529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e3e97efa6896656ba6e73504496ac3a5605967cf6dbcac8af669590ea62089`  
		Last Modified: Sat, 16 Nov 2024 02:43:53 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d9e0790b8ce1c7ff3994e65ca85fa7ee445b4dc2ee067561e9a339b0f09931`  
		Last Modified: Sat, 16 Nov 2024 02:43:54 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0417904c12fbb6c33b5373dc7f75ce97c5ac7f6c1fe878f9d5e8a4bdd5012f`  
		Last Modified: Sat, 16 Nov 2024 02:43:55 GMT  
		Size: 5.4 MB (5357085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a859b78d775ab0ac06448f9823679d455a3e22e4bfbe8fc7f0af502ef7e8cfd`  
		Last Modified: Sat, 16 Nov 2024 02:43:57 GMT  
		Size: 75.3 MB (75323350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd25e15adeafc0b75871b8b167efba5b3b35c76944976105404669d395ebe03b`  
		Last Modified: Sat, 16 Nov 2024 02:43:55 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:f17fd84f76de451250da094ca9e69739f60acb9bb996f5581916029d02119c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129116173c0fb8b054e14f8c587d71d6c9b816809cabebab55a3bb6e672cd89e`

```dockerfile
```

-	Layers:
	-	`sha256:20b9abbe49183a1216e74422ea80a74fd6a1c2d9a5cfacbffac6cab79670259e`  
		Last Modified: Sat, 16 Nov 2024 02:43:53 GMT  
		Size: 40.2 KB (40202 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:f08b84b048b81964de630109ce260e38a0b8f5481aa2c76ede1ede753616d4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196150642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3465385892adfa0cf048dfec82cbd4951e73e59103f9504f98fe048df507b19c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RAILS_ENV=production
# Fri, 15 Nov 2024 17:24:07 GMT
WORKDIR /usr/src/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
ENV HOME=/home/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_VERSION=6.0.1
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.1.tar.gz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_SHA256=dcee3f15e3c15b9dbefba1fa9d8dfa12e89a7d40b3f3ed82da903d80d2548030
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 15 Nov 2024 17:24:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 15 Nov 2024 17:24:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1fa0dd9a03ad255ee7ba0764f0e4efb1e4a3f6a15da7560e4ed54bd358cc22`  
		Last Modified: Wed, 13 Nov 2024 08:12:38 GMT  
		Size: 6.9 MB (6946894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2fde1b135368546b5feb8d1ca57e81ccc540e3c449d44d3b92d84a7ab4948f`  
		Last Modified: Wed, 13 Nov 2024 08:12:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11eb704522fb73cabac960902f1fc286549989a597870ac18ba9563849759636`  
		Last Modified: Wed, 13 Nov 2024 09:39:06 GMT  
		Size: 33.3 MB (33250003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df052bad82674168c8f468393b0e6a8de1f93bb9fcef36d6a443205975ad92fb`  
		Last Modified: Wed, 13 Nov 2024 09:39:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405bd4e6df9c7ca04996bb705c63b6fd85aad7de01d98708c0f0bb70a649d642`  
		Last Modified: Sat, 16 Nov 2024 04:26:11 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81adfac57a8d89bc70f90af3966b5eeaaabbf78bd278869c4f7620ea90baf11c`  
		Last Modified: Sat, 16 Nov 2024 04:26:22 GMT  
		Size: 69.3 MB (69274905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedc0b61381654223eb92f2779de8d69c59c4e142f33bc5c950870e3c566974`  
		Last Modified: Sat, 16 Nov 2024 04:26:12 GMT  
		Size: 1.2 MB (1163814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35973493a0a64bed19857bcd9a1c084392563cadb8db8a2134bbaf568027ec67`  
		Last Modified: Sat, 16 Nov 2024 04:26:12 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614bde1b091eb97d1613ba9d6067e5af0fa81112f35afe5132dff71a134ed232`  
		Last Modified: Sat, 16 Nov 2024 04:26:12 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd229c3deb9495b1adde5ffdcc64a94fbccf7e6992b386b6ec06c2e2fd47349e`  
		Last Modified: Sat, 16 Nov 2024 04:26:14 GMT  
		Size: 5.4 MB (5357091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455f0ff9b6988d34bb9a2698f4874ecd0221dd5ed996a3cf55a7295b19080552`  
		Last Modified: Sat, 16 Nov 2024 04:26:25 GMT  
		Size: 76.8 MB (76782963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181cee57038de93b8bc54be43f351ae3f72b885246afa0d91c3cd5e7d6f77ca2`  
		Last Modified: Sat, 16 Nov 2024 04:26:13 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:0ea46b08aa9b24e1caed79818a99456ded93a879fbe62977a35ae85b0b1daaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc8ce95b57fca4a56d5bd51c8b59709c35eb1513fe258d7be487e3be2c9910`

```dockerfile
```

-	Layers:
	-	`sha256:07e034142361001c6c3482adc858b909c985991152ff9fb676baa6b0348f3924`  
		Last Modified: Sat, 16 Nov 2024 04:26:11 GMT  
		Size: 40.2 KB (40202 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:01b40eb939511a7a8539f2821270a91c8571eea04b54d33d49d9c5367feac5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 MB (197183559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f91012f21555a7527d9a0b0795796650608a1512da315b6cdde1d89adef7154`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GOSU_VERSION=1.17
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RAILS_ENV=production
# Fri, 15 Nov 2024 17:24:07 GMT
WORKDIR /usr/src/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
ENV HOME=/home/redmine
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_VERSION=6.0.1
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.1.tar.gz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV REDMINE_DOWNLOAD_SHA256=dcee3f15e3c15b9dbefba1fa9d8dfa12e89a7d40b3f3ed82da903d80d2548030
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 15 Nov 2024 17:24:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 15 Nov 2024 17:24:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f066a3ee687f4e302993aff72d7f4bb4bf4e87a2a5ad0e3ba073da627d993c5e`  
		Last Modified: Tue, 12 Nov 2024 21:37:18 GMT  
		Size: 7.1 MB (7061713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d515556de7496906ba5acdbc93988aa16ec53873197d71dcf8469a671fa7c84`  
		Last Modified: Tue, 12 Nov 2024 21:37:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafe8a39618de8b0781b21277dca58a3ad1e339e72e59ee3faf745bffd6a4881`  
		Last Modified: Tue, 12 Nov 2024 21:47:15 GMT  
		Size: 34.7 MB (34743051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b3d98a1b43d11a9888565f2e5e0e89cc2f66d28734f8984ce8b2359195ac30`  
		Last Modified: Tue, 12 Nov 2024 21:47:14 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec275c4cfeba40803e77404fe7d16a198515f02542b4ce2d16f1e193f8fad26`  
		Last Modified: Sat, 16 Nov 2024 02:37:45 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08264cae31fcd77674a8880632eeaf2aed1ca25bc1e1a923b2c22d4939fbbc9`  
		Last Modified: Sat, 16 Nov 2024 02:37:47 GMT  
		Size: 70.8 MB (70835814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15562bad844789b67e467c168b8dd6afa3a73b040ade7304fa2a0babcfb8de8c`  
		Last Modified: Sat, 16 Nov 2024 02:37:45 GMT  
		Size: 1.2 MB (1160348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3c57b0c5f61b3d28fa4c191ee690e2db61e83b0d1bd55bb82a742bfe709c71`  
		Last Modified: Sat, 16 Nov 2024 02:37:45 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d06602d1fd3f15c4c54ad00c8555512f3b8a8cdef40b39873c469867a3ff92`  
		Last Modified: Sat, 16 Nov 2024 02:37:46 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7e0931058c3185c03d1ef47eef627da91bd45e4604cc66f293f92c1410613`  
		Last Modified: Sat, 16 Nov 2024 02:37:47 GMT  
		Size: 5.4 MB (5357051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75060a3f9ab09fabbb80f79d6aecee7960f1c70bb27cc32a274e4e47806aa73`  
		Last Modified: Sat, 16 Nov 2024 02:37:48 GMT  
		Size: 74.6 MB (74560483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8506a329847d87b8d8c810e60d26965523f1fda20ac90bb531273349e55094`  
		Last Modified: Sat, 16 Nov 2024 02:37:47 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:05484ec972bac17565337d38ac7f47f16f789e6fa65f01ad6d749831289967db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294f36e250e7546e7a79720a0c6b8662de314a858bffa18c568c7a720e712695`

```dockerfile
```

-	Layers:
	-	`sha256:37ee02e0eaccbcf851a9c7e9519a0ed1d6d959ce3fc8810433154cdcef3ed762`  
		Last Modified: Sat, 16 Nov 2024 02:37:45 GMT  
		Size: 40.1 KB (40124 bytes)  
		MIME: application/vnd.in-toto+json
