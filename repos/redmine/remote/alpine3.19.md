## `redmine:alpine3.19`

```console
$ docker pull redmine@sha256:c2c64bd19d3721148d1546f0b7105d33e6ae64627bd831c4ec91c2c4d2228ce1
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

### `redmine:alpine3.19` - linux; amd64

```console
$ docker pull redmine@sha256:85d9b11c76fd5dc25fe415b368170f8b02cc93f42389bfad226784aee3f904d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191414956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537f1f2bb067a501c3f6b47467d1d786e9fcb0eb41fe37553ed1dc7affab1cc0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18e5b612786d49a2d300b60f28986cd04d4cffed62c9c9e7a802b087049e450`  
		Last Modified: Tue, 12 Nov 2024 02:51:28 GMT  
		Size: 6.7 MB (6676626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8142a4b1672020f371b5f13b5ce8240e6950cbb9aacfd36be39b1b4401e018`  
		Last Modified: Tue, 12 Nov 2024 02:51:28 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5bc242fcbf6ae8f342c4ef6e26ad0d0b42c949610b3a7ea6e145067024b4a8`  
		Last Modified: Tue, 12 Nov 2024 02:51:29 GMT  
		Size: 35.4 MB (35393091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f91d0558adf22180c548eabbc807a2112876de71700807d700a20cced28d2f8`  
		Last Modified: Tue, 12 Nov 2024 02:51:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaf99778124150f15cf02013e2dce5006e34e85ab487b627f0778d92aa278c7`  
		Last Modified: Tue, 12 Nov 2024 03:21:35 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceffe1e173a6a6abbd5e5ab4ca606539dc8cb974700ddabaf513f09611bb5ec6`  
		Last Modified: Tue, 12 Nov 2024 03:21:37 GMT  
		Size: 71.2 MB (71199488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c4be61eae9649f421aef3b6d15d1136e100ada9cd91ca6df023dc34565fc7`  
		Last Modified: Tue, 12 Nov 2024 03:21:36 GMT  
		Size: 1.2 MB (1205520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4145b3a02966e21c152829c463043d665d325727ea5f227d1e3ffd8d2d8ef9d`  
		Last Modified: Tue, 12 Nov 2024 03:21:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cd6562b2a296d2a44ffc6e8be0fe3697d96a029b92710fba3ddfad3acaa876`  
		Last Modified: Tue, 12 Nov 2024 03:21:36 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d423fa62974afffbf69944775b58d24658f40fe8914c2cb5cab8b2b4ebd833f0`  
		Last Modified: Tue, 12 Nov 2024 03:21:36 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc26dff475ce6591d2ebbf9bc4225780c8ec77ab09989188270f1b42162b870`  
		Last Modified: Tue, 12 Nov 2024 03:21:37 GMT  
		Size: 3.2 MB (3248965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2b88bf58a523ddd15ab1a0aa5b73db37a99515ecc9e5890d9dc028518760d7`  
		Last Modified: Tue, 12 Nov 2024 03:21:39 GMT  
		Size: 70.3 MB (70267599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644bfbfb9c3a3be9cbc16de0b00ee2fb9366c5ad5158924d867a71e0a0419d4b`  
		Last Modified: Tue, 12 Nov 2024 03:21:37 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:4bec632730ba9e0ec96ed91959773abf9a644b737f9df0aa2cb6b2e67a529314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09e108ba7ed42a06ad4b78bff42cf8eedec3dd9dd0ef5fc78b0befd3b7c7933`

```dockerfile
```

-	Layers:
	-	`sha256:e86a6a76c2398b74573e25b0971a5dea39006a45ffc8f8dc2af357738b48783f`  
		Last Modified: Tue, 12 Nov 2024 03:21:35 GMT  
		Size: 42.2 KB (42218 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; arm variant v6

```console
$ docker pull redmine@sha256:0e940990964c9481d991eba6ac5afb204a9bea81c84b67b40ea1898668362f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183000844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84430ef60469a5bd242573faf3b0a7f8ced6a1368ef63096597a502a12afdd11`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f08ea3601d5a1781cef5e4c363759ed7e5e73dc317c612b0ed98f9e2095192`  
		Last Modified: Tue, 12 Nov 2024 15:11:29 GMT  
		Size: 6.5 MB (6527579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77891824d7c35d244969c467fc44021077184266584502d6d960c90019ebce72`  
		Last Modified: Tue, 12 Nov 2024 15:11:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90075293fb494fb57d064151720fc3ce948822e26556eef9d54afa0aa9db7cb9`  
		Last Modified: Tue, 12 Nov 2024 15:25:23 GMT  
		Size: 31.1 MB (31111063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfb6461cb91c5dc57e11907bfc196429b39871d8b60f3a8c22a8f7d6a7a4104`  
		Last Modified: Tue, 12 Nov 2024 15:25:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0168ed6621be2722b10293a51b887cd6d6f8c3858f8a333e71bc22e277b3839a`  
		Last Modified: Tue, 12 Nov 2024 18:07:47 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137dddcdae3418a12cb4789e6d0a4ef9ef9e3e95dfd0fd673630c7226c93660e`  
		Last Modified: Tue, 12 Nov 2024 18:07:50 GMT  
		Size: 68.1 MB (68142182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61600f4b2ecef1d02c165ab7f9be989485d9070a2114244b39f4cc891c5284e`  
		Last Modified: Tue, 12 Nov 2024 18:07:48 GMT  
		Size: 1.2 MB (1173539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec24e25a896069fdf00d7d9c0a1b2b9b6f0a841236ad310912a030d19a2c47f1`  
		Last Modified: Tue, 12 Nov 2024 18:07:48 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9473a2eacdf6b7bd108ed872ad8bbf7c114662bbeea0d843b8450e3806460c6`  
		Last Modified: Tue, 12 Nov 2024 18:07:49 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0321d928af203fb1032430c2125e0ebaad476e17e518c2b4ec55b46c96260a04`  
		Last Modified: Tue, 12 Nov 2024 18:07:49 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db2c75b073b1069fbdbfdcfb4de5b9d894207ffd5afcfaade018dd067e0b665`  
		Last Modified: Tue, 12 Nov 2024 18:07:50 GMT  
		Size: 3.2 MB (3248709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fca624ec2fd3e739294086bf3c53c1fad82153f1146311906848920d2cd91f`  
		Last Modified: Tue, 12 Nov 2024 18:07:52 GMT  
		Size: 69.6 MB (69617401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232efd72e3dad5ba6eae5ac62304026bd3ddf7e1875af652751462ae4e1a920a`  
		Last Modified: Mon, 04 Nov 2024 22:10:41 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:f4117ebd52a0c42a0261ee96834fa02860a286ca168ad6500edb2487181370a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 KB (42372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7424e83e78b30b32bb4270918c2444cb81410a0eb038961cda719d311dd6e5`

```dockerfile
```

-	Layers:
	-	`sha256:746575d801ce0c6f84337fe201c3e896c8fd69cef9c5ad31599e39ea8640ce84`  
		Last Modified: Tue, 12 Nov 2024 18:07:47 GMT  
		Size: 42.4 KB (42372 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; arm variant v7

```console
$ docker pull redmine@sha256:6749de54d9e138e1cf8dad1376583b71d7b6a6cf27600cfc031f1e2b5779e33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178665158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f4dd648b88da463a6502a883b4ee4f2ac4d7d43ba3ab0bc4932d3c3ddfc634`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:02dfd5e2e7e47e8d8f9020a0d7f4d8240d6646afc6a52b168c0899bc0c3d06a3`  
		Last Modified: Mon, 09 Sep 2024 07:03:23 GMT  
		Size: 2.9 MB (2927731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8157160dc050b6c4bd3c17ce2232a293211e4a1cabc1ba9dd5ef82a951f2d42f`  
		Last Modified: Wed, 13 Nov 2024 06:13:49 GMT  
		Size: 6.4 MB (6369570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d6de3aaf88434cde47a7e1940152023d4b13076c5a307728be576b2f5d1d78`  
		Last Modified: Wed, 13 Nov 2024 06:13:49 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa41a507c2652f61c30f7d5c941c96fe81db6f2a7daebcaaab6f59c9436383`  
		Last Modified: Wed, 13 Nov 2024 06:33:45 GMT  
		Size: 30.9 MB (30862899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2e1f29237595ab91d5cecfbf41f5f43a9d86049a154dbff223f402860edcac`  
		Last Modified: Wed, 13 Nov 2024 06:33:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b8b0d0bf88fa4f1ff272f7457ccc99f92bb494f9bf990e4fce3610f566a795`  
		Last Modified: Wed, 13 Nov 2024 15:08:11 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e523fa3e62058d6206b38973b73e64b4609a03ad2d4ee710def4a5edf48d30`  
		Last Modified: Wed, 13 Nov 2024 15:08:13 GMT  
		Size: 65.5 MB (65464345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17441451a344e493c90a3ee13101056f43ab17bb4072a4b8ad59d77b4f8fa64`  
		Last Modified: Wed, 13 Nov 2024 15:08:11 GMT  
		Size: 1.2 MB (1173518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613ba943e8ca65a0bcf15ff916c4e3120f3b56c744ee4c0d4e3170998b6f8356`  
		Last Modified: Wed, 13 Nov 2024 15:08:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014c9d328d1300b37dad2139b42b1d204b1a865a276c7eee57fdca3892fc574`  
		Last Modified: Wed, 13 Nov 2024 15:08:12 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2ef2e27ccee76747cdb477513b105b977a305d8cdbdedfa88c75701bf51e56`  
		Last Modified: Wed, 13 Nov 2024 15:08:12 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2771eec1e7a822bb9fd4d06865e6490b3a0394c578f288311cf3b8516a1cb5`  
		Last Modified: Wed, 13 Nov 2024 15:08:13 GMT  
		Size: 3.2 MB (3248970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4d4b34baa8cf1dd10d962a938cca50edf9f1d4c40e404188b2c4386f3e8c86`  
		Last Modified: Wed, 13 Nov 2024 15:08:15 GMT  
		Size: 68.6 MB (68614187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4516d19f114927d93740230248424b51562e23c03ed6e21f21fe48d66ad88562`  
		Last Modified: Wed, 13 Nov 2024 15:08:13 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:0a5f33902cd13397c45128d5b2ce24f3b5fa22e90d9a705b607816793486ff45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 KB (42372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75128a13171883fbb0d0c70c730a0dc0cd56374203014c63390475dd07488bf`

```dockerfile
```

-	Layers:
	-	`sha256:f389e2fcaf72cfdafe67c0b691c380eb93377382d485e3c8b5a72caf03e3e0ca`  
		Last Modified: Wed, 13 Nov 2024 15:08:11 GMT  
		Size: 42.4 KB (42372 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:f640822a96eba5f5cca410d96058574fc7347b7879993f7510d0ef6712f283cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191866120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db05898cb9ca04565e03fcfa663c7eb6ba01b9c9cf273dd59d09f717a915ce73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7932c9115c34fcb74d38afbced45febc31052d4263b74dcf1ca706c2c2b975ee`  
		Last Modified: Wed, 13 Nov 2024 00:03:39 GMT  
		Size: 6.7 MB (6741414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482dc4bcc67843a569f39cfac0000826b3acaf91a693052909bab3ab27241487`  
		Last Modified: Wed, 13 Nov 2024 00:03:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f627fd250f5f9feeeded6c23f84ef898a138b1c37c8990e31d2387c6086791cd`  
		Last Modified: Wed, 13 Nov 2024 00:22:11 GMT  
		Size: 35.3 MB (35343776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa84fe5b0ef14ab53453c316cbcf082607539b6ae7de17fa30043d896159b3f9`  
		Last Modified: Wed, 13 Nov 2024 00:22:10 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7973c56253ec12d250c0d0e9af43d161c421bcddc86fda35b2580253c0508a`  
		Last Modified: Wed, 13 Nov 2024 07:45:28 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4d1d19e6241bd4d7c35f6fd330ccc53556ddd80aa85192864e89888785dda5`  
		Last Modified: Wed, 13 Nov 2024 07:45:31 GMT  
		Size: 71.7 MB (71684427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df097e8d4181efeb709f7b872c4ab542542a8d5bcea823470a03d15376ff1691`  
		Last Modified: Wed, 13 Nov 2024 07:45:29 GMT  
		Size: 1.1 MB (1135596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c667e584950b2a4571554fa6490793c7826f1d7aa329be39874969b27d59e8c9`  
		Last Modified: Wed, 13 Nov 2024 07:45:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac0deafde2c105cc3f0b21e7512bb4c1e760b187d673939b28e0b45bda50aa7`  
		Last Modified: Wed, 13 Nov 2024 07:45:29 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194d28583707ba7331bdc54417b60236c24773552ebad83fd9ee5129fc659631`  
		Last Modified: Wed, 13 Nov 2024 07:45:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc325a878cc3ceb7c764974754cc1e2768abff19db9e2a2531b97fba188c035d`  
		Last Modified: Wed, 13 Nov 2024 07:45:30 GMT  
		Size: 3.2 MB (3248970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52981530441296349bd4296c6c8e81536f897b581d76b5468347dce14cf69a9`  
		Last Modified: Wed, 13 Nov 2024 07:45:33 GMT  
		Size: 70.3 MB (70348751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cfb25e3dc8484b9ce49c59ad82eac7f985ffaa1b2623eb86f0f130d1ff71b9`  
		Last Modified: Wed, 13 Nov 2024 07:45:30 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:d216b8b904739f88bc36a60cf7fc3eb999a061ded958d33c3a3051099425a89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 KB (42411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec83058ee1da08f8d06a099928d9b1dfb7e16b3b619fbeb3353687094ff173a`

```dockerfile
```

-	Layers:
	-	`sha256:248aed3dfdac76423c67a64413b048b23275a8c72a162bd93cd2ad351125420e`  
		Last Modified: Wed, 13 Nov 2024 07:45:28 GMT  
		Size: 42.4 KB (42411 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; 386

```console
$ docker pull redmine@sha256:dbea4cb26577a0c83d30c01080a242dbf43c53aa39796b052fb0389ed592a7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187661508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677a67805b4670e081b1e5ca2ef559b52b37a1ea77dfcfd7ca28f5d82d4a76d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817edac21bc5265a78e5265ce306261d959dddfab075225697a6a1f6bbb6820c`  
		Last Modified: Tue, 12 Nov 2024 02:51:13 GMT  
		Size: 6.7 MB (6743133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ea3692655dd333384f04762a6a481cea40ebbc438b3c72854545c46d26066d`  
		Last Modified: Tue, 12 Nov 2024 02:51:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe2e2e79051c8b6f34cab58f4478f0bba3e1c26327a9ac6cd5d42ee0c7cfc40`  
		Last Modified: Tue, 12 Nov 2024 02:51:14 GMT  
		Size: 31.1 MB (31125537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2028fae09fa7a787704a2173ea5e5e7671d2231dc56d115b699cbd962fddc42e`  
		Last Modified: Tue, 12 Nov 2024 02:51:13 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2ac71754b2ffc43bc8126cabc52e90d0e0b569a6495ed8c9ac4c7f69be8982`  
		Last Modified: Tue, 12 Nov 2024 03:21:51 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1d91306ee5f50af35a8c2054b25ee3d109d06bf767580eaf22d910cdd0dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:21:53 GMT  
		Size: 71.7 MB (71701863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f8a2b5f651d81df0c6337998949d2537df0c8321b9b322ed1235ef1e5feb4b`  
		Last Modified: Tue, 12 Nov 2024 03:21:51 GMT  
		Size: 1.2 MB (1182486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108459f89da5fe139cdd7267f75de19c2230c85a1c00031a907b83c95d7332d9`  
		Last Modified: Tue, 12 Nov 2024 03:21:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baf613d5df6967dc2ec31ad7d44827ed8b6556d865358097d791e85bcacd6d7`  
		Last Modified: Tue, 12 Nov 2024 03:21:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7554c6e2fdef25190a6de249a1aa9a536d192426db4ce440b0aca762294839d6`  
		Last Modified: Tue, 12 Nov 2024 03:21:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2775db65c1cfcb411e949573d4f6f9668ee4c61828cac27e8f67c4538665a35`  
		Last Modified: Tue, 12 Nov 2024 03:21:52 GMT  
		Size: 3.2 MB (3248985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8880d7499782981abce57dba2ec7466605384a54cc233b094874a756d2b5be5`  
		Last Modified: Tue, 12 Nov 2024 03:21:55 GMT  
		Size: 70.4 MB (70401893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee4c85f62460e8d6f8df1cd38077a6d2bc3ccfb0c51392e8b985695f4abaf28`  
		Last Modified: Tue, 12 Nov 2024 03:20:28 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:2d25800729bdcb43d3039371961b11e0ebf3471c6308ce2fd4b1fa0b4c0e1c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafda77f4c1917f41d63baa5f9b556c1462a68f9e2a62eacf4fb487100fe3903`

```dockerfile
```

-	Layers:
	-	`sha256:e10e33b8c4d2dc251787e738e6942ccf396d8e77233e836e67e48bd02edc7dc1`  
		Last Modified: Tue, 12 Nov 2024 03:21:51 GMT  
		Size: 42.2 KB (42173 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; ppc64le

```console
$ docker pull redmine@sha256:9bc9dace4180c6e5f7ac16353d28c9200eda368490a182fa80d473fda5e5c526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192200803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba33b4f0f0e3e17491b144a8994eb2ca804c8b1b1fcdcc87a002786249a857c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8076ee924defe041a88a414fd56eca298d413a962c86f670234138c61de81ef0`  
		Last Modified: Tue, 12 Nov 2024 14:16:57 GMT  
		Size: 6.9 MB (6903357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e810a61593feaacc85df2139a106caa00b4337d87e8952e646a2b3ae29b1c30`  
		Last Modified: Tue, 12 Nov 2024 14:16:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebebfa48d412e85692506b58f6dd8ee89a416b7c0b10a01341877741957ab826`  
		Last Modified: Tue, 12 Nov 2024 14:35:10 GMT  
		Size: 32.5 MB (32539971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb76a69edfa31d55b022d20587f94e601a255044738ec1d1bf38f945e863ce2`  
		Last Modified: Tue, 12 Nov 2024 14:35:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd3f46b70cd3380c6a06551d21fe6722f6f648047c973af8bfa2beb288c6a24`  
		Last Modified: Tue, 12 Nov 2024 23:43:48 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faa17140bd69b081755df3d8eae374de862679e14097afb9a12ed1130d62970`  
		Last Modified: Tue, 12 Nov 2024 23:43:50 GMT  
		Size: 72.8 MB (72816655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0217c1757f583e5cd3e2d09c91fa5a9da9122545dde7a67abd868c686bd87962`  
		Last Modified: Tue, 12 Nov 2024 23:43:48 GMT  
		Size: 1.1 MB (1123279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e74bbac7e62f415f09c983dc48f30e95d251bdf0c603cea461c83d70b7ea4e9`  
		Last Modified: Tue, 12 Nov 2024 23:43:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20dcd945d3b345c1f267739eefb69c2556cdaea985cdff7f60bb63e2423820c`  
		Last Modified: Tue, 12 Nov 2024 23:43:49 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808c0fa676ee1cb970d98b0dc260214c8dad8484d62a5444f48d0f75b9536091`  
		Last Modified: Tue, 12 Nov 2024 23:43:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74672e987af808773e9d7fc8e2c8473ce29d174ec708594f3bf929b50e6d13b`  
		Last Modified: Tue, 12 Nov 2024 23:43:49 GMT  
		Size: 3.2 MB (3248995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9af8ab32730cf1ea197815998a4119b979bc4d3b5ea1a77dadc764a8a5f6310`  
		Last Modified: Tue, 12 Nov 2024 23:43:52 GMT  
		Size: 72.2 MB (72200097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e12f502c6778e5980b4dfd14adebd31cc8b3ea690780d7b224a697c5f4629`  
		Last Modified: Tue, 12 Nov 2024 23:43:50 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:b90eb071a2ae98839ebf5fd5945c511470c2579f1c5d5bcd681e41b6b51738fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 KB (42273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11d46193090f2c559d87ca19d447c9de07ee6ef26ccb52f3c7eef85f2e8d9d6`

```dockerfile
```

-	Layers:
	-	`sha256:226309090525e691bb1bd0ef73895597d99c09d7481b010a7c07868f20c7f4c7`  
		Last Modified: Tue, 12 Nov 2024 23:43:48 GMT  
		Size: 42.3 KB (42273 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; s390x

```console
$ docker pull redmine@sha256:66846fa0e411512856239310343d7b7363d824591f0581ea5af4ec093e46b973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190533323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f027728e346b0d810265ff0b5446be82b806cf837844a5f26da908ec38a3938e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Nov 2024 03:38:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a05c55475a41d5f9943edb8c30d37d9f856a98e6fcde5b62c8ebf6dde0923d8`  
		Last Modified: Tue, 12 Nov 2024 21:40:35 GMT  
		Size: 7.1 MB (7051878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f45b7631e24d14b96c75ef9b46f24cee40599eb727dfd8910c6cf2943ecb75`  
		Last Modified: Tue, 12 Nov 2024 21:40:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3339c8a244e74a53a88f482026d81eab1e6ffe48cd42d7c51351e65b944e8f7`  
		Last Modified: Tue, 12 Nov 2024 22:06:36 GMT  
		Size: 32.3 MB (32285181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff45577b8f8dea03a747bba573304f096f98439d07853f2b1e89e67309641b4a`  
		Last Modified: Tue, 12 Nov 2024 22:06:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0649af8402146051e8cee3ee7f79e28c585028a027c24c36e94bd7808d63561`  
		Last Modified: Wed, 13 Nov 2024 04:01:56 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e73c8a495891daf462e9b19872472ebe843f56e50fca9a0e71cb7a6e188079`  
		Last Modified: Wed, 13 Nov 2024 04:01:57 GMT  
		Size: 72.1 MB (72061215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3aec5dc9ca4c11cb43eb4eca95366501894749aaecb0617cdaef81f49094ae`  
		Last Modified: Wed, 13 Nov 2024 04:01:56 GMT  
		Size: 1.2 MB (1172758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6356b91d88a263c0e5ca89de7c155ef5f529ed202d10a8fe6d740e18804b0f`  
		Last Modified: Wed, 13 Nov 2024 04:01:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63f4bb898555ccc2f0b24b7a4110e96d2e186c73d7cfdfcf74258375f29d035`  
		Last Modified: Wed, 13 Nov 2024 04:01:56 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dff5efda902cc76102d0d1be2ef17493e5e760a8d1620c0e75547798c53d294`  
		Last Modified: Wed, 13 Nov 2024 04:01:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c4d63094b4261cd7971367b78e5fd3d6712990cc23ea06e75f9ab2a1b71619`  
		Last Modified: Wed, 13 Nov 2024 04:01:57 GMT  
		Size: 3.2 MB (3248973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ba7659d5363784978ae699ce9a3d88c81d3d5b970704b871b94e0ab660dbee`  
		Last Modified: Wed, 13 Nov 2024 04:01:59 GMT  
		Size: 71.5 MB (71455980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677180dd820940f0b643067343033659bab8c56d5c0a32358c57c99c30d60e2e`  
		Last Modified: Wed, 13 Nov 2024 04:01:57 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:fd5281f77d557c7ddf161b5b1206b33f0fb5edabfb8eaed2d5cbf21c2a338a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1a93fa0648a108272ab7d8d84f37f49a7ff10e7c5fd7bcf13ad64ff653eff8`

```dockerfile
```

-	Layers:
	-	`sha256:375d60c6a23d2f15d76205efdfcdd0ebdd52ccad96caf1e098d7b0c5f6b445b1`  
		Last Modified: Wed, 13 Nov 2024 04:01:55 GMT  
		Size: 42.2 KB (42218 bytes)  
		MIME: application/vnd.in-toto+json
