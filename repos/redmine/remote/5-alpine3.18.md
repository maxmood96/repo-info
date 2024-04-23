## `redmine:5-alpine3.18`

```console
$ docker pull redmine@sha256:f09e2223e9b02187d73cabc57c4b9c0ed0f29bac98af0afe213464187916e131
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

### `redmine:5-alpine3.18` - linux; amd64

```console
$ docker pull redmine@sha256:91b878c1be5470256df8b8beebe0092ffb3c8c65dc02e37d08064e9744be0219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202489394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aea429b072ca23a0453aaeae749018c32534280bb5729093f8660f5d7a7339a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV LANG=C.UTF-8
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_VERSION=3.2.4
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:34:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
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
	-	`sha256:8015fde631612c7da49cde041a2053e3c374debae3c5dcdf32e5efba9479f870`  
		Last Modified: Tue, 23 Apr 2024 16:55:04 GMT  
		Size: 4.1 MB (4140817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602508000a8e5641300d184da8bc9c24745fce1946bec3c62e8317a1c3348a8b`  
		Last Modified: Tue, 23 Apr 2024 16:55:04 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b5e2462d35de3cebd7e07ecf67a29dd3d80fd877835e8782fccd66db93da27`  
		Last Modified: Tue, 23 Apr 2024 16:55:05 GMT  
		Size: 34.2 MB (34211081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69f29194e2315c6b5a018b128808a7c76f8b825e10c2b312bab3f9ae2df8a1`  
		Last Modified: Tue, 23 Apr 2024 16:55:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0617164f0dabaa090f59f4c86c9a04d6c90c79d1e62870cd0c114aa7821bfee`  
		Last Modified: Tue, 23 Apr 2024 17:57:46 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438b80f4f1100b5d7b9e592300ef5f247589f0f18f05b8ce5d1e4a6d20c5693`  
		Last Modified: Tue, 23 Apr 2024 17:57:47 GMT  
		Size: 87.4 MB (87375209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d1d166be7291b4e925982e417fa693a58469d33342791592e604d40126f5d4`  
		Last Modified: Tue, 23 Apr 2024 17:57:45 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bf327aaf64b41db965d6a3b7e02639a06abcf894be783c02591ec1bdaaed03`  
		Last Modified: Tue, 23 Apr 2024 17:57:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d6891772482472ab9f33219f05b241534c80994d811ef5248e821c59a9f4bf`  
		Last Modified: Tue, 23 Apr 2024 17:57:46 GMT  
		Size: 3.2 MB (3242953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0435ddf002018709131f6c8ff7747b1a1c2d6a27ed6416621d9c112b76e131`  
		Last Modified: Tue, 23 Apr 2024 17:57:47 GMT  
		Size: 70.1 MB (70112978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c7ca4ee9f41188efa355148538812f78655f76e3b99b8e2f25ff9c00812ee5`  
		Last Modified: Tue, 23 Apr 2024 17:57:47 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:e77cdf3750e8daba19ed7f783d0a96aca10ff1b977456287b15c99673d4821b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5395711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93009b20f700840b437ca7d24323cec64fcf872dd5b8808c116a6990cd7a544`

```dockerfile
```

-	Layers:
	-	`sha256:bbebd1c920f32525f4cf31815e353f778e5d7ef32ea7054d15e93a86b6fb0ca0`  
		Last Modified: Tue, 23 Apr 2024 17:57:45 GMT  
		Size: 5.4 MB (5360484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3a786e5862de693ba47150282a054b92950dc894d3a3e2dd2c286dc1b874fa`  
		Last Modified: Tue, 23 Apr 2024 17:57:46 GMT  
		Size: 35.2 KB (35227 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.18` - linux; arm variant v6

```console
$ docker pull redmine@sha256:8a1c525921456824e862d86f9b020b995ec54ca7920d80e920531b42c75ead45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192672646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1939e0ec1548c8002af8329b6172ee3cd62e497c227b34bf708dc32ed587f96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV LANG=C.UTF-8
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_VERSION=3.2.4
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:34:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
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
	-	`sha256:f552652f091dfe0a928791eb6f50f81ec123ad9891af681575e3be4a2042d11c`  
		Last Modified: Tue, 23 Apr 2024 17:00:18 GMT  
		Size: 3.8 MB (3816403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fda9f81cf6aa6ffbc83f8a78a90e50b455b3969d586acd3584d36beee27a7b6`  
		Last Modified: Tue, 23 Apr 2024 17:00:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f326d541bacea473f47d35c2c3fec7e56cd5a0f3f633375f59a244618ae5c5f0`  
		Last Modified: Tue, 23 Apr 2024 17:06:33 GMT  
		Size: 30.0 MB (30015753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d914950cab98694a8509c1ac855aadbd66443c9c1b3a6be232c1a44f16e7e2`  
		Last Modified: Tue, 23 Apr 2024 17:06:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396db7808e9e50479bf285dae49313bd56171bcd109566fd2f49d5b0c26af8c6`  
		Last Modified: Tue, 23 Apr 2024 18:03:39 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b98a13b48406a25abc81fe0078b24d7a6d257457a6ecfefac8fe29249cae9`  
		Last Modified: Tue, 23 Apr 2024 18:03:42 GMT  
		Size: 82.9 MB (82913264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52eb5f62b611b7aba7151484e91a758934bc91066f6a477efd0ff5f63f09f4d4`  
		Last Modified: Tue, 23 Apr 2024 18:03:39 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6b48a78d4d28945747ac2f1cc2adf24876a412831a5cb5c4ca5d0e5022514e`  
		Last Modified: Tue, 23 Apr 2024 18:03:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9fb8992fbb222f77659a6e4e1e9b66d6b8c045bed9f0189ec0eaa6121d2313`  
		Last Modified: Tue, 23 Apr 2024 18:03:41 GMT  
		Size: 3.2 MB (3242948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b74f7062b7e43ec1199ac60ee94928096780535d547d7e47888d3ba592ac524`  
		Last Modified: Tue, 23 Apr 2024 18:03:43 GMT  
		Size: 69.5 MB (69533404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd96ece12a15edeed950a380fca7cadd61e6ce1b7474ecece7b6c4266183790`  
		Last Modified: Tue, 23 Apr 2024 18:03:41 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:c2548ef700bac7b1d0f9499ffba4abf76ae04fbc8edd1c605594691d3a2981b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 KB (35222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581a6cec72a3b4a3fbd4e88bd8562fd4e2b3a08bc18301dc26e793fc5d359d9`

```dockerfile
```

-	Layers:
	-	`sha256:47ebeb3003de69a063de99629e65f500994bd1915f25b19dead98c9042465501`  
		Last Modified: Tue, 23 Apr 2024 18:03:39 GMT  
		Size: 35.2 KB (35222 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.18` - linux; arm variant v7

```console
$ docker pull redmine@sha256:f2f53e0a62ef9cb3369d2c83cd85fcf6877d303c08f0a10761649e7f9f2e1979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187568732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c8410993a1a49da6ac68d09ce5124081569226661cb9c39a82fa83687507ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV LANG=C.UTF-8
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_VERSION=3.2.4
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:34:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
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
	-	`sha256:6540439ddf5e1e7b6eb4e80bc550670012c5d4e0d098079197a75778381420bf`  
		Last Modified: Tue, 23 Apr 2024 17:52:19 GMT  
		Size: 29.8 MB (29754450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bde9ed09649652548112347e7fa668e1245eace35a31b84bbaecf7a980b6fa5`  
		Last Modified: Tue, 23 Apr 2024 17:52:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd495bf30f5c58f23e1922d56ec490de45a7717f04f6fc4b0d3c8f16092d1b`  
		Last Modified: Tue, 23 Apr 2024 19:32:40 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab694c316adca0f9778be934bf4b020f3024b07bf949173cc6ded55a560479aa`  
		Last Modified: Tue, 23 Apr 2024 19:32:42 GMT  
		Size: 79.4 MB (79403229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd607d1c494d3da2ceea470cc1f132da70141ee5c3d2808f9446d9bb94569fe`  
		Last Modified: Tue, 23 Apr 2024 19:32:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3280177164c2da3c419b7c80168fbe9fd42056288810350bd3e7cd1fbd9f3a`  
		Last Modified: Tue, 23 Apr 2024 19:32:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ed7ddaa6a96df0c0240c7a724ff98e57eb03958b75c42a3bc0f85ea72c04f0`  
		Last Modified: Tue, 23 Apr 2024 19:32:41 GMT  
		Size: 3.2 MB (3242811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291b06cbca4f9e426a7d87e77d69de734c5b60650bdc4414a767bb8e6c7efb0c`  
		Last Modified: Tue, 23 Apr 2024 19:32:44 GMT  
		Size: 68.5 MB (68545949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23622c2e5b1b44898b5d8f6784340ec0fca027e24b409f8b5ee362103ae4da0`  
		Last Modified: Tue, 23 Apr 2024 19:32:42 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:138b71f02370d19cc4bf549f52d3960b732aa424e63b87740e7201eebaca9e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5372999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20932b66c6b9c3114abb329eabe51b88f0849956849310ea4122381593945265`

```dockerfile
```

-	Layers:
	-	`sha256:93f0531312f6bd3d85f6d74420b77785514bc2b79d26a9eb8cda3ee87ecf4a3d`  
		Last Modified: Tue, 23 Apr 2024 19:32:40 GMT  
		Size: 5.3 MB (5337558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b087b012cdb2fcabebc1001b8ec886ce634dc8f3dde7dfaf99e37b24e51d27`  
		Last Modified: Tue, 23 Apr 2024 19:32:40 GMT  
		Size: 35.4 KB (35441 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:a608c688d4890209b6c45313530ab6c9d277652914cc76b1795aa3f3f0aabc0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201760004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eef305668652a740aa72fd92c2a8e9ba7ae7ebadcc08466fc29782801277d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV LANG=C.UTF-8
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_VERSION=3.2.4
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:34:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
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
	-	`sha256:34bf32488dbfcebe416f45916c55ef4000ef91383c4aca2d50db6a7bdc7cb484`  
		Last Modified: Tue, 23 Apr 2024 17:31:43 GMT  
		Size: 34.1 MB (34093624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc96d205ec96f39276a028a0e2d5defb2f7bceb0abf226f4f41a940a9887e32`  
		Last Modified: Tue, 23 Apr 2024 17:31:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85b52f5edc8d06e148b466efad57334ad15f4eb0c1c0e2edb03dc56e9a14a79`  
		Last Modified: Tue, 23 Apr 2024 19:41:07 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec32c6bbef7c137766aef7678a7f297a58a0ae78b63e293e3b3937a1a6987aee`  
		Last Modified: Tue, 23 Apr 2024 19:41:09 GMT  
		Size: 86.8 MB (86817836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8675a8972361f4647535a62a9eeebe4fe0d218cd35f6e4dd0b1087e3ed54ba74`  
		Last Modified: Tue, 23 Apr 2024 19:41:07 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83483e3e47c27ac974fc5a41d251f2b92164a662f8e8985cfc12f10f612966c`  
		Last Modified: Tue, 23 Apr 2024 19:41:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf3e99d372d622f17bea3c17618cda09a0abbc06edd5b68002323e977ebeb8b`  
		Last Modified: Tue, 23 Apr 2024 19:41:08 GMT  
		Size: 3.2 MB (3242907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6b290506ad4a45a05c0ff2253f60f1e18512954d070c61466f810524d1feaf`  
		Last Modified: Tue, 23 Apr 2024 19:41:11 GMT  
		Size: 70.2 MB (70207083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a590804d5f65b7aad1eff2c3c4fdc730f8397845f6889efe48a8a8f399547f0`  
		Last Modified: Tue, 23 Apr 2024 19:41:08 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:13ec1927b9437722f6d250dc659560fbd3b0c4819a76a35fe4095615a12fd58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5373805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120f9d026d4e13f14a732e33c4a8606c102855aa04df84740ec9fb42c1583c69`

```dockerfile
```

-	Layers:
	-	`sha256:2e04a5ddeb4ccb12c574d19090ce27bc5a75254f27d361efb30b5d06e68af657`  
		Last Modified: Tue, 23 Apr 2024 19:41:07 GMT  
		Size: 5.3 MB (5338500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e459e6e06a46001e1d069599391e1151722e53d20b2326475bc6cd02265f0d84`  
		Last Modified: Tue, 23 Apr 2024 19:41:06 GMT  
		Size: 35.3 KB (35305 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.18` - linux; 386

```console
$ docker pull redmine@sha256:766d4039f43a0cc19ddbb5c38400d7ad7431a3aa7065e632ea022c15c3e35758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194950124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1951c9b96601984c102adc0c0dae03d9a87c6de9d19a3f006cf52b8af7d7983`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV LANG=C.UTF-8
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_VERSION=3.2.4
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:34:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
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
	-	`sha256:4089b09abbafbc64146d41b9b66dc87e25a575d9bc51fbf66d29e95fbe09def8`  
		Last Modified: Tue, 23 Apr 2024 16:54:38 GMT  
		Size: 4.1 MB (4146990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2415467dd25e288f2b5f09a929d530f9755d507f4b55a9f9d56955cdff42445a`  
		Last Modified: Tue, 23 Apr 2024 16:54:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1583251aad521c0dadeb64ec74a2c9ed2e22288265a5b59332b89cdac4a7685f`  
		Last Modified: Tue, 23 Apr 2024 16:54:38 GMT  
		Size: 30.0 MB (29953571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a9934640675fb957f013cbcd8eb1443f7514295d2552b7a451ed04d4874999`  
		Last Modified: Tue, 23 Apr 2024 16:54:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7133a91d0f4519be7f6d5b8f8df2b9815ee36adae95c03a6bf0f0c654cc0a43`  
		Last Modified: Tue, 23 Apr 2024 17:58:14 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78a6689b19b7c0feb7de5116b53695bd46be5be76b131f346335676fe99b5f3`  
		Last Modified: Tue, 23 Apr 2024 17:58:16 GMT  
		Size: 84.2 MB (84230506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9870cd911fb15aae85b864d6bad72157eab5cb3a372d7d998a46e969ca34ed`  
		Last Modified: Tue, 23 Apr 2024 17:58:14 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b9628becdc2b2145c0cd2a5369bc63af6cc8b6f1ac39d3ed29de3f96b44e0b`  
		Last Modified: Tue, 23 Apr 2024 17:58:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b42b8ce4609139ed227feeeb53af62dddbdd961c82d4f86e7e3886f37d39bda`  
		Last Modified: Tue, 23 Apr 2024 17:58:15 GMT  
		Size: 3.2 MB (3242967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2720e6070061ffd0249073016149d13aa36d49c6fdd7b5ddc4788755f6175a13`  
		Last Modified: Tue, 23 Apr 2024 17:58:19 GMT  
		Size: 70.1 MB (70133212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905a6c6337e1a2f246fb357c4fe4b7598005232bb5545239160ae171cec7512c`  
		Last Modified: Tue, 23 Apr 2024 17:57:51 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:30f0132eb62a3d86e63727903d51d01c0027e3b77929348ccaffe0b1416434b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5395382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abe7a685aa2a93e0a9dbff6523b0c2873af6b8e416aaa98cc5d33a136c69ea3`

```dockerfile
```

-	Layers:
	-	`sha256:ea4befe83ca3af6f19159eaa39dacc522228208d5aa9b8e0b4e60396e481c261`  
		Last Modified: Tue, 23 Apr 2024 17:58:14 GMT  
		Size: 5.4 MB (5360215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f72c736d70f14ba6412e62fdbca7562f8d3dd4985eff753993ffa0f0632f01b4`  
		Last Modified: Tue, 23 Apr 2024 17:58:14 GMT  
		Size: 35.2 KB (35167 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.18` - linux; ppc64le

```console
$ docker pull redmine@sha256:07a73eb0e4bb8c5e15cbd77aee20e2b5c09d0625bb62c74483bac55b3b09edfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207537658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a859c5086442b265595e7794113aa7c570254798e038bf7ceec46cee163897d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV LANG=C.UTF-8
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_VERSION=3.2.4
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:34:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
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
	-	`sha256:87d1b9e46c762a0cfa57794c331b5b6e95c451702d28589536de047939fef272`  
		Last Modified: Tue, 23 Apr 2024 17:54:47 GMT  
		Size: 31.4 MB (31386015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da2cb3e58f68e89746f7d5ad88ab8c95ab689a0b4bbc2939850e39d92feed3`  
		Last Modified: Tue, 23 Apr 2024 17:54:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49684402f6c531767ac5d72d7a856645ac98a9ef0b953f4ddd1b560cafda0bd8`  
		Last Modified: Tue, 23 Apr 2024 19:27:31 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a5ed65d4b83d537e7f11153334eeec03c60789cd035c7b1df2fd4866c5855d`  
		Last Modified: Tue, 23 Apr 2024 19:27:34 GMT  
		Size: 93.0 MB (92991128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3cd7a6f20cb79278b50a36bcf27073b601cbbee20102b29a2c4125d99d1c16`  
		Last Modified: Tue, 23 Apr 2024 19:27:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc77e83fa4ba478882f50e096025b79ae9319f4ae22efb58c93cdb103e0173c`  
		Last Modified: Tue, 23 Apr 2024 19:27:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca20dbe810714341e3a1f57cd248e663fdd721812f9dedd41c20649bf914ea9`  
		Last Modified: Tue, 23 Apr 2024 19:27:32 GMT  
		Size: 3.2 MB (3242912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744ef1da90bda5e2893611d8fe289aabfa11181c007ee3cbdd6bf470fc399e5`  
		Last Modified: Tue, 23 Apr 2024 19:27:35 GMT  
		Size: 72.3 MB (72286110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908a8089db74f75449569d6e1a00552d8f5a781754be30ff196535a8e3961169`  
		Last Modified: Tue, 23 Apr 2024 19:27:32 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:4650e1987bfe9ff0932be492447601f8a08ed66636b197fffe3205b0827cbc6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17655954e73ff40b468a68c705db7a3696d67d544989477b10dd40b015c2a9e1`

```dockerfile
```

-	Layers:
	-	`sha256:1f85b81653ab28ddf6681500712ac73fcbbde20028fd0e1cdf100d3153ceafd1`  
		Last Modified: Tue, 23 Apr 2024 19:27:31 GMT  
		Size: 5.3 MB (5344985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8275738f387ee3fba99a12f9d2dc6d44d7a8e16fb901564e0894c6c7805c17e4`  
		Last Modified: Tue, 23 Apr 2024 19:27:30 GMT  
		Size: 35.4 KB (35356 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.18` - linux; s390x

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

### `redmine:5-alpine3.18` - unknown; unknown

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
