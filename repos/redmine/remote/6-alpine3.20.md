## `redmine:6-alpine3.20`

```console
$ docker pull redmine@sha256:e2157a7820796cd53f648f872b3f65565013030f8cbca8b9ed694ddf9957af11
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
$ docker pull redmine@sha256:65b60e9f3c4208fe0004ac4cf4435ea8b335a402c9b0f289cb6cf0120f4ac65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196711693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb30607cf87d3bdfb2c402c7ef00de2743c8022013fe20438c5ee8a5685b4ee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 15 Nov 2024 17:24:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
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
	-	`sha256:5697bddec4c9576e515bbdc127dda921817d9c2a291873ce9254cfbadf3b1719`  
		Last Modified: Thu, 12 Dec 2024 22:34:31 GMT  
		Size: 6.7 MB (6684086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c11fa5b923884b054e505fdb81f8c3c3d83b360f77263dd7401b993db0ae1e`  
		Last Modified: Thu, 12 Dec 2024 22:34:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a634ab18b0f786b4b4d6e00380d0f7dcadb5ec506066c343e56ebca05443b22`  
		Last Modified: Thu, 12 Dec 2024 22:34:31 GMT  
		Size: 37.5 MB (37454562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc52a171b9c23bec562a716b4cc6006b255e3fd3523af680801281dbc316b2f8`  
		Last Modified: Thu, 12 Dec 2024 22:34:31 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ff622099e0b27fd3a11d5d3b2f9df8ace3afd9b5dc4d3b02de2288701dafeb`  
		Last Modified: Thu, 12 Dec 2024 23:33:52 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f2e24e58116c6a5d708e8e3a0e75798f8dfb414746f735c8e785eb30b8b724`  
		Last Modified: Thu, 12 Dec 2024 23:33:53 GMT  
		Size: 69.0 MB (68970832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355c0aedd7aa7eb33b7a5b4f433fe917de5ead505a01ab096037e8195f5d80ac`  
		Last Modified: Thu, 12 Dec 2024 23:33:52 GMT  
		Size: 1.2 MB (1195324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bc95856a7d317fc9b68f78e9389f30a12de7c523a1c0ed3a1f9603a38567e8`  
		Last Modified: Thu, 12 Dec 2024 23:33:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712b0ef54fa78de3deca67ceb520ae9e69d2bfa4a4f17da9b315ad70a1180c93`  
		Last Modified: Thu, 12 Dec 2024 23:33:53 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ba8451d0f444d1c6769e3b6479570439d8d8b86ebb892c97e6061f505bd512`  
		Last Modified: Thu, 12 Dec 2024 23:33:53 GMT  
		Size: 5.4 MB (5357041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85144e651fd5691f49a4376517ef5c6be081058adea506a72b2910a38b712a65`  
		Last Modified: Thu, 12 Dec 2024 23:33:54 GMT  
		Size: 73.4 MB (73422466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4439fb880704ad9db07c4393b863f19564519c7e982b70c4a55fd70379822a6a`  
		Last Modified: Thu, 12 Dec 2024 23:33:53 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:9af1d64e6d051631b727593f9d352acff816ef85a4787fe8d56cc380d46aee43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95e84de35115a384c5d00c221e62011bc9e612db000dd8352da4351cd00aa44`

```dockerfile
```

-	Layers:
	-	`sha256:aaacec0686cdaf37ded3689b5378144bfba283aed8c225fe0434229d68402de2`  
		Last Modified: Thu, 12 Dec 2024 23:33:52 GMT  
		Size: 40.1 KB (40124 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:6881cc0179c005f1ea30e011321a4aa5b6f2c1f83e54b93a492cb519399ee4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.3 MB (187319191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1baa323a38bbbb494a4eecfce02c4aae64e89bbf89c08f89a2bb882f62cee3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
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
	-	`sha256:fbeb1bd04ef861b8c279cc98988255093aad6baa04de2ca17b9379c91b4e4f17`  
		Last Modified: Thu, 12 Dec 2024 22:42:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d400403c68809573f20f0a47b3ed2a393ff2751b0f77b0cf677d4261627bfaab`  
		Last Modified: Thu, 12 Dec 2024 22:47:34 GMT  
		Size: 33.7 MB (33655279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ecb354615f23e99b13e209d3c123d58d4e44716deb191291f83b6ecea50bce`  
		Last Modified: Thu, 12 Dec 2024 22:47:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0fcc68bed066aee422c82622eb85fe2cbbef75e4108132c57e5f0613abe266`  
		Last Modified: Thu, 12 Dec 2024 23:36:54 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e10cd97a5073bc435dda2f96013c29f39342e83abb48599ec17a6a0083aa55`  
		Last Modified: Thu, 12 Dec 2024 23:36:56 GMT  
		Size: 65.8 MB (65796875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c574274685a4c70c07518e7cc3e2fac3f6f7f2d564ae6c54b8979a7bb83118b`  
		Last Modified: Thu, 12 Dec 2024 23:36:54 GMT  
		Size: 1.2 MB (1162100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c9dfb805a03b56219d56eddefe4abae5e99020052f982a6886c76edba9bec1`  
		Last Modified: Thu, 12 Dec 2024 23:36:54 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe993ca3a207355dd69701e89204e66612ffb563826f748232b772889beb4b4d`  
		Last Modified: Thu, 12 Dec 2024 23:36:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5e4346d9afc63d189212a79157d1c7730c832e9e0403a6599e2d2cf939e2c5`  
		Last Modified: Tue, 17 Dec 2024 19:36:22 GMT  
		Size: 4.1 MB (4060122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84762cf0780beee7a8ab1a6f5d7f60c7735b7c8bcff2fb131d6d70b145fbef36`  
		Last Modified: Tue, 17 Dec 2024 19:36:24 GMT  
		Size: 72.7 MB (72743255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b51f06549466768829699057209dc4ca24103451efed37ae17e7c9e858b8064`  
		Last Modified: Tue, 17 Dec 2024 19:36:22 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:c4f43a09de35ea2f2626e7f28a7f504716447acc786269c76edb17bc745edb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 KB (38764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411464277c9c271780cc7176783bcc5fc309b00e8d73bf3d0da4a6ddf2dab88c`

```dockerfile
```

-	Layers:
	-	`sha256:d4c96c906944ec8af53cd822aeba1142511766e4d260f70ea22253faa0159bb7`  
		Last Modified: Tue, 17 Dec 2024 19:36:22 GMT  
		Size: 38.8 KB (38764 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:38f4545a84eaa6196e2ae610bf3f5d24553195bb74fd4c2bc3c76fda05e9d2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184074770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4522346212b83cef91351bb676bf7f58b111a37fddedaf304ce2d75700a62d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 15 Nov 2024 17:24:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
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
	-	`sha256:c365461f41c5dabf158c626b6e97c08591ab48c22d336152f8fbab5794134c11`  
		Last Modified: Fri, 06 Dec 2024 22:37:04 GMT  
		Size: 6.4 MB (6375880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1388c50ae20735a4afc3f061f18890d7ec46063937225d7a060a8dfc1f2274`  
		Last Modified: Thu, 12 Dec 2024 23:20:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba0b02a0b593bff2b609fac4a68605c3a404b7f03d54f5fa3d24d131cd44b62`  
		Last Modified: Thu, 12 Dec 2024 23:37:38 GMT  
		Size: 33.2 MB (33176769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d7f88acad662bd8c4f6ca4e497793a61a55041fb09384cb0fa74bec2bf2625`  
		Last Modified: Thu, 12 Dec 2024 23:37:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7459537a898ca39d29005f25b9fc01be62f0dc4e750d8e13e52733fb8b6601c`  
		Last Modified: Fri, 13 Dec 2024 00:53:30 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b6d8ab98ae51116079ee65027e2166d2f16ead524137d54b4a4179d8f52974`  
		Last Modified: Fri, 13 Dec 2024 00:53:32 GMT  
		Size: 63.2 MB (63191150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da72dfe3ad459002367d3c7b3be31f581c1b80cf5a9abc4455b1fff5cbdb69fa`  
		Last Modified: Fri, 13 Dec 2024 00:53:31 GMT  
		Size: 1.2 MB (1162090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11610f958325ae0b77b95786f21289fa6ec4ed6672f5aee9bc195767f2a53bdc`  
		Last Modified: Fri, 13 Dec 2024 00:53:30 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8c5d76e841de1cc90ec7527ad1d053edc7ee54277d5c062ac95b8a729cbf85`  
		Last Modified: Fri, 13 Dec 2024 00:53:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356658b6e16e4e129dcc5daf9e465ea64a3d7d6aee33f9837e80393b6ed6d752`  
		Last Modified: Fri, 13 Dec 2024 00:53:32 GMT  
		Size: 5.4 MB (5357113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73021d2d868e9afa0be87b77dd5b864cde7743d28462f7509cd22872ce7bb7c`  
		Last Modified: Fri, 13 Dec 2024 00:53:34 GMT  
		Size: 71.7 MB (71712805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15c9a36fb6a7e663f2efc7b7c1a382ec5147393c15d46302221148378855026`  
		Last Modified: Fri, 13 Dec 2024 00:53:32 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:fb261c7c6d331b32a2d13663c2e2b7b0380a4d70667885ddf6addfe8eee70d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663b9430a4d87d749222c3ffb673bb25acbd338cb8efeaa50128199af92f25d2`

```dockerfile
```

-	Layers:
	-	`sha256:7c6b1ef1877d7f6b752eeb3013b4d81220a1dd9731452b7024a3a905563e349a`  
		Last Modified: Fri, 13 Dec 2024 00:53:30 GMT  
		Size: 40.3 KB (40297 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b17e3175a799459779b7e6060785195cf65f63ab219ee1c133f7173fdb73f71a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198206718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d68dbeb5b4d8a7a73bda7618c3614da9af43866ac3701a3ede5a5bc2823e80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 15 Nov 2024 17:24:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
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
	-	`sha256:bb5537c6b035f2a2426310af3b8faf05e1cad8a072cbc9a3070280887d4de8b4`  
		Last Modified: Fri, 06 Dec 2024 22:35:34 GMT  
		Size: 6.8 MB (6750691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e577112cde8a45d3df9506d7905d60b1d1b3e44e7a54e949d5a70a9f7671b7`  
		Last Modified: Thu, 12 Dec 2024 23:14:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecdac15028f4195b4e7932836cb942b111cacb2aeb4aa78a5c9f0eb6713d4a4`  
		Last Modified: Thu, 12 Dec 2024 23:28:54 GMT  
		Size: 38.0 MB (37961712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7df0afce49cdae104794b96f6f4384c48303ea0d0a34d5f101eebe5e6dc4a90`  
		Last Modified: Thu, 12 Dec 2024 23:28:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33909746aa37357a026711632f61a0a92d7a18f6400daa0a11c580c32a117a3d`  
		Last Modified: Fri, 13 Dec 2024 00:57:30 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f4e5ffbb5410e0705aa9ed4c90dbdaa4bb3d2051abe28b5eed0e6cc288a3ea`  
		Last Modified: Fri, 13 Dec 2024 00:57:33 GMT  
		Size: 69.5 MB (69452310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18f9753a9d800f5bb7f35abbf9352b6afd72fbf6944bf3d8683205eaa5d0edf`  
		Last Modified: Fri, 13 Dec 2024 00:57:31 GMT  
		Size: 1.1 MB (1121077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258873a7461c4cf09754b3138240ba2b6b4ac95590e31edfda3f2e6fd545127d`  
		Last Modified: Fri, 13 Dec 2024 00:57:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56637a8095cfe16a3e957ab2a180afccd22f75b4e8961745463570b0faade39`  
		Last Modified: Fri, 13 Dec 2024 00:57:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0f635323ffd56127119c1684b88b47346071fecd77d0f5ba446d386ebce0c`  
		Last Modified: Fri, 13 Dec 2024 00:57:32 GMT  
		Size: 5.4 MB (5357062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f99f47d4cce675b6b73f4a1892d8dc5a35c84b5857315f40ea52c303b32fdb`  
		Last Modified: Fri, 13 Dec 2024 00:57:34 GMT  
		Size: 73.5 MB (73472663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0aa95c51ec874ce05c7d48ff9ef2054934d9b9ce2e747c9394dd2748ed16dba`  
		Last Modified: Fri, 13 Dec 2024 00:57:33 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:2011c0ca4a94635aaf57cd206284c7c13f5af6779040e0286e5f6310b390b243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0db068a5df4e0e3f8d4c129efb34d2e789810be96bc914124e2a8ebcd41bf99`

```dockerfile
```

-	Layers:
	-	`sha256:1c738ddceaf3558645ca47dc26ebb915a3bc2f707332c5915b6cde6872c3032d`  
		Last Modified: Fri, 13 Dec 2024 00:57:30 GMT  
		Size: 40.4 KB (40350 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:f4cc74d19f158ef35c44baf75fc1b21cc9cb7edee6813d2baaa0b65e458736fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192122049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf8c09b9be11fc4ee2be264996966e3d2804ac8e3dc4391b84e01e8ec5da34d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab6d339a4d1bc8ee6251faa95572792da65199bcabe2d208d77dc75430917dd`  
		Last Modified: Thu, 12 Dec 2024 22:35:22 GMT  
		Size: 6.7 MB (6749337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e8b33014daa381d404bba31cbe6b0e5bd09ac99b73750e2b873fbc2c21fafa`  
		Last Modified: Thu, 12 Dec 2024 22:35:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd1babf01a0fe36b6c5c076ac742cfc2d3f2b0c47ba2aa28f3068556cdfa44e`  
		Last Modified: Thu, 12 Dec 2024 22:35:23 GMT  
		Size: 33.5 MB (33532163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83aa52579a4fdd44a29cb70e1de09412c6aa57c53dffc33b3afa845c13bfcd2`  
		Last Modified: Thu, 12 Dec 2024 22:35:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67707e14477b4f976ddee041a65d1cdd8912b276741638a9811230182c157b21`  
		Last Modified: Tue, 17 Dec 2024 19:31:45 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69458beacffb9b1f0db9e47144c1fcebcb7593b21f23373f971d59eef4a4b17`  
		Last Modified: Tue, 17 Dec 2024 19:31:48 GMT  
		Size: 69.5 MB (69548638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce8aab49ce7780b770785312196087f1b8c0d33ebc8b7cd43a3ae73a060ae41`  
		Last Modified: Tue, 17 Dec 2024 19:31:45 GMT  
		Size: 1.2 MB (1170580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa90b6938468efd46f9fa8d941411b9f48ea6e9534bf941712eb063a2b7b15c`  
		Last Modified: Tue, 17 Dec 2024 19:31:45 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ab823e34cc71bf6f3b38b27cea32565aa7942288a8e01e85e66b0cef76e041`  
		Last Modified: Tue, 17 Dec 2024 19:31:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ddbd7bf673e2604ed9dd66ad68b8b00827c185f732ccb15e912f18a63bbedb`  
		Last Modified: Tue, 17 Dec 2024 19:31:46 GMT  
		Size: 4.1 MB (4060080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b63354635d0b7f72df182e0ad3891d83203dad865134de2d0774cd2dc3d539e`  
		Last Modified: Tue, 17 Dec 2024 19:31:48 GMT  
		Size: 73.6 MB (73588552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbd75b7134c81e1fc939bda8be505853bc6e7f0d134d9d87239e0a2ac18d1d9`  
		Last Modified: Tue, 17 Dec 2024 19:31:46 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:7a11351d5967fea2e8afdb960c9917c3794fa76b67c8cbe9f03bc8956112e4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 KB (38581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e875a4648f2bc9dd8904b8d3eb2e2ed82b6c31b14e9c5d33af815c817c293108`

```dockerfile
```

-	Layers:
	-	`sha256:09d3950cc4365c4b6bf57efb870483cd6e739263438db2bd8826ff8ce4939bad`  
		Last Modified: Tue, 17 Dec 2024 19:31:45 GMT  
		Size: 38.6 KB (38581 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:60140928f7eba33af922a57f2d76683442efbad9539ee48bb5ea238ce1501287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197888521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954213ca56a1e522e3e0a1ef0c39e883cf7cd1b35fbc56fe1228cf7597f30906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 15 Nov 2024 17:24:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
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
	-	`sha256:74b0a0af37b39f4d5d445ecdc6b2d182999eca644fc246d92bc8a0dfbb26b336`  
		Last Modified: Fri, 06 Dec 2024 22:36:08 GMT  
		Size: 6.9 MB (6911688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f4fd2674a6153c52ab87bad52d6c1faa7a4374c4703c84197b8296be3687e0`  
		Last Modified: Thu, 12 Dec 2024 23:13:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231a60e2b34673d873ae2472b24cd1a6c389732144b90dd57672fbb09f9b9bd8`  
		Last Modified: Thu, 12 Dec 2024 23:25:39 GMT  
		Size: 35.0 MB (35014775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72116fbc29191fec926411a770239928c69340b1de7e9d0e38f9b1f23576223d`  
		Last Modified: Thu, 12 Dec 2024 23:25:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e640698b37aeead23e2a874af8e40e539eb001830b4d7aa658e7bfc1fa4db21`  
		Last Modified: Fri, 13 Dec 2024 00:06:52 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c67629f335b796ac491356316f298316ad69fc2471b2827c0ebd10cbbde2a`  
		Last Modified: Fri, 13 Dec 2024 00:06:55 GMT  
		Size: 70.6 MB (70563696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2244d45183f6cf9f9f58238bb9b8620e479c37c87f6a666091a388ffa42ada`  
		Last Modified: Fri, 13 Dec 2024 00:06:53 GMT  
		Size: 1.1 MB (1111524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d1ea57708f9274f6ee2852fb3957f58bf45cdd23e700af96aa4dd38d8ded0d`  
		Last Modified: Fri, 13 Dec 2024 00:06:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807308e145e7de94694b50c5bfe113bb59ee41dfb569c352f81b83b3f0ef90d`  
		Last Modified: Fri, 13 Dec 2024 00:06:53 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b028e8541f1fc5f33861acf04f76b2d6e2f0e3658a1be75c2d60eb9fa7d161ef`  
		Last Modified: Fri, 13 Dec 2024 00:06:55 GMT  
		Size: 5.4 MB (5357140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3588ec695112d1676c638f4ecea707a1179c90cb44cca5fdb99f31e49098bc1c`  
		Last Modified: Fri, 13 Dec 2024 00:06:57 GMT  
		Size: 75.4 MB (75353753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad39b5246934173e1c9b2a104eaa6fb5f0abe81247370a15b134aa75374aeafa`  
		Last Modified: Fri, 13 Dec 2024 00:06:55 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:1fb8333704c7e415eb3f4512703964207834f67042b690d09376de8ca90d0701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75473e0ad78bbd9f4719f1bf3b422346c49d1169c11c9e37a4e470cdfc794974`

```dockerfile
```

-	Layers:
	-	`sha256:34e33c80032e63dd6da246ceda668d9bdb99a8406e549a83ce1ea43326ab688c`  
		Last Modified: Fri, 13 Dec 2024 00:06:53 GMT  
		Size: 40.2 KB (40202 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:20bb57544f0a07f3f46cb047771e6e0ab7152510884f83fa172a0e9a3f62604d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196408917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4ec8a74cb7793cb422238898fc6b4a675fb815490e6ad087286293e60cc959`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 15 Nov 2024 17:24:07 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 15 Nov 2024 17:24:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 15 Nov 2024 17:24:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 17:24:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 15 Nov 2024 17:24:07 GMT
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
	-	`sha256:f4de5e03db46d36352b57067054b4becfae3816f131583bb3208b379d75d19a5`  
		Last Modified: Fri, 13 Dec 2024 10:31:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e943f7bb5f471a262f97f3da5ea3913e81ef9399d0b049c4144f3f9cd53bfaa0`  
		Last Modified: Fri, 13 Dec 2024 13:30:53 GMT  
		Size: 33.4 MB (33433033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e099e79169776271c5499fcc38f0c79c2ae60ab0f5e3a49c6a37e37df9f067`  
		Last Modified: Fri, 13 Dec 2024 13:30:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0b8b9b565dfcab83b48e40e06dcc103579523b3059b1c5041cce07446f06a1`  
		Last Modified: Fri, 13 Dec 2024 21:13:48 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1720b9baa60949d47f4982c742423d816676ce2c73db64a04969f5e5e6b2bd15`  
		Last Modified: Fri, 13 Dec 2024 21:13:59 GMT  
		Size: 69.3 MB (69297565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210c5216b0c86bf289764c4228447bdbe7238b87a89fdf8c94f6a1d254ac873b`  
		Last Modified: Fri, 13 Dec 2024 21:13:49 GMT  
		Size: 1.2 MB (1163818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d58d09ae31fea219cff935c0012ceb5ee877ebc9049de69296d35e9918a6ffd`  
		Last Modified: Fri, 13 Dec 2024 21:13:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9dfafe26d225c94cf65d05a3252b9150fc7df49c76e4c60914b16589bb6a29`  
		Last Modified: Fri, 13 Dec 2024 21:13:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fc00c329f03ca47a8c971e6a19945ea41fe3239798d443e67f9082900efd73`  
		Last Modified: Fri, 13 Dec 2024 21:13:50 GMT  
		Size: 5.4 MB (5357102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881f1cc3818298deab54360ab25ba8ca01fb3a6d3d54a0cb5f0ecf37f621cae5`  
		Last Modified: Fri, 13 Dec 2024 21:14:01 GMT  
		Size: 76.8 MB (76835541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dec63b6b9cef289f37a8a83462fb7dfa7f83bcb12e40afca9f193e0e040fa0`  
		Last Modified: Fri, 13 Dec 2024 21:13:50 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:fac4fc9c8164b85cec897643fd19608d82fcc22532485a986b079eff0fda5770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cf952b18a639577e790cb24e1ff845df5d920bd9f97f3309030f479ecb12b3`

```dockerfile
```

-	Layers:
	-	`sha256:5229fd0ae2df4a2ca264dab1461a2e96cc915b199f09ff6aaeefbfe5ed7c3742`  
		Last Modified: Fri, 13 Dec 2024 21:13:48 GMT  
		Size: 40.2 KB (40202 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:b45714b4e3cb86d34d21b45e883df57d094a9fc7962b958a1721c3ad50be97b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195770003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f839662d0a73746941244b790922d65964a57b7bd10bc3d5468b5355340ee6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6672241fa4d39198ee64b270113855533928b42f802593a5b849cba8008704fd`  
		Last Modified: Thu, 12 Dec 2024 23:34:19 GMT  
		Size: 7.1 MB (7061692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd6c3cabafcebde40071cf05e940298c705b40e3608a7764bb8b82efe1a7c3d`  
		Last Modified: Thu, 12 Dec 2024 23:34:19 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9015800426dc919b29876608828a6cba304b7237de48bb9f9e5f3c00108d928d`  
		Last Modified: Thu, 12 Dec 2024 23:55:03 GMT  
		Size: 34.7 MB (34742716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a861fbf8860e79aba9e2c9111b9f8f8963b1647ab6333cff173433373e0338`  
		Last Modified: Thu, 12 Dec 2024 23:55:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3ebfc890fcb0939a5c909536d1b5c6b2a3ddadeb832d6351c4175dc1242e8`  
		Last Modified: Tue, 17 Dec 2024 19:43:27 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e677fbea063ef6a9b0ec93b4a3e218d6045067e0d938245fba21aedbac7925`  
		Last Modified: Tue, 17 Dec 2024 19:43:28 GMT  
		Size: 70.7 MB (70657134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28576c8508169f55d9917075ec47d754c7c5109a14ce866710efd21e00ff0c56`  
		Last Modified: Tue, 17 Dec 2024 19:43:27 GMT  
		Size: 1.2 MB (1160341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8daab3df18f2f8d82111981b9a654785d1bb374923dcc3a2daf5cacef33a318`  
		Last Modified: Tue, 17 Dec 2024 19:43:27 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6173596af698010b5e49100c54b7b0f9d4eea17a6971818f8eaccde213ec4dd8`  
		Last Modified: Tue, 17 Dec 2024 19:43:28 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fa6bcebf0eb124d6d508f5d6042bed66373fdf2babd4b55112853c9ef9ca38`  
		Last Modified: Tue, 17 Dec 2024 19:43:28 GMT  
		Size: 4.1 MB (4060073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b9b126aa60de905871e6c27026b2d711b03bec001e3374b6a179972a66be6d`  
		Last Modified: Tue, 17 Dec 2024 19:43:30 GMT  
		Size: 74.6 MB (74622960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ad2261ddc8e76fca376fca834e142795998c46ed0fe2e2b8e492c496d3c66a`  
		Last Modified: Tue, 17 Dec 2024 19:43:28 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:74d7e7cba72821c14a0ec6b1179e65b1a833497775328128ce561c546bba32db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 KB (38623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f140150290b813798edaaa30b22a6c2c8ad740a9dd91fc58e4f4699e2c03d878`

```dockerfile
```

-	Layers:
	-	`sha256:b48dd277534c40711c3a4ae168431ce1809cc2b45e3c026e351e06a0c9186a04`  
		Last Modified: Tue, 17 Dec 2024 19:43:27 GMT  
		Size: 38.6 KB (38623 bytes)  
		MIME: application/vnd.in-toto+json
