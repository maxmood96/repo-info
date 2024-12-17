## `redmine:alpine`

```console
$ docker pull redmine@sha256:16e3142eb0fba3c586bde4d701f7080420d705e30dc00dd481ab561c4d6d3d71
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

### `redmine:alpine` - linux; amd64

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

### `redmine:alpine` - unknown; unknown

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

### `redmine:alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:21b29200d4348e2e35fbc0fe4f6ff7e54bdf54db75d22ecb02d8ba3590e71b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187189881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d09e1eebcb25dc37ff5d3da93437fc5a0f64bf533f32da5ab823f257484a21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b12c95f1fe69503a4e99b4118a13b41c40d0844feba72e2e756a769be5fa7`  
		Last Modified: Fri, 06 Dec 2024 22:32:43 GMT  
		Size: 6.6 MB (6568172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ca0d2bb66a7dcb23798d7aa23885d8544420f7868a1046f3f039325e9bbe07`  
		Last Modified: Thu, 12 Dec 2024 22:38:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28fbdf9c6aa2e61e0897f6e09a3031cdb361ef949585d6c88a24b70b8a158ed`  
		Last Modified: Thu, 12 Dec 2024 22:44:55 GMT  
		Size: 31.7 MB (31650253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146965d9a90634afaf43d0565f581b102ca823703f2fa923b13457eb5d2344df`  
		Last Modified: Thu, 12 Dec 2024 22:44:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f93bcffef1883776512b92ec0d9aa35cd0aed667adbdc270ca6b6db7ec78dc`  
		Last Modified: Tue, 17 Dec 2024 19:33:18 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b848a75706a564e2ccad56d6bea490d7685338f1c4035c7ad59bdd0fdef157`  
		Last Modified: Tue, 17 Dec 2024 19:33:21 GMT  
		Size: 67.5 MB (67538734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb90b9b5a989095877430e41df0c44566df1711d21edd044be7f6dd14a6c724`  
		Last Modified: Tue, 17 Dec 2024 19:33:19 GMT  
		Size: 1.2 MB (1163952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27f2fd2046c32b1e49005e63663b828237f9e3b4cdf1b649952fa87962fa631`  
		Last Modified: Tue, 17 Dec 2024 19:33:18 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99af07b0a9b9d0ac496ca86e17a3e8c818a0abb2d514c3c4486d24464688200`  
		Last Modified: Tue, 17 Dec 2024 19:33:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87165ebe5acf2b94804f9d8b11b8a07d984363ed47f36d2c04454055fd7a1a`  
		Last Modified: Tue, 17 Dec 2024 19:33:20 GMT  
		Size: 4.1 MB (4060010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908fe8a7424785facf4af80e927a3ae69a318665e321bd041862b0db4e4da5ad`  
		Last Modified: Tue, 17 Dec 2024 19:33:22 GMT  
		Size: 72.8 MB (72838096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3e4256a8c59f5ad109e9af8a6de358ea9e4d75ba6eccde0b3f521782e8a7ae`  
		Last Modified: Tue, 17 Dec 2024 19:33:20 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:b43f41be95c7e193819351ac0ae4edf7f54f05a5484a491855c24f5fb70a2c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 KB (40019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e31fa6d029344795574dc260f1cf0eee2af296876f971b0547883bc422156e`

```dockerfile
```

-	Layers:
	-	`sha256:2569f7e2e53dc45cea1597c0ad71bf33a0ee5a94af91c22bc50ca065f0b0c376`  
		Last Modified: Tue, 17 Dec 2024 19:33:18 GMT  
		Size: 40.0 KB (40019 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0cc3e7ebe995049ec2a2e0fcdf9bdabd0c63e725977081bccb5986ebb2eb853a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182950213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774d153e2b780cd55a5c717376eca097c831db63821663fd48608917df198ed7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b26c224a9a1e46e5dfbc9bf70fcad8ef517f0a3c0bcf4815427a79622b385a`  
		Last Modified: Fri, 06 Dec 2024 22:33:32 GMT  
		Size: 6.4 MB (6408987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a6cefa53cbec58b80f6c0754a11c80ccf91e1b3e090d1a5b9687f91648e830`  
		Last Modified: Thu, 12 Dec 2024 23:18:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6742d287c1a9e78818a2f19114c275f2f291c53d2619718d204bc00654b73b`  
		Last Modified: Thu, 12 Dec 2024 23:34:55 GMT  
		Size: 31.5 MB (31525888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65b2ba08c050532c36ea0ac8412fc9e901682c3e94197cf36e9bae610e21570`  
		Last Modified: Thu, 12 Dec 2024 23:34:54 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e154a9023fe1bf24c0e94c182ac41e8ea9628a58dc1dbca6a11eb0628bccd2c3`  
		Last Modified: Tue, 17 Dec 2024 19:33:37 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729e5b90fbba5d5a7712202ceb1d75da233d47ee2646c777d69cd27d883b2e41`  
		Last Modified: Tue, 17 Dec 2024 19:33:40 GMT  
		Size: 64.8 MB (64811929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351c45224a6c811f4ede354b6f1d7afe00f2fe4b28017330b50d1a1557dbcdf0`  
		Last Modified: Tue, 17 Dec 2024 19:33:38 GMT  
		Size: 1.2 MB (1163943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57b98c55cc7049a185adaa01b5994b24bdd0862dc62586e8c03a1bce0961a6`  
		Last Modified: Tue, 17 Dec 2024 19:33:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd29aebab722e3ec2cfc84eea78742d5042d813503a2de143c43879a0bd394e`  
		Last Modified: Tue, 17 Dec 2024 19:33:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9078f00ae5b3f811a1b13912e1f85357df02f95314ed01a142e8b472d2446f3b`  
		Last Modified: Tue, 17 Dec 2024 19:33:39 GMT  
		Size: 4.1 MB (4060059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e71408023952be303785361ba982ea17efec05601afba3136fa8eb427a664ce`  
		Last Modified: Tue, 17 Dec 2024 19:33:41 GMT  
		Size: 71.9 MB (71875889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd6828717b890135b960dbc311b5d8bebb448e25127b6fe80761a2f120232ec`  
		Last Modified: Tue, 17 Dec 2024 19:33:39 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:ffc354f8764ae60686af278a51c70b6ed97a53d8a84bbb34a58c5d32a3e642ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 KB (40020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc2cb41733280d00ce2d2322c376b312246160efbad34cf9c3cf81c1be3115e`

```dockerfile
```

-	Layers:
	-	`sha256:b57dd1a4a46279efd8ddf5f901e4e96a6fe617e705098a9d698f92f4d1a7e152`  
		Last Modified: Tue, 17 Dec 2024 19:33:37 GMT  
		Size: 40.0 KB (40020 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm64 variant v8

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

### `redmine:alpine` - unknown; unknown

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

### `redmine:alpine` - linux; 386

```console
$ docker pull redmine@sha256:d9e63ab36345443d0f67d4d004d329769adbfc95ab28b724d490ba31d75a49c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192144416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79066c17102df207897d004b5c7803626b19aee82377f1e41f146c3c117a6fd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af60f1cb4b6e732678c8e027d3afaabf456155c5d2d5a048b9a09304e7d1e86`  
		Last Modified: Thu, 12 Dec 2024 22:35:10 GMT  
		Size: 6.8 MB (6812912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f60202703919e30a94e46eb9cb4f21679f8d43abbe0596a5b4d33746b1db126`  
		Last Modified: Thu, 12 Dec 2024 22:35:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2a005e9537ea77476d4b2c7990047c1b16d0a35fc3ad873c344d51ceea63a4`  
		Last Modified: Thu, 12 Dec 2024 22:35:10 GMT  
		Size: 31.5 MB (31538629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73a5ec640647400802816d4431860654755e23303318d2d744c777c7afcc133`  
		Last Modified: Thu, 12 Dec 2024 22:35:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6a49a9e65fc4454394b169314cddc6984dafee006a391048acbe4765848570`  
		Last Modified: Tue, 17 Dec 2024 19:32:12 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca77436e4c40daed2457195f63c7f502f3b2811b4d07e153e41f8298d03f9de`  
		Last Modified: Tue, 17 Dec 2024 19:32:15 GMT  
		Size: 71.3 MB (71328942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b06e2a6c5e903083d6efb91f3b1a71e2f09dba408488b05070c6bc60b7870d4`  
		Last Modified: Tue, 17 Dec 2024 19:32:13 GMT  
		Size: 1.2 MB (1172813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34972ed5b0d6954f911cbbd5d23af040d1efad9f6664b651e9aa3f0da9b455ab`  
		Last Modified: Tue, 17 Dec 2024 19:32:12 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1c81811abb57648c93718c86dcc50031b1031f283a827d9592e101cb319812`  
		Last Modified: Tue, 17 Dec 2024 19:31:27 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5875d81ec9a34743fa5ee2c46ee06fbff464ca8a4e17933b4e7509dd6ad94c5c`  
		Last Modified: Tue, 17 Dec 2024 19:32:14 GMT  
		Size: 4.1 MB (4060101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0c2220d1c4fea07e3dfb01f412f8def09b235eb8230f21ef3ed54671786b0`  
		Last Modified: Tue, 17 Dec 2024 19:32:16 GMT  
		Size: 73.8 MB (73761465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dc5be93e78214a659eadbf4767473d9cae85d470e8a7505b7bb3aa9d1f204a`  
		Last Modified: Tue, 17 Dec 2024 19:32:14 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:0fab3efd997e0c2ce9d3b2d4b97cb0ff0b8b0ad6676c1cd24ebef99adae58362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ea27e4c1bcf87200bcf97b888333c93512d53286131a7353abdc368aec30b9`

```dockerfile
```

-	Layers:
	-	`sha256:7261b060119a546c85cdd6d7ebbc2bc36e0b2c193d1e5a666d4d03b2521a1578`  
		Last Modified: Tue, 17 Dec 2024 19:32:12 GMT  
		Size: 39.8 KB (39785 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; ppc64le

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

### `redmine:alpine` - unknown; unknown

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

### `redmine:alpine` - linux; riscv64

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

### `redmine:alpine` - unknown; unknown

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

### `redmine:alpine` - linux; s390x

```console
$ docker pull redmine@sha256:afd79d28740a46d58b64f0b5a1d06f91b6082f529fc458a65599e71e76663b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194749406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75761d5e03e3bb3490653cbef37262b51179b14a5094d3e047634e50531aeb0d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b1f2773e2373f026433fba037fb86a595d266626e42b662f8860b751051e6f`  
		Last Modified: Thu, 12 Dec 2024 23:30:57 GMT  
		Size: 7.1 MB (7120254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864ec4ce260568825466b713bba3f9b2fa5a20892a04198640c61084b49eb264`  
		Last Modified: Thu, 12 Dec 2024 23:30:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b4968fe585d95350f5b783349a96b3c374014aabb7194420884403d370892f`  
		Last Modified: Thu, 12 Dec 2024 23:51:53 GMT  
		Size: 32.8 MB (32778273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179a4112b44829f776bef61721047109c4474951e2a22356eb2fe2305e4fdfd8`  
		Last Modified: Thu, 12 Dec 2024 23:51:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8e04b5df2b0d1127a035e55134e68445033c6cf030edd21df40d292fd58031`  
		Last Modified: Tue, 17 Dec 2024 19:38:23 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1818f9c61cf356e887215bdb505c3795b4476e71a9c168167e0901d4bf803712`  
		Last Modified: Tue, 17 Dec 2024 19:38:25 GMT  
		Size: 71.4 MB (71357842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66dc872779c8a25418f15a4e070c4038bbd9062d9ef3b4a894d889c227e26bd`  
		Last Modified: Tue, 17 Dec 2024 19:38:23 GMT  
		Size: 1.2 MB (1161440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92d7826f0348b948c2e58c5c555b3f4b9645e74be670f66b638a33bb6f02f21`  
		Last Modified: Tue, 17 Dec 2024 19:38:23 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5029346b03f5991e5cbc45484b2b7deb41766249e3e4e4000ba4ef68495985a1`  
		Last Modified: Tue, 17 Dec 2024 19:38:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aada8726e32463ed2dce588a07652adaa007b254834aa2171af178fc97d7136`  
		Last Modified: Tue, 17 Dec 2024 19:38:24 GMT  
		Size: 4.1 MB (4060081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52907682d639c974a38524ee827f7053aeb5b8dd4c9a07840a81c71a2197a30`  
		Last Modified: Tue, 17 Dec 2024 19:38:25 GMT  
		Size: 74.8 MB (74798516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92489d4f7a40e4500cedcb8badfd671527fb7edadc8c9b11bb2ab7a8a7788900`  
		Last Modified: Tue, 17 Dec 2024 19:38:24 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:5392714f5448445b6305879bba71017827e631b9ca305d135c2bfd5130461f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1d8672441ad3c5297b9a3e0267d634b617704b808833def265cb745ac40833`

```dockerfile
```

-	Layers:
	-	`sha256:3748b018a008682a09e4b9c1da480f6123bc00ac83afb3fb1691fbfc97b5f97a`  
		Last Modified: Tue, 17 Dec 2024 19:38:23 GMT  
		Size: 39.8 KB (39846 bytes)  
		MIME: application/vnd.in-toto+json
