## `redmine:5-alpine`

```console
$ docker pull redmine@sha256:9dc0f58f020dd3bd54d2b7a5b056412de98d398e3ec8ff04dd635d9e4f31728e
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

### `redmine:5-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:30e30b699735597141c27b4d8b466a62badd1afb2b5e0d3ab197f2a9b673be47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189072905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4f4a37eb14098095b4a4832ed5b7d12c59df767ef5a4327ae1005f18b2f4ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccdbb10be86e2cacde4845b2b5a5c58b70c5cb9dce0033dcba82189188e3c29`  
		Last Modified: Wed, 30 Oct 2024 18:10:33 GMT  
		Size: 6.7 MB (6684093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9507251b29111df6dde99fdf6447842a86e7a27cb3436af8182796700890ed7d`  
		Last Modified: Wed, 30 Oct 2024 18:10:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83af5589cc535e8ccd949e8832439e12afaf2c675d60f194b37e205534ab56a3`  
		Last Modified: Wed, 30 Oct 2024 18:10:29 GMT  
		Size: 35.2 MB (35213425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c1b373be8124ee9d617e8fac95a7bd73b8ff9793873a3751e119236619f2c`  
		Last Modified: Wed, 30 Oct 2024 18:10:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd56855e9c00e77382cbe3f1c4830e5b0629f878303c95aaa75a241946534d6c`  
		Last Modified: Wed, 30 Oct 2024 19:04:06 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92531457b71de53869440cffd4e7d3ba2eb23f6a7b6d6c943e28976f6b7d4bde`  
		Last Modified: Wed, 30 Oct 2024 19:04:09 GMT  
		Size: 68.8 MB (68821911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16da909a29ef1b334360a4f39e3cacc21e79ceb214d6a9c1eed9c6fc078da03`  
		Last Modified: Wed, 30 Oct 2024 19:04:07 GMT  
		Size: 1.2 MB (1195328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2105da3653adc83e6126faef4ba4926d2a08c2697a5912b00d47fea98f64840d`  
		Last Modified: Wed, 30 Oct 2024 19:04:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554792703c37514f5fdfe518d24acace69bf4a3ca2b2dde323bc929a09d67da7`  
		Last Modified: Wed, 30 Oct 2024 19:04:07 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987676d5f305da45edfc07fd55476fa77810749679a0e6ce1a888b77d453916a`  
		Last Modified: Wed, 30 Oct 2024 19:04:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568732c1e0ec42695d09ff5321f3357842d9ebfaa8174912c6191ac2bbbf6baf`  
		Last Modified: Wed, 30 Oct 2024 19:04:08 GMT  
		Size: 3.2 MB (3244110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5926ef9a10fe4c6598b3fce0e069f6ea7a4770694aee43e36d545542b2ea194f`  
		Last Modified: Wed, 30 Oct 2024 19:04:09 GMT  
		Size: 70.3 MB (70286528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1112bed3764e9fecc3441625ead3a66d921696691d18a7260a83e0142d6c3a2d`  
		Last Modified: Wed, 30 Oct 2024 19:04:08 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:bdae52da9d681ede46048982ac3cc7a330f70771428ca01b396b1295ad217668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684a9f7003c4928e7f5d2b65fdcfe0cfd045edf775e58e8f7191a3a58cbe0d18`

```dockerfile
```

-	Layers:
	-	`sha256:ac690f374d975e19551e6b51a9bd28ab4ddbc873937b5205d65b9b11e34008df`  
		Last Modified: Wed, 30 Oct 2024 19:04:06 GMT  
		Size: 43.4 KB (43433 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:9f574957f523d70531f7c7a472d542d126ad60f2d6cb30a30b0e3a0e266246ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181120696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc77c32a1075b2674ac31af7d44a4f640c900bb08aaf434797d1c269a771284d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7482308aeaf448ab510de66c0f7083c3f9f720a77f12ff2547be8a7fe4e277f0`  
		Last Modified: Sat, 07 Sep 2024 12:23:17 GMT  
		Size: 6.5 MB (6531246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac1582ea2b0d99bb913a6f07f9302b8130cf8a529fe6628b8ffd2cc37a19ee4`  
		Last Modified: Sat, 07 Sep 2024 12:23:16 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f067d04bc8564742de24ce91c72a0979e413d43bf5ae7e163a350da0a6975a06`  
		Last Modified: Wed, 30 Oct 2024 18:21:32 GMT  
		Size: 31.5 MB (31529578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a161cee52137c245bd2e28a76f8f0871fb6275556419a030b23cd234ac872646`  
		Last Modified: Wed, 30 Oct 2024 18:21:30 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d01d3e48a691819b97cfe26e2334e7c8e47a50d8d571556833b4bd79f7c0b8b`  
		Last Modified: Wed, 30 Oct 2024 19:03:29 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad3c3afc426de00b6376a801532a55b1bc4d9f4bc8c5d310f40cfac501610fd`  
		Last Modified: Wed, 30 Oct 2024 19:03:35 GMT  
		Size: 65.7 MB (65650135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0d6ad492a54cb34fb9e822c7a975ca6c03bb3c0d86aedd6b99414d07a3b67`  
		Last Modified: Wed, 30 Oct 2024 19:03:30 GMT  
		Size: 1.2 MB (1162111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02aff0a1f038c3abc8dcb2671d03202f8096590a44df264ee0eb41e0d4cfdfc`  
		Last Modified: Wed, 30 Oct 2024 19:03:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dbaa1673f46a0956e9ab64d1c1e7a85a28a4ef455968fee7e5aeab15c14194`  
		Last Modified: Wed, 30 Oct 2024 19:03:30 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6009f343921a951e485ed60f9b4064f580a6f85a3697b381918e74ca24371588`  
		Last Modified: Wed, 30 Oct 2024 19:03:30 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3784d35232be1f486542fbec9e99dcf92749bea4c27b07244ecf864d4c1721f0`  
		Last Modified: Wed, 30 Oct 2024 19:03:31 GMT  
		Size: 3.2 MB (3244146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c8fa0ad68a700eaf7767fe39f266c37521dc9bd8adec3609dd1385af2bebbc`  
		Last Modified: Wed, 30 Oct 2024 19:03:33 GMT  
		Size: 69.6 MB (69633271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dee02d7142aa9f2f0a121f4b5329419fd8168a54f8c55b3437eaccfbfcb22c5`  
		Last Modified: Wed, 30 Oct 2024 19:03:31 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:52aa12752a23ffac7212959f51d53a009f773d1fcb6af6e004c925875739140a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503631f5c55e3de5aac10340a7264ba4a6aa0b6b7f4bca0dc80ed30f4bdd52d9`

```dockerfile
```

-	Layers:
	-	`sha256:8156b86824354cd1ab51b9d647254506766761393cac899ab2fa58e8c3bee4a6`  
		Last Modified: Wed, 30 Oct 2024 19:03:29 GMT  
		Size: 43.7 KB (43679 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:b85caacaaf0f3298e6b9457003d035585c1fb6e81055bbb05b741fb441517175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176647479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc63e607dd97fa174e13faf8421ea500c6d2cbaa7ebe2c932e467d9b5ab2154f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144a0b15b16a5460d2785d5992999e8460241448fbfbaab6e80402384bd6ddd`  
		Last Modified: Wed, 30 Oct 2024 18:43:37 GMT  
		Size: 6.4 MB (6375856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd32429e7ee45fcd9be91e5600c4298cb53c5c6e7e8896af54b2becf86bf65da`  
		Last Modified: Wed, 30 Oct 2024 18:43:36 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dd9a382ec2b56197b00a5aa4286eb7f1b51ea1e092f8f11c112e2e473fca7a`  
		Last Modified: Wed, 30 Oct 2024 19:16:28 GMT  
		Size: 31.1 MB (31075648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af8b095903aea4df942b39e6845720eb7907ed1cc7cac7db06a7f89653bfd3`  
		Last Modified: Wed, 30 Oct 2024 19:16:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dc14435d9dfdaced5e42a6db6c2df59cbe4c6d39e0c6babadae9db90980f48`  
		Last Modified: Wed, 30 Oct 2024 19:59:24 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e14ce41fa56b769de3c9cae14b5af76741441f5969e2e6fd20e73e46fa4a8a6`  
		Last Modified: Wed, 30 Oct 2024 19:59:26 GMT  
		Size: 63.1 MB (63056941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee93da501ad53c23ed1290b0eeea34940fa3ad56569614a8a36154dd982669ec`  
		Last Modified: Wed, 30 Oct 2024 19:59:24 GMT  
		Size: 1.2 MB (1162103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d78dc74ca1f76038b6a34ca06dffdbf0f3c2f191920c6b9ccc64895ec45f185`  
		Last Modified: Wed, 30 Oct 2024 19:59:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25477e25e1d66bc7ab7645eb56967f8344ce77e99fd472391eda22117265c61d`  
		Last Modified: Wed, 30 Oct 2024 19:59:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb38b20f2352a5c2f7e8264c0603a8a37d5f8cee59287502ea83f938c88e870`  
		Last Modified: Wed, 30 Oct 2024 19:59:25 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31792e4f06a0cc4d5d5aecbf7c7440a6a1c87a1b56f6cfdc23bc42dfdc01b12`  
		Last Modified: Wed, 30 Oct 2024 19:59:26 GMT  
		Size: 3.2 MB (3244119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7c676c37e78835ae0857568565909f021a8a6ae1f5e825083b76eae409862`  
		Last Modified: Wed, 30 Oct 2024 19:59:28 GMT  
		Size: 68.6 MB (68633609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0b46efead597b442a41c32ba4f35b5c9c0a88be411b462045e24fdccd5c6ee`  
		Last Modified: Wed, 30 Oct 2024 19:59:26 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:0c609e158de46d6025b416fa573e5404abc53ae8397e9bf4bdbe17feb30f2703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c3c9b9cbf29a3a0a852c286437fa95fefd9fe088f1548e7914930b6ba073aa`

```dockerfile
```

-	Layers:
	-	`sha256:7656fe3d8813922a21d7dbf3127bfb0a0932195631f7fa6be09dcf79d7860562`  
		Last Modified: Wed, 30 Oct 2024 19:59:24 GMT  
		Size: 43.7 KB (43679 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:824a9f741c3f7e507daf948e37b820990bcbc2d5d317b5f2c3fed256d3936bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190522604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2d3228a6c5160ed4ca4cdcef6a07bcf0d7c799024084f3d9a4b02b9a7546eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bd737e2436eddcccd7fa558c2c782925021378c569ea93c4e75d40145c8663`  
		Last Modified: Wed, 30 Oct 2024 19:45:52 GMT  
		Size: 6.8 MB (6750679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06121bcf8320312b8ae004b1f8627d54b545b6ee22f63e7f402e68fbd7ff6d3`  
		Last Modified: Wed, 30 Oct 2024 19:45:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cffb1a0c1a438e3382a9c89709feaaaab730c70cfa533500caf3f4af5fc6c63`  
		Last Modified: Wed, 30 Oct 2024 19:45:52 GMT  
		Size: 35.6 MB (35644602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4285d4070b552137e82f07b33ad073a0f32c69f1e484a2b5fce3d47f45bd80d`  
		Last Modified: Wed, 30 Oct 2024 19:45:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2a61676c632be26365b33ee695953bf0f2ab1d53d1f00c6a3f221d12b7e3b3`  
		Last Modified: Wed, 30 Oct 2024 20:16:37 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f324461d3afb288c8587b63f8ae0a5a22b04b5bb6403bd93e3f2b4d7ac7931e2`  
		Last Modified: Wed, 30 Oct 2024 20:16:39 GMT  
		Size: 69.3 MB (69308065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f9e8083d89f8255b54fb9c43e2fd7c13abfa215d5a40ca426e2520538514f9`  
		Last Modified: Wed, 30 Oct 2024 20:16:37 GMT  
		Size: 1.1 MB (1121082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a7746551dd400a1a5aa06938a9b748ab06e0b4ea56242845a9ffb0b463ec9d`  
		Last Modified: Wed, 30 Oct 2024 20:16:37 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93beae27704789e11c3724b8c15b6e36e6f3fb24c4b9928a921b06db5f95fbe4`  
		Last Modified: Wed, 30 Oct 2024 20:16:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ce038acf6faedc90c7287ecc152cb92e8e2c16f8d072cea1bbfaeea0d5ef81`  
		Last Modified: Wed, 30 Oct 2024 20:16:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7672e1f5b973d9deaf98ae34bfc992316827a34d8909c8f5a43ff9eeae965959`  
		Last Modified: Wed, 30 Oct 2024 20:16:38 GMT  
		Size: 3.2 MB (3244123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fe44af3eab063ed5ead1908ec7120bd720d3750b87c2bc46c763548dd04f0a`  
		Last Modified: Wed, 30 Oct 2024 20:16:42 GMT  
		Size: 70.4 MB (70362704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7d02a30a8eb6f51deb12433c40a14ce3cfe3c9e9e3f2e496a20487da47a94e`  
		Last Modified: Wed, 30 Oct 2024 20:16:39 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:5a02ba0f38c2937573fecb83924cefca63ec39e773cbeb2f450f967363c70cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c48db4dd974fbc2187c871519998fc991f15a0e0f4b2e9af16681127080ca6`

```dockerfile
```

-	Layers:
	-	`sha256:39f3d5cdf5a5175c2f5d59f0dc62455f60f2a67adbd0b7d8ae5ccc0ef9c2bf63`  
		Last Modified: Wed, 30 Oct 2024 20:16:36 GMT  
		Size: 43.7 KB (43734 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; 386

```console
$ docker pull redmine@sha256:3f14cddffe596fab29afcca2ce32ef45dcaf08cb7935be0a9d8d703fa13f18eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185864241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb41f7ff27afb0756092a171b895d41600e0547fca0c296465e47d4138efa4a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401e774aa09c028517a5caf63ff5c660ec34faad2d4dfaeffe149012214478be`  
		Last Modified: Wed, 30 Oct 2024 18:06:16 GMT  
		Size: 6.7 MB (6749350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f014cfe17a98c6309a8ec8827d3a0059da6387650781d23b20ad5724d69324`  
		Last Modified: Wed, 30 Oct 2024 18:06:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9116632f1da3b4b57db5cf260eddc3391ceb3e170237320426cb1534ba36c75`  
		Last Modified: Wed, 30 Oct 2024 18:06:17 GMT  
		Size: 31.4 MB (31390333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f5235f1e9dfb107a488690024df040b0b0c4f8afb6e401ebbaa43f6be3d048`  
		Last Modified: Wed, 30 Oct 2024 18:06:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8853fbb67645300992ae052b534e2688c1869a98ead60e30465b9ca943bc23`  
		Last Modified: Wed, 30 Oct 2024 19:04:12 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa36432dc9954f0553740c17b304bdab88cafc54311192cd41835c6a96c53f6d`  
		Last Modified: Wed, 30 Oct 2024 19:04:14 GMT  
		Size: 69.4 MB (69397787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7338cc78b8a8320621bf09804ce5388ffd1b731ec96a51a946f6c65a07257a0a`  
		Last Modified: Wed, 30 Oct 2024 19:04:12 GMT  
		Size: 1.2 MB (1170571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e3629413724d7fa1e07029ff43e44e744c889c024e036fe718c0a7c5cb6530`  
		Last Modified: Wed, 30 Oct 2024 19:04:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14501cc74f505d766472e0380abf59a81820c3207f35a6e1fb2312c2ad820209`  
		Last Modified: Wed, 30 Oct 2024 19:04:12 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987676d5f305da45edfc07fd55476fa77810749679a0e6ce1a888b77d453916a`  
		Last Modified: Wed, 30 Oct 2024 19:04:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9a8ca165d2526a08dc396c2d1dcfc3fcd9d3cd665bf948f54c0037776965ae`  
		Last Modified: Wed, 30 Oct 2024 19:04:13 GMT  
		Size: 3.2 MB (3244103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f7485d270881492d3dd33cd9115e1f2c7629edb310a2fb0ec1e21d915b7300`  
		Last Modified: Wed, 30 Oct 2024 19:04:15 GMT  
		Size: 70.4 MB (70439228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2168b0d8b5ba6f8b82ea224ed173bd9ccae282a307781560313c86478380aef0`  
		Last Modified: Wed, 30 Oct 2024 19:02:45 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:1dc4f54100a7e365f19700dd72706d0df3534c203bbed932789ceff811b02882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3aae6bbfff2c74fbf594e60b7c44a48f2e111f6c2e12a8a53cccd8957c4ac57`

```dockerfile
```

-	Layers:
	-	`sha256:c3410438684e2a279e3c1a18901de0b8233f0d28da314a7f3bc710a68c1fa8af`  
		Last Modified: Wed, 30 Oct 2024 19:04:12 GMT  
		Size: 43.4 KB (43369 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:e576de9d4bb7d290d859ad9af1d8d4546f5a729465afd508530d2ffddfb14d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190258898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7783dd8a1e6d86c43886cc5d5ab9b0c51ad63cb7001c7dc24d55881416932e55`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32e4b3847e4b4db773ca759fee0fb64b5e18585fc43614f20d1a96ebe122c60`  
		Last Modified: Wed, 30 Oct 2024 18:32:55 GMT  
		Size: 6.9 MB (6911683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327d4fcf0c23e80b9c71ceaaff7941a53660d062094f3525284445b2a64efa9a`  
		Last Modified: Wed, 30 Oct 2024 18:32:54 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036e434fe586a7536798ee7c1cd1eeb170b5baf2e567753fa4da462492028999`  
		Last Modified: Wed, 30 Oct 2024 18:57:43 GMT  
		Size: 32.8 MB (32798694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4abf0daf5131ef9f42089091c2fe3e60a51347f85645e3f2a54a0d9d19d4b5`  
		Last Modified: Wed, 30 Oct 2024 18:57:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b1645f0bd21b2aa90bec24966adf328f10aa51a72950a8abf6d931479cdff0`  
		Last Modified: Wed, 30 Oct 2024 19:30:42 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc4bf113da46664ae6f0fabdd896fcd77f4d17fabc7c3895265f9500efcb95`  
		Last Modified: Wed, 30 Oct 2024 19:30:48 GMT  
		Size: 70.4 MB (70404589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a00333978b247a247801577d89ce463262229d848784e05b1f72d34b404fe35`  
		Last Modified: Wed, 30 Oct 2024 19:30:43 GMT  
		Size: 1.1 MB (1111553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d0967b65b81ae797943e4bf3db18cf90e3d16e4c5b985834609904f06d9678`  
		Last Modified: Wed, 30 Oct 2024 19:30:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580f290317b27b1eb37ba3390143e438c35880208915ab178c5da38c1aaea436`  
		Last Modified: Wed, 30 Oct 2024 19:30:43 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d579f56e2b2394cccaa81d646b048b229247c887474a9b2a0e1939637c5e3e77`  
		Last Modified: Wed, 30 Oct 2024 19:30:43 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4568ea9d558a5d9d25f7f99cc49e92a2a5a37f037d992530465bdb189064457a`  
		Last Modified: Wed, 30 Oct 2024 19:30:44 GMT  
		Size: 3.2 MB (3244141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba40acbcad78036719e459c85020bff95b6d0ed4f805352dd45562b4f62b0c`  
		Last Modified: Wed, 30 Oct 2024 19:30:47 GMT  
		Size: 72.2 MB (72212118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5add5d736b1fdb5efe91274b8dc20376b14ff4f7bbb5966226b1227977389296`  
		Last Modified: Wed, 30 Oct 2024 19:30:44 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:e465f3ee93606d8000ddaac18b23eff25987044e2e406ad2178e4dafb43dabd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63f417f5a9650281d206e7fbfd6ca1b64448fdd226517b68c907713674e50ac`

```dockerfile
```

-	Layers:
	-	`sha256:743a4dabc4ba51e74e81c2a591a3ec1839d3ffc345732011b20a42132ac43709`  
		Last Modified: Wed, 30 Oct 2024 19:30:42 GMT  
		Size: 43.6 KB (43573 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:76bdf199fab3f3efb4eb184cfdc86514c3afd8580a8547f35743eb9bcd5a7489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188914768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e92042e0c50a5af7f87388012acc5da7b245ce34594ebb86a9d990995c1dc5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f415934773bb3279d1e59447161213866d8d558ab1e46978460c059379f097da`  
		Last Modified: Sun, 08 Sep 2024 13:24:14 GMT  
		Size: 6.9 MB (6946838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d825ee7f9e2e2c32f71c97db0bf40f10edca4983062295c5bac56c1e34fbe2f2`  
		Last Modified: Sun, 08 Sep 2024 13:24:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d541197de3679337b26e7808bdb9e80cad77d1eaccb3c307b4b463dd52207f`  
		Last Modified: Wed, 30 Oct 2024 22:30:08 GMT  
		Size: 31.3 MB (31324442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fa328ae5b72ac4f90b6fde1e8cd130a4bf8fbf3cd60329cc44bcb63c7047fa`  
		Last Modified: Wed, 30 Oct 2024 22:30:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03205a67741d656fb8fd7128c032acd6674dfb8ca673da0d9bbd66a69d732125`  
		Last Modified: Wed, 30 Oct 2024 23:54:11 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c027833c1dcb7e1af75d635622017314504d296d0809daef7874a8c4e1311c55`  
		Last Modified: Wed, 30 Oct 2024 23:54:21 GMT  
		Size: 69.1 MB (69147145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04db518277770776cb8b2e5e4084b9a55fcec979dcdfa99bf7121b0dbf98ea1a`  
		Last Modified: Wed, 30 Oct 2024 23:54:12 GMT  
		Size: 1.2 MB (1163819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e242e1859cee5083d9462331eed7d51c419839716e140fe9e202dd2f7c76ad4d`  
		Last Modified: Wed, 30 Oct 2024 23:54:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24aa1646eaae97609c1a32bb12b4dee33b794a8828f15647bd8726a4fd819f7`  
		Last Modified: Wed, 30 Oct 2024 23:54:12 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2e1b4cb5ca69aeea37ec0f1adc9eff05fc7a6c29677037a5048c0a779bf6b5`  
		Last Modified: Wed, 30 Oct 2024 23:54:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf50a7de6e659bf542602a8d0fe4ffda7821185ba686cfe370300fe6d513ceb`  
		Last Modified: Wed, 30 Oct 2024 23:54:14 GMT  
		Size: 3.2 MB (3244321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af17c41b206ed7861442e1668415edaa34423d683230544b663c0627c1daa9d2`  
		Last Modified: Wed, 30 Oct 2024 23:54:28 GMT  
		Size: 73.7 MB (73713047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6804e3d43eeaf00e1a74d76b5bec63c782947de084cafa5f4d48f1468a719808`  
		Last Modified: Wed, 30 Oct 2024 23:54:13 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:4844758e6447b0c20cc4a03df215228706c95b7c68a3d40dd3d590fcd308cff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbe44b0619e8d555676f2a9b7bde135c8c8bdff38d48a790b9f34d6188699bb`

```dockerfile
```

-	Layers:
	-	`sha256:1722930fd65efdbf52e98dcc76014d7652f8eae02767836de33e57eb63dd6c9f`  
		Last Modified: Wed, 30 Oct 2024 23:54:11 GMT  
		Size: 43.6 KB (43573 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:6f508ad4adc4a850f91a35f599c50ec2ad16e2a9fd6b86e78c41c4fb5f6c13bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189448519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55754503d63fa1f6d0fdb47cb401a46b5c7b1537cf14f6d415d348c9557d9662`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aace386700f7519dbe51639ba130b690fd2486da9b9222e5a560c73c7b6ee14`  
		Last Modified: Wed, 30 Oct 2024 18:40:54 GMT  
		Size: 7.1 MB (7061703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190d308936c031782fff1ed3f91769f04fd94a40dd3f441189355cabc7611a9a`  
		Last Modified: Wed, 30 Oct 2024 18:40:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6f475017d3858e4991c95e0f988ab8e92d2ef37c0264a9ff081acaaa390260`  
		Last Modified: Wed, 30 Oct 2024 19:27:17 GMT  
		Size: 32.5 MB (32548605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372fb9412c7936e14e3c78072dd1cf9613c06d40b345a472d4afdbf855e16d6`  
		Last Modified: Wed, 30 Oct 2024 19:27:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f8002dfbca8bb4e2a06f87f3c2d3342f51c88fa9098d6c4fa09685916f76f0`  
		Last Modified: Wed, 30 Oct 2024 20:02:33 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece7fa9c090b868c1d570bfacf0c0b4c620a931f51653a543ff14de96f383ec5`  
		Last Modified: Wed, 30 Oct 2024 20:02:35 GMT  
		Size: 70.5 MB (70498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70dd0e3541a4d8426af777f0f915789ba1944d10b76c9d8f45d0010e5368727`  
		Last Modified: Wed, 30 Oct 2024 20:02:34 GMT  
		Size: 1.2 MB (1160349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5572bf50db0c8193bdb148b087a822d37df2595306f497e35b6a2fff027b46`  
		Last Modified: Wed, 30 Oct 2024 20:02:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19ca859b73fb139e0edda744621165f0e825e9ce3b11814fe6b1b0c11b23ba`  
		Last Modified: Wed, 30 Oct 2024 20:02:34 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd3f637fba9f551659bb60c75dbb4871d1364d04c8252585af503b996bdc96f`  
		Last Modified: Wed, 30 Oct 2024 20:02:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec34f56ba3bd12537fb0ddab6f50e68928d2167a2002c0d770f21d35e698328`  
		Last Modified: Wed, 30 Oct 2024 20:02:35 GMT  
		Size: 3.2 MB (3244091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5023eceb37906803acd5ddaeb55fe62c1d215c5d740d97298a230cfc06c486a8`  
		Last Modified: Wed, 30 Oct 2024 20:02:36 GMT  
		Size: 71.5 MB (71470110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb5a18b27025fb22ad08b9c21e307edc2b504ef2f0b1bdef0a71d575417f1e0`  
		Last Modified: Wed, 30 Oct 2024 20:02:35 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:62218fb8233fb8fb96f43df1fff320d603d502df266b73922d56f75de255e0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 KB (43493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecdd8f6a910eb4e64fd923b1b788e935c11b2bf34942c1e87edb6ba405aa9e4`

```dockerfile
```

-	Layers:
	-	`sha256:825896c01fc84da48ea8897b102dda48ef1a0ac1a0373ffc108d601aef00f66a`  
		Last Modified: Wed, 30 Oct 2024 20:02:33 GMT  
		Size: 43.5 KB (43493 bytes)  
		MIME: application/vnd.in-toto+json
