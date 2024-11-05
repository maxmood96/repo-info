## `redmine:5-alpine`

```console
$ docker pull redmine@sha256:cd7a3330def70b0a50b5d7e40a8652aa22c4adfbf9db5a9b7f660f80b883da37
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
$ docker pull redmine@sha256:1c53e9067875e272ccc20fcad6434f762cf982e59cb242380f492ccf13ffd4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189074806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cb57e8f2d23022830d7f937e9c9b154bc7eb5fa3b3212dc9af8c35cc1ae95f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
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
	-	`sha256:04ac95cfcc9b323c6aa370471fa6c614988dda9aa054b158a6b4cfd72c32b81c`  
		Last Modified: Mon, 04 Nov 2024 22:08:55 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a14ed7effd057af7b5551b2fa5663abd8451058f09d361310073cf42090637`  
		Last Modified: Mon, 04 Nov 2024 22:08:57 GMT  
		Size: 68.8 MB (68821763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665bb4fb92e1c2e1d8ad569f8760cbd40f8730e4e4b97598eec61cffd69d6408`  
		Last Modified: Mon, 04 Nov 2024 22:08:55 GMT  
		Size: 1.2 MB (1195339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daaac0ad989fcb6182a783cad8ce23259de16f1d83f255945dbabc12651da20`  
		Last Modified: Mon, 04 Nov 2024 22:08:55 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64bde32d69134868341578ffe4e1abf7874fddfb99771b491513f7ef4649607`  
		Last Modified: Mon, 04 Nov 2024 22:08:56 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464ef2431f6d760a8ca42f2efb5a1d7354eb183ab3e5a2395d26712166a60541`  
		Last Modified: Mon, 04 Nov 2024 22:08:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d79f00f4ffa4cf684007e45f2dee7ae8e6290c8fda9459fb28842eabdc0a7f`  
		Last Modified: Mon, 04 Nov 2024 22:08:56 GMT  
		Size: 3.2 MB (3249045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffac3b03e59350dd474d890aed75ae56aa0af2fbc2ea8439e1d04393a8657bff`  
		Last Modified: Mon, 04 Nov 2024 22:08:59 GMT  
		Size: 70.3 MB (70283670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379283a204b9b55a61dbce3ef342663769b6aa53fcbb02d52f88d73d51fb4b32`  
		Last Modified: Mon, 04 Nov 2024 22:08:57 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:a8d9518eab1d1992f1b9ab4285f96dbcc0a8931faa87df12943919541e29a2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b26f5e2d1c02e64fb69f1bdc624c3c92ce622dc91698a925d9bcc8c92af9841`

```dockerfile
```

-	Layers:
	-	`sha256:72b51a818126bb69f0810520a3b9aa9748c089d8c4e9689d2fa5c58870709c5f`  
		Last Modified: Mon, 04 Nov 2024 22:08:55 GMT  
		Size: 43.4 KB (43433 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:abe196fde6bc0cba69e06584ca58880ce46a0d3b4f3e0ffaa1e97509bd5afd8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181125072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38d94fc805c6b3fb1e3b94ea7947b36c526af1f16eb90b36fc730cace28169`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
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
	-	`sha256:2d96714b15a561402ba050acf10898bd794259826aff7b3522242e7c8b022bdb`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 3.2 MB (3248924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b74f8f53170d41d736d073b3f3d3a019c76b3143dc89be796b35d83fef7396`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 69.6 MB (69632913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed302813a71d30a89b3c36fdebcd8062b22a9dcfca4159d4bfc93d6766adce4`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:91f1f7984407082731b8c1ef236018253f5441262030b9b9db3dc7a5a8897ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ce2405c4d93d91b2963907ef02b99fbae75669fc3720aabfbe43699b297108`

```dockerfile
```

-	Layers:
	-	`sha256:3ba5ac0313c15daaeee0cd0343d3224c785c31fed1a227da8f06b50365c06275`  
		Last Modified: Mon, 04 Nov 2024 22:07:12 GMT  
		Size: 43.7 KB (43679 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:26503036eced5c1984eb2d25017b2528cdbfa09e8ea8da856e9fd3f69c19d7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176654404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc536b2cdd712b1c07af5a28ffd21de3366b390919a42178a78e1b8a61fb00bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
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
	-	`sha256:be1e6237dea76bd9ff5258d3362572e30dfeeb75d25d7fa6859a352d3cbddb75`  
		Last Modified: Mon, 04 Nov 2024 22:59:04 GMT  
		Size: 3.2 MB (3248983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b2e3369ac77e92a627e28615f780055d71fbe687c8024459085ac5b0d26734`  
		Last Modified: Mon, 04 Nov 2024 22:59:05 GMT  
		Size: 68.6 MB (68635714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52dcd515cdba9f646ab4f1285a6669f1a53d6c063e9c10ab5ee1b37d13e0dbf`  
		Last Modified: Mon, 04 Nov 2024 22:59:03 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:4c4dde5fa8252c110754f390a3c85914593fed2ab27c6f6a5d013bccd45a46ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf94f40cdd98f85ba0ea8a08313b16dd466c81b7fdf1f75fb6fdf859969d28f`

```dockerfile
```

-	Layers:
	-	`sha256:2f1821730f59a16aa267ddf57ff0e75b788a4a6198304a228e28e6b1100c4cdf`  
		Last Modified: Mon, 04 Nov 2024 22:59:03 GMT  
		Size: 43.7 KB (43679 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:625f20d3488c0fd1d8e8b92fa189aa05b60cf880f8644ff5f8fd09687faf5f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190530810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c739dda763bd44b80fc098b7dbe03805ac0be4f678caad50f5d29da766de742`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
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
	-	`sha256:88a1abdaf3298c81059c18003c8c53c6c0191b6e644853fc6ea53bbc9ae8ebc6`  
		Last Modified: Mon, 04 Nov 2024 23:17:32 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155d9e541e93ca5244459a604c89e786ef380bf7f79a43803371da14cb0c48bb`  
		Last Modified: Mon, 04 Nov 2024 23:17:35 GMT  
		Size: 69.3 MB (69308187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4734cff3ce3c64ed51f9a14bababf472a69c750bf1bc93c082796adedf033ab3`  
		Last Modified: Mon, 04 Nov 2024 23:17:33 GMT  
		Size: 1.1 MB (1121086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1723ef4f21461bb5c4af36be1050d9f034645fd8140c85d2584d95eae1f52f82`  
		Last Modified: Mon, 04 Nov 2024 23:17:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e315e68a6fbff858e6acaa2017c0a97cec77c6712778ab5ed95e5986467c06d`  
		Last Modified: Mon, 04 Nov 2024 23:17:33 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80bc5d8afe49f39ab9ccc85a4786fa731dcd04f9b1bf064f6dda4131c9dd35`  
		Last Modified: Mon, 04 Nov 2024 23:17:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f366a4d60af51561cf72c96a54509eba1b0f9184690f7a6f3ae133a7e489b4b`  
		Last Modified: Mon, 04 Nov 2024 23:17:34 GMT  
		Size: 3.2 MB (3248976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1569109ddc12b5dec3475ac16dce2c5211a912bb772f1ea980464306adefd2`  
		Last Modified: Mon, 04 Nov 2024 23:17:36 GMT  
		Size: 70.4 MB (70365970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9411373ce9eee48d8a52b9aaa1e5b1be103329e20fbd7cbc113d5ac4b0ba1008`  
		Last Modified: Mon, 04 Nov 2024 23:17:34 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:ff4c56ea6bd45a9760cbdddf829fc33cdb7437c944405c70e1f828cddae9de9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9107d95baf36f4c5209eb62d076207acfceb7846a0f82a49cdb8c853cc17a3b5`

```dockerfile
```

-	Layers:
	-	`sha256:21171c8e9bad5dc8ff27d9c9776b30ef428fd44f956d2f121306b54657373569`  
		Last Modified: Mon, 04 Nov 2024 23:17:32 GMT  
		Size: 43.7 KB (43735 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; 386

```console
$ docker pull redmine@sha256:59e3364004420c1ec34df186f4f2918972e381b5adc4a6ed5e88bd99389c177a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185867278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe1fe64e8ca2b6606fe8f224298ee6b19d54d49dc7c12cd1d0f181ad913d05c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
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
	-	`sha256:2dcd113bf11f713d38a7f2e2c788fb3a1af1faf01f92b2d16c473144d8363b96`  
		Last Modified: Mon, 04 Nov 2024 22:07:37 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcac2042f22a09e087d891aab1124def8444476cbdbda667b12e387fda9ac787`  
		Last Modified: Mon, 04 Nov 2024 22:07:40 GMT  
		Size: 69.4 MB (69397558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b46bd8c3a9113ce6a3b2179bb47f93eb065907a3a514f7940d712a041e467d1`  
		Last Modified: Mon, 04 Nov 2024 22:07:38 GMT  
		Size: 1.2 MB (1170569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d930db4786f90cb1b22fd67be136749a19b577c29ed764dae32b9f9cf4b6d37`  
		Last Modified: Mon, 04 Nov 2024 22:07:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f0ccd28c99e2e000bb746d48bb2d31ec5897abdfb1102731dc15fda3c23f14`  
		Last Modified: Mon, 04 Nov 2024 22:07:38 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3aa3f26b7a61d6b77ec3d1c3aed0598452e601388414edb606ca7f0c108866`  
		Last Modified: Mon, 04 Nov 2024 22:07:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34dd16f881621bbe7e58e09e219ddd8718461b74a748c600d9f5c720038e06`  
		Last Modified: Mon, 04 Nov 2024 22:07:39 GMT  
		Size: 3.2 MB (3248926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8033f434cf1ff4b62b87ccc5aa3228c83ee2d01ed0842e43cfeeed3216aa83`  
		Last Modified: Mon, 04 Nov 2024 22:07:42 GMT  
		Size: 70.4 MB (70437715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e91f6f9355f95f1c89cac776084def3854424996106cb63e5c23d30ef661ae`  
		Last Modified: Mon, 04 Nov 2024 22:06:58 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:c5140a86b9d93b99925cea221542ccfe6f4c0894acd7a5b2b98c493968db37cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ec5b174ef32265ad13b46834f0cdbbf21a28a609e2626365284acd42fa6447`

```dockerfile
```

-	Layers:
	-	`sha256:75058d15b89f12fa70ba78624c0c670782793357b31d79b74c8ab8cfcc0e92af`  
		Last Modified: Mon, 04 Nov 2024 22:07:37 GMT  
		Size: 43.4 KB (43369 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:faf3fa9731eee0dfdc073a2de9fdfe086ef5b9c6bdb5a20d1dcbfbd7fddcf002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190264830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147985a248d391e75b9692287e0df593d684e0a96ff01e1bea7f9a8cd5be3e41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
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
	-	`sha256:a2b73b3e210a068b142a52872b30772fa34dfb061b6c4d54ac2e01cadda1712f`  
		Last Modified: Mon, 04 Nov 2024 23:36:35 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25f995f26bc2a975a0ab81f411fc0bb602c60171af38e2d5d43b0f33aa4f3c1`  
		Last Modified: Mon, 04 Nov 2024 23:36:38 GMT  
		Size: 70.4 MB (70404783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3977164e6ba1b6c172c1970f097c0f15531c8795fefc79f9b5fe2ed178e21d99`  
		Last Modified: Mon, 04 Nov 2024 23:36:35 GMT  
		Size: 1.1 MB (1111549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc31d2f002a58da629af2e8f4b2f0b372cf25cef86dadd377a43e3588a860315`  
		Last Modified: Mon, 04 Nov 2024 23:36:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d624b84f7ea543fdad7843d0f355208ff54fd25ce26f43093b47ff5a51f4fd5`  
		Last Modified: Mon, 04 Nov 2024 23:36:36 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d01c463228876350889d4d7f8b412148b0abec9cdc80be87ed7daf8a5c0fd`  
		Last Modified: Mon, 04 Nov 2024 23:36:36 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483aea5624797e6aaabe08686d05f676991e4693e3c9b9dbc9e80c2656047fe3`  
		Last Modified: Mon, 04 Nov 2024 23:36:37 GMT  
		Size: 3.2 MB (3248963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b0f5bf0c078426e0fc3f230c9f510c65c50d89161af53bdd60fffdc251bef2`  
		Last Modified: Mon, 04 Nov 2024 23:36:40 GMT  
		Size: 72.2 MB (72213075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d3b0d0c79a6a8738baf50742c62260b755df06b6a1f01a0ca33d94190c03fa`  
		Last Modified: Mon, 04 Nov 2024 23:36:37 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:61e7a59d72bde54b4452d64d8d3baac8654cf0a5e11de3c0f4b8ff84596b722b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fe9767190cfb6d69f2416b64f2fa176c1d06d294763ad7d43aa091e7f828f6`

```dockerfile
```

-	Layers:
	-	`sha256:4c62182bb9cbfd5df3d8c1af170691fdb4b1401e36bf6a54730bb1decac260e5`  
		Last Modified: Mon, 04 Nov 2024 23:36:35 GMT  
		Size: 43.6 KB (43573 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:0fbc14497bcaf1fde4a2d9a4c0c48b09d79cc3e3c7bdf589d260264a221a857a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188920829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277c4e9e364c66045022e4227379b8e0eae510c2949cd926f376097bff38b6d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
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
	-	`sha256:432e199cae8cb92cb07da259b910fcb12525a5c2d7383e71cd567e667137cf33`  
		Last Modified: Mon, 04 Nov 2024 23:00:11 GMT  
		Size: 3.2 MB (3249059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff077c6d19761276575f7305ff829f539ab0931f69e6bfe449321b62f4ebe0b3`  
		Last Modified: Mon, 04 Nov 2024 23:00:21 GMT  
		Size: 73.7 MB (73714413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77e09b7b38fd4094742407771c626685e6e9c08aefedbad18254d209f3ee36a`  
		Last Modified: Mon, 04 Nov 2024 23:00:11 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:a4aa7ac037698ece709786c41d6964776f20b7d7e6247f8950e2a7ccd2a78dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33baa5e0ccdae74d845df2d39b16c76b17107ec387d216a3a7ac641af8254c0b`

```dockerfile
```

-	Layers:
	-	`sha256:7b3d153703e9304be0e57cd78a953c01ba5d8874830c1592ef86a22fad883019`  
		Last Modified: Mon, 04 Nov 2024 23:00:10 GMT  
		Size: 43.6 KB (43573 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:d78ebb9adf171412898bb330ea816c269db0d5e94ffbcf6b37792bc710f98449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189452663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7005411ee83ed17d50887efdef09a8b5c5132f0637060264301f465d25f6822e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
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
	-	`sha256:7546787e93d5103d5926f97e1ccc215dfd33c4e7cd227aebcc1787e543b99754`  
		Last Modified: Mon, 04 Nov 2024 23:19:55 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fb1324260ba2e38e0e6dc769ff51ac0db6c777c47ec5670d67060bf6b56ffb`  
		Last Modified: Mon, 04 Nov 2024 23:19:56 GMT  
		Size: 70.5 MB (70498151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3825730b3e5ffcd343a97c61a5e2367438078bdea81f2a303f4add9fe916f81b`  
		Last Modified: Mon, 04 Nov 2024 23:19:55 GMT  
		Size: 1.2 MB (1160358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cfd324ffdcaf5cb79ee36dd2700e460522b80315c0a4a426fb2a1ee182e3b0`  
		Last Modified: Mon, 04 Nov 2024 23:19:55 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911afd37aaca68e94a7f5a8e26a69e8ec9b5f614b17430d69ea83ed51aabdcb0`  
		Last Modified: Mon, 04 Nov 2024 23:19:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a480933c3fef5e591f81883c20938fa4978489118740dbbfc2d57d55e11a7b7`  
		Last Modified: Mon, 04 Nov 2024 23:19:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e671d4ebdd8664448dbc820aef43ebec430a391dbdf693005cd6b6bea2a9b4c`  
		Last Modified: Mon, 04 Nov 2024 23:19:56 GMT  
		Size: 3.2 MB (3248942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0e16b66bd930c3ce4f370cb8abf000c51027f1f2a420df2c6fca44421f0faa`  
		Last Modified: Mon, 04 Nov 2024 23:20:01 GMT  
		Size: 71.5 MB (71469646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b4e605528fc9f19a6e46f742bfafc6da49da3c219733303871dedba0a933a`  
		Last Modified: Mon, 04 Nov 2024 23:19:56 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:7100ddbbddeac6c67c787a37f8eceae9433fd3087c785c66c7ccf4374621e37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 KB (43493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0fac0ced0b6611bc683213f47a89378875657fe1ff96fcf0ae5a380fa5764b`

```dockerfile
```

-	Layers:
	-	`sha256:b722f3b108e1ea94a91c0ed45da2deaaf9c1397f3b0476cdcf82cdde41ab05e7`  
		Last Modified: Mon, 04 Nov 2024 23:19:54 GMT  
		Size: 43.5 KB (43493 bytes)  
		MIME: application/vnd.in-toto+json
