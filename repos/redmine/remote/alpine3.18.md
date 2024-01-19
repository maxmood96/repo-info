## `redmine:alpine3.18`

```console
$ docker pull redmine@sha256:534f0752376d706f5d55ee9f81cf38acebd660e17b077188cff4f15bef60b7aa
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

### `redmine:alpine3.18` - linux; amd64

```console
$ docker pull redmine@sha256:0c72592e80405851ca890cc72252dd14778a52071364b8bfbdb8d598c4f89377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.4 MB (202411303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0242b8645fedaa2e7c75d50988331b5317cd6877d5220c3ab37520033768fba2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_VERSION=3.2.3
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 Dec 2023 17:42:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:42:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["irb"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RAILS_ENV=production
# Tue, 19 Dec 2023 17:42:47 GMT
WORKDIR /usr/src/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
ENV HOME=/home/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_VERSION=5.1.1
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 19 Dec 2023 17:42:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7292c03ea2416c3bfebac51d3b25f83a7fc7347aa60f8e10664081ba8d0660`  
		Last Modified: Thu, 18 Jan 2024 23:07:18 GMT  
		Size: 4.1 MB (4131306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c2f9db2c4ad8e8c329914fb7dd83dd64981318e33a1c7e0cf7f16a373fc88f`  
		Last Modified: Thu, 18 Jan 2024 23:07:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f418a6a5f86f6e6b49ee3eb9735218a364834a2c52487ebdbf9ae9633846c7de`  
		Last Modified: Thu, 18 Jan 2024 23:07:19 GMT  
		Size: 34.2 MB (34196998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa47c1374c44511b27f8d84684e7615b4fb228ec0500beb1d0e7624fd87e5517`  
		Last Modified: Thu, 18 Jan 2024 23:07:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed68b20e3ce0423fa5f8b9d1b6128af505f4e28f01b87018210219074f7e21c`  
		Last Modified: Fri, 19 Jan 2024 00:00:56 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c2e57fc1b6713475faa8516263be1625dca865fc15718d91df12ff0174894a`  
		Last Modified: Fri, 19 Jan 2024 00:01:00 GMT  
		Size: 87.3 MB (87320881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b6fef5bfec8407b676aa7ca337348672cbdf456e2fca8c138b0a0161781872`  
		Last Modified: Fri, 19 Jan 2024 00:00:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed403e1e12d21490ddb55c74644778e6c8a686dde110e99d55084d6d8f77c9e`  
		Last Modified: Fri, 19 Jan 2024 00:00:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138c5a2eb309628f750dc88d6bbf80f00f695a855330e3af57f00870f525c23f`  
		Last Modified: Fri, 19 Jan 2024 00:00:57 GMT  
		Size: 3.2 MB (3236781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba162c426cf31c0d4438a0c1480381412ac489328a32310805b5906500ab6f14`  
		Last Modified: Fri, 19 Jan 2024 00:01:00 GMT  
		Size: 70.1 MB (70119103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b2a6178059cd91a16ab7480215bb3530540d0c49a603b8718c108492e1332b`  
		Last Modified: Fri, 19 Jan 2024 00:00:57 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:cc82b8d3c80e1fd7b9fc10cf4caf3f64bf18442c991d26be5e49a0bf0a475f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4608568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9371e54201d09aeb824d1042cd4945157fb95cf30b9bc84800aa2e2ff01cb0`

```dockerfile
```

-	Layers:
	-	`sha256:c23796e9d9fefcc381f4c05da478ef751716b3f513df0af031a38c1ded31824c`  
		Last Modified: Fri, 19 Jan 2024 00:00:56 GMT  
		Size: 4.6 MB (4573345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637fe384262ae81f7d369f36ac89508df5f1efb18c22e70e2f378dcee5c16bf2`  
		Last Modified: Fri, 19 Jan 2024 00:00:56 GMT  
		Size: 35.2 KB (35223 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.18` - linux; arm variant v6

```console
$ docker pull redmine@sha256:061a5b0ea9ab609777e28e17265c4d36e24845145267c59069f36bf2259389c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 MB (190768611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a9a5fb1bed75f3ec0581cd0bd15540bf59ce861621b3be5a1f274bc1b8e3b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 08:27:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 08 Dec 2023 08:27:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 08 Dec 2023 08:27:14 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 08:27:14 GMT
ENV RUBY_MAJOR=3.2
# Fri, 08 Dec 2023 08:27:14 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 08 Dec 2023 08:27:14 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 08 Dec 2023 08:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 08 Dec 2023 08:27:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 08 Dec 2023 08:27:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 08 Dec 2023 08:27:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 08:27:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 08 Dec 2023 08:27:14 GMT
CMD ["irb"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RAILS_ENV=production
# Tue, 19 Dec 2023 17:42:47 GMT
WORKDIR /usr/src/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
ENV HOME=/home/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_VERSION=5.1.1
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 19 Dec 2023 17:42:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac4102a1a867f369c980a90985230f98b70b5adbaeb2c8a3ce4653840b6fd2`  
		Last Modified: Tue, 09 Jan 2024 00:00:58 GMT  
		Size: 3.8 MB (3807307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa2a8ccba1d698dbae0efc64b73da679551a8ea8d5876590ebcfd3b04e76efa`  
		Last Modified: Tue, 09 Jan 2024 00:00:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f860a004d869af9246159cf7f775c8d65d599f2f86fe4fba7f4d2b1f6a6cb4`  
		Last Modified: Tue, 09 Jan 2024 00:05:32 GMT  
		Size: 28.1 MB (28105793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8714d2a8eba8ff82efaa14d1388ed427efa39a48db61db6d0728ab760bcc0581`  
		Last Modified: Tue, 09 Jan 2024 00:05:31 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9726326754855c239ae8111b926054a4a3b4edbe47c138c7458af6f4a0e22892`  
		Last Modified: Tue, 09 Jan 2024 07:16:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae31e0e515cd03d7ca8fb5d7098b4f07b51c9f09cbf97e73c90fe8f552a0be7`  
		Last Modified: Tue, 09 Jan 2024 07:16:49 GMT  
		Size: 82.9 MB (82896872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6258cebfc93c52e592b3447f262d56e22db12754b9ee5b5c8fe7b5350127a0f9`  
		Last Modified: Tue, 09 Jan 2024 07:16:47 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a4293286f6a207101c55bf71d6935d35df8ad62518c239d5c2dd63c754a34`  
		Last Modified: Tue, 09 Jan 2024 07:16:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e598537ee21fcdedae6509ce566c7bd7b0a532a42070181098ff3d5530dcd193`  
		Last Modified: Tue, 09 Jan 2024 07:16:48 GMT  
		Size: 3.2 MB (3236712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aef08d434b112a00e274330cf93cba5c2af049981f3d07c4e0ad8637fdf01`  
		Last Modified: Tue, 09 Jan 2024 07:16:51 GMT  
		Size: 69.6 MB (69571247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a01bb421aa7591a592e52d49f5065f449c453e6c2dc73a35a617e276c88f91d`  
		Last Modified: Tue, 09 Jan 2024 07:16:48 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:02f45ce1d571a33ad20cce53e4f549cdb9108c82927a9bac463aeace13a2310a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 KB (34912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b44206ae4eafc8ba264bc657ac5467ea65496f5b14e82d04ba6f676acefb901`

```dockerfile
```

-	Layers:
	-	`sha256:fd8add36cbd75949557886715a6b27f6dab21c3604c598cb02e7f42cc32ec303`  
		Last Modified: Tue, 09 Jan 2024 07:16:46 GMT  
		Size: 34.9 KB (34912 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.18` - linux; arm variant v7

```console
$ docker pull redmine@sha256:30f48af49502f51b0b1514e627d06f546124a15bd24181acbd80aae902f60000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187505965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877fe63eb003badc5e74fe623c1a520f579fe7e355a21fbf34a985b0c8277b13`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_VERSION=3.2.3
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 Dec 2023 17:42:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:42:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["irb"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RAILS_ENV=production
# Tue, 19 Dec 2023 17:42:47 GMT
WORKDIR /usr/src/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
ENV HOME=/home/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_VERSION=5.1.1
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 19 Dec 2023 17:42:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0749f3b0efa821230d28ae473fdc082c47032a93f02bb59e86145a80bd80b8e3`  
		Last Modified: Tue, 09 Jan 2024 00:40:14 GMT  
		Size: 3.7 MB (3717086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654b58f0f160303b0218412d2644994f07dadb8689c9cdcd6669bcc10c469a60`  
		Last Modified: Tue, 09 Jan 2024 00:40:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4acfb008f477fd184dae70c8b054a478773c376e2a3e96dbee1c88e9c50596`  
		Last Modified: Fri, 19 Jan 2024 08:41:06 GMT  
		Size: 29.7 MB (29743258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93731896ebdf4f935166e497430ecf444c7319903af5abaa96c5db4f0aea997`  
		Last Modified: Fri, 19 Jan 2024 08:41:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2abfd0a400d97e890e8664e02c4e225bde5976c7143b975769ce2c69af2d4c`  
		Last Modified: Fri, 19 Jan 2024 11:16:48 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2feef16013f0ca5a80c1c836376d83aafce61c4418d9762f17553233267935c2`  
		Last Modified: Fri, 19 Jan 2024 11:16:51 GMT  
		Size: 79.3 MB (79346310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a51cdcc36fc39aea572cbc6c56ce961e4559abeaf6274b67881575b5ab16e33`  
		Last Modified: Fri, 19 Jan 2024 11:16:48 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0836ce55b72131a49b2794a11fe3339fda875113b00f67c281fac6e6929f89`  
		Last Modified: Fri, 19 Jan 2024 11:16:48 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d42e01cfa02e3ba43e7b240b701fd4e187991c95e2a0a55a13fd941b577c35`  
		Last Modified: Fri, 19 Jan 2024 11:16:49 GMT  
		Size: 3.2 MB (3236799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faada43a6cf08eb82bfe0d2e82a4e0f9229d17651dc427d7a2bcc01e1ebc533b`  
		Last Modified: Fri, 19 Jan 2024 11:16:52 GMT  
		Size: 68.6 MB (68557692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326317363c312e83388dcb7b642478b86fc2abb582a68bedcb2213b30d979e2b`  
		Last Modified: Fri, 19 Jan 2024 11:16:49 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:51251f0a50668abb13fdbc50b401bf434b10dbb6aa6ddeab3a3787a9f59f8379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4594005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f08d61eb873c3305461262984358cb12b44e7c096828a7641c69a710b925fbf`

```dockerfile
```

-	Layers:
	-	`sha256:8468382e9311ef127927373c42549e4808b2a463a4d740b9d1b952dd4dbe9d3c`  
		Last Modified: Fri, 19 Jan 2024 11:16:48 GMT  
		Size: 4.6 MB (4558568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a1c220e3e389a5609e003a88d2c01c767ccafae223f63c3846f062ffe2bc94`  
		Last Modified: Fri, 19 Jan 2024 11:16:48 GMT  
		Size: 35.4 KB (35437 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:2743912f5c4c509768e1069f2fb5c443f9dd6e8f8de1f7161e757764bcfe7b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.7 MB (201720434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1fa4f10dcb858ab4c069e29a80f781b07f1a0a3fca73844da722f09e078bb5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_VERSION=3.2.3
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 Dec 2023 17:42:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:42:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["irb"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RAILS_ENV=production
# Tue, 19 Dec 2023 17:42:47 GMT
WORKDIR /usr/src/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
ENV HOME=/home/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_VERSION=5.1.1
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 19 Dec 2023 17:42:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913c9a36677bed0b58848a467bca0022a408c0367ed3bea8c91e07acea3056f1`  
		Last Modified: Tue, 09 Jan 2024 00:42:07 GMT  
		Size: 4.1 MB (4061383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01647eac9928e13f49ef82d760dc0e09f240ef8ffb8178a93ef6b12dae93ac`  
		Last Modified: Tue, 09 Jan 2024 00:42:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41587859f929764618bae79c7b9bb32fe3fd56053bd6ef3d8fa73b008ab17dcf`  
		Last Modified: Fri, 19 Jan 2024 03:36:32 GMT  
		Size: 34.1 MB (34080966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5e057c55f542e73ee7522421402c91fe380b75c11e4406d921aa65b10604d4`  
		Last Modified: Fri, 19 Jan 2024 03:36:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe7794b6c0a7cd2f7ada04ceed3b3bf04a0ce6de7b238349dabff28741c4e73`  
		Last Modified: Fri, 19 Jan 2024 05:39:00 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051bd406caaba59c26973a072876b94631fcdda29745b57615078c97b81da747`  
		Last Modified: Fri, 19 Jan 2024 05:39:03 GMT  
		Size: 86.8 MB (86769351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1378170a60e123e2591a675daf522a678e6862ddc5e9eb11ee7989724d15f068`  
		Last Modified: Fri, 19 Jan 2024 05:39:00 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f13884242481bce305df392ff661209ecb704c274aa91f65a085219ba142e4f`  
		Last Modified: Fri, 19 Jan 2024 05:39:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585021a24a4dbbd03ddb4cebf044b90f5cbc7122f008fd74b6505538aed9725b`  
		Last Modified: Fri, 19 Jan 2024 05:39:01 GMT  
		Size: 3.2 MB (3236766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de26173dd6a7621b3e19fbff846f07999b267160a0649835b89878f8704e2f4`  
		Last Modified: Fri, 19 Jan 2024 05:39:04 GMT  
		Size: 70.2 MB (70235125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9184f715e1937b2eb0809a2d728b08e77f043cc8a782f3de398aeef418d44a`  
		Last Modified: Fri, 19 Jan 2024 05:39:01 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:1913c949c6c59e46c3256cf1d616dafecb58ed9f787aaf090c74c9a72812c93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4594599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590e97ad44e80a20980568e2ed2ae49818b0ec5b87e0c8cc95774172843cd865`

```dockerfile
```

-	Layers:
	-	`sha256:e4d419658fbcb80f54f3a08c66bc65d33de531b5c72e4628c73f68d362d7c9e5`  
		Last Modified: Fri, 19 Jan 2024 05:39:00 GMT  
		Size: 4.6 MB (4559298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2ad7a7e92e7424591ccac2da9991e1c27e12f2cbdef1b882d743184400b0d6`  
		Last Modified: Fri, 19 Jan 2024 05:39:00 GMT  
		Size: 35.3 KB (35301 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.18` - linux; 386

```console
$ docker pull redmine@sha256:f77448ecc2ec3bf14062e0c371ea31774a837fae82eb4f43223b24af31380870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194891782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5d3b59e5bc1f4fe2d627d3275bd3d4f8f40ab3b6ca859b86f313a06a853f0d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:44 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Fri, 01 Dec 2023 02:03:44 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_VERSION=3.2.3
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 Dec 2023 17:42:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:42:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["irb"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RAILS_ENV=production
# Tue, 19 Dec 2023 17:42:47 GMT
WORKDIR /usr/src/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
ENV HOME=/home/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_VERSION=5.1.1
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 19 Dec 2023 17:42:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5103be0ffb5e807f37e5202a354ca09ea8f0eba6c1c96089bdbe15627f56ebe0`  
		Last Modified: Thu, 18 Jan 2024 23:06:55 GMT  
		Size: 4.1 MB (4135750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dfa8a828882872f954322407b448f1a3baf05dc435438e11c010dae9689d76`  
		Last Modified: Thu, 18 Jan 2024 23:06:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69242b264fa9805b6b3d65913e251bf68a9ffdc8e20da261d5da780808f65d8a`  
		Last Modified: Thu, 18 Jan 2024 23:06:56 GMT  
		Size: 29.9 MB (29946847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82bb03ff204842e49ecbfdd0f01b61ff72573ad57c77349b422b29067b8c213`  
		Last Modified: Thu, 18 Jan 2024 23:06:55 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6891ba193d277ede274fb014060915d3cb3346958c9a013073a3185c7a062869`  
		Last Modified: Fri, 19 Jan 2024 00:01:01 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9becd873bfb73d9fb8cae6edfec9bc8e3a2c8b0a46a84377fafc8149b958c850`  
		Last Modified: Fri, 19 Jan 2024 00:01:03 GMT  
		Size: 84.2 MB (84187834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3ae13082081aa5466cb78887c171a9bfd55ea13a2cd69d7aece0eccb3ce187`  
		Last Modified: Fri, 19 Jan 2024 00:01:01 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63bc5a574d3cfbe3647a837b562d772b85bfaabd52ae8c53fd0e9fbdae1bad5`  
		Last Modified: Fri, 19 Jan 2024 00:01:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ca27143577fd4c90f6134e06dbb251df0c66c6e540d85d228ebdce9a17dafd`  
		Last Modified: Fri, 19 Jan 2024 00:01:02 GMT  
		Size: 3.2 MB (3236533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cd6469ed077436094a9fe1f5b0e60fd2da365e182883934884187572eaaca6`  
		Last Modified: Fri, 19 Jan 2024 00:01:04 GMT  
		Size: 70.1 MB (70142173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835418c8e27cfab895f56b00da844975eaaa22e07e1f83c134adc71d43ea11e4`  
		Last Modified: Fri, 19 Jan 2024 00:01:03 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:728752317c49fda945851f03ce2e8acff4ee1d2947f9992578200853848f3e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4608239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff2615031301abebcd69d317d04f0a67ae01fb8086502999e9e463e26007caa`

```dockerfile
```

-	Layers:
	-	`sha256:00a5f0efcfc2c5b0615be0b600dd68b5b0ef278e49a8e9de7c78efa8f67a82a6`  
		Last Modified: Fri, 19 Jan 2024 00:01:00 GMT  
		Size: 4.6 MB (4573076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16aab5902e34407b665b9663d8badbdbff63ecad8d076452836600fd6d674db8`  
		Last Modified: Fri, 19 Jan 2024 00:01:01 GMT  
		Size: 35.2 KB (35163 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.18` - linux; ppc64le

```console
$ docker pull redmine@sha256:4de98e667f036e1fd51172d087c3550c0660f0903ec5ede9ede1a34955ae9566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207492262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483ef61091eeaf753fa4f9bb7c4863f144f7277ef6abff11b05147f367ad82d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_VERSION=3.2.3
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.3.tar.xz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RUBY_DOWNLOAD_SHA256=cfb231954b8c241043a538a4c682a1cca0b2016d835fee0b9e4a0be3ceba476b
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 Dec 2023 17:42:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 17:42:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["irb"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RAILS_ENV=production
# Tue, 19 Dec 2023 17:42:47 GMT
WORKDIR /usr/src/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
ENV HOME=/home/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_VERSION=5.1.1
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 19 Dec 2023 17:42:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c747964fe8e897c577857ad402f9f9d19fd9ae6eff414e72b12b28d1bc7de3d1`  
		Last Modified: Tue, 09 Jan 2024 00:40:20 GMT  
		Size: 4.3 MB (4279242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6788641a1eb13419541cf6d2285aaae7458f55a2af9ad7378bb8eb241a4b9ec4`  
		Last Modified: Tue, 09 Jan 2024 00:40:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef571bfb7a110773f06e62a73c5018d7dd4546af62d003b0736a57d8222e3154`  
		Last Modified: Fri, 19 Jan 2024 02:17:42 GMT  
		Size: 31.4 MB (31379953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40e44232fe3aa5e7c4727b1c8fc68131620644a548c8edf7a42ceb9924f2a14`  
		Last Modified: Fri, 19 Jan 2024 02:17:41 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9069d23b93615ee3e3c3e12de8683f97d4ea8740ab1f0d7c20733520866169bc`  
		Last Modified: Fri, 19 Jan 2024 03:17:37 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106a6ff2d910e3adbb45a403dccb7219e0c95773a30bc978e70643c957f5fef0`  
		Last Modified: Fri, 19 Jan 2024 03:17:41 GMT  
		Size: 92.9 MB (92942272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc069979653ed64a6502df659ed6006cc4d34a6d5cc82900dcc0502a9510e6e`  
		Last Modified: Fri, 19 Jan 2024 03:17:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea27176709c6b0612d4a5215f6c58a3a7e8d4bcad9eac532db3fac215cc90d`  
		Last Modified: Fri, 19 Jan 2024 03:17:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf4d93655113eb94415b69a743b7d112eb678b1236a4f2a41301fc4dd2ecdf1`  
		Last Modified: Fri, 19 Jan 2024 03:17:39 GMT  
		Size: 3.2 MB (3236830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b83c59a603f50442c661c7267c4e289b5dffac8e761425ce48820914e0ba14c`  
		Last Modified: Fri, 19 Jan 2024 03:17:42 GMT  
		Size: 72.3 MB (72301827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1568b17b95e5eaf6b5dfe705313b7e9002ba444c442fd4bf8087c44ac52963f`  
		Last Modified: Fri, 19 Jan 2024 03:17:39 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:57f4f088dcaefb9283a7d429f2b1af2e5085289287da534abe7074c17243b309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4600075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07f352a756b78c71aae7b488f5374232e56d8c68dfa4d2a27e4f3e150ce59b7`

```dockerfile
```

-	Layers:
	-	`sha256:c65fc03e278f5cbabf38ea18884f37e4d60ab8949f4994aa25ba499d2cdbdb79`  
		Last Modified: Fri, 19 Jan 2024 03:17:37 GMT  
		Size: 4.6 MB (4564723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87136cba16582b235ccd3ed3b9c5ae51e21ff2f053f70e54edd1b38b6c10d81e`  
		Last Modified: Fri, 19 Jan 2024 03:17:37 GMT  
		Size: 35.4 KB (35352 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.18` - linux; s390x

```console
$ docker pull redmine@sha256:35a4f15d53f987bed042b1aa4bef6539b24f5531386fffbc085c38aa6eba10be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196371094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d22d86270e393f6f9db366003150dbe680e3fb4cf1b32f462f8015a5c876a1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 08:27:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 08 Dec 2023 08:27:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 08 Dec 2023 08:27:14 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 08:27:14 GMT
ENV RUBY_MAJOR=3.2
# Fri, 08 Dec 2023 08:27:14 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 08 Dec 2023 08:27:14 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 08 Dec 2023 08:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 08 Dec 2023 08:27:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 08 Dec 2023 08:27:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 08 Dec 2023 08:27:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 08:27:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 08 Dec 2023 08:27:14 GMT
CMD ["irb"]
# Tue, 19 Dec 2023 17:42:47 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV RAILS_ENV=production
# Tue, 19 Dec 2023 17:42:47 GMT
WORKDIR /usr/src/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
ENV HOME=/home/redmine
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_VERSION=5.1.1
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.1.tar.gz
# Tue, 19 Dec 2023 17:42:47 GMT
ENV REDMINE_DOWNLOAD_SHA256=edf3095746effd04ad5140681d618f5fa8d06be09c47b6f8b615dcad0b753e6e
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 19 Dec 2023 17:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 19 Dec 2023 17:42:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Dec 2023 17:42:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 17:42:47 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 19 Dec 2023 17:42:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3525bf6d67566b913f7eeb140bddc1c60100601a384f027950964feea85b1815`  
		Last Modified: Tue, 09 Jan 2024 00:34:05 GMT  
		Size: 4.2 MB (4235221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbfbe6c0328d323d1da07bfbc9b0c07e2ee59964e45c36d6492d00225520475`  
		Last Modified: Tue, 09 Jan 2024 00:34:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4636fb43192e7d8a7f0ea6a3682ab152c1759cdd0b888fc0831a43a684a289ee`  
		Last Modified: Tue, 09 Jan 2024 00:49:52 GMT  
		Size: 28.7 MB (28693257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0cb6e174887f4e9fa22549353cb1a8570d4d964718270b2ae9564ad271028e`  
		Last Modified: Tue, 09 Jan 2024 00:49:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e77f3376460f7f277660995eb65489cccd6fd94fda5da653a5ce061cce0ea99`  
		Last Modified: Tue, 09 Jan 2024 01:39:22 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfc2012d2d0b6791672991e8a28ef3d65bb978db124bd9a4c9daf580d55b8c9`  
		Last Modified: Tue, 09 Jan 2024 01:39:24 GMT  
		Size: 86.7 MB (86684032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c242f4b7d07e3e7bf75522620b571025329ef38396b0ede055f74800ae124fe`  
		Last Modified: Tue, 09 Jan 2024 01:39:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664bbf71b3bc7d6f9e52e6115e6cff59d4002f977e9dadaf65cc642858eaa8b5`  
		Last Modified: Tue, 09 Jan 2024 01:39:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34486cecfeff2a5575cf766d0829f63793bb35e68ec92957647a2f32b6935278`  
		Last Modified: Tue, 09 Jan 2024 01:39:23 GMT  
		Size: 3.2 MB (3236719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff0b8726b15b82bb3b7b1c6f077e0525705f6945ac02f5d8ddbfb261a5b1c8a`  
		Last Modified: Tue, 09 Jan 2024 01:39:25 GMT  
		Size: 70.3 MB (70300602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56140195cd5ba6fcbc5832e7adab83b3efc10848d667a13e921d2756b4b4a464`  
		Last Modified: Tue, 09 Jan 2024 01:39:23 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.18` - unknown; unknown

```console
$ docker pull redmine@sha256:3e81d481af0d282e1c1192dbb87138af654635eecc34f7ca75802ea8d7e93f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4600584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3197946962f17f1e22cd18214f5f11391231fa1572a358a7983f33bdeb86b9`

```dockerfile
```

-	Layers:
	-	`sha256:c8029b4eeb19f1a4cd82d1e3560c42367b202e4aecbe9582dd77b4e67e850053`  
		Last Modified: Tue, 09 Jan 2024 01:39:22 GMT  
		Size: 4.6 MB (4565617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adb90556430f0d1555ff6429948eb0548f71e36579154361728f1ad747919647`  
		Last Modified: Tue, 09 Jan 2024 01:39:22 GMT  
		Size: 35.0 KB (34967 bytes)  
		MIME: application/vnd.in-toto+json
