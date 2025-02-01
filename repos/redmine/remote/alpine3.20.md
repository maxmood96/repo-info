## `redmine:alpine3.20`

```console
$ docker pull redmine@sha256:625d936674b396c2382f14621e0d14e29b29bde84673aa3972493a102839b9aa
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

### `redmine:alpine3.20` - linux; amd64

```console
$ docker pull redmine@sha256:07ed58af48c097e87ec6162dbcea37a05365e9557a68aaa54860421a334a3a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187943977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f6720607f50275a79b53501f5d17135146d22fca87e158e933599f7f3b07c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af9c474b1fd911043d5c0089a9b2dce8b573658542791aeeb75b0b028d48395`  
		Last Modified: Fri, 17 Jan 2025 15:31:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bd4b4e7686c356482cbd8bd4d6cac57b05a11b30f5397850c8ce966564c962`  
		Last Modified: Fri, 17 Jan 2025 15:31:37 GMT  
		Size: 35.3 MB (35284503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a356c0021182c48aaea4a6fa39834747cd22d62fd5604f7654cf9852a0d285`  
		Last Modified: Fri, 17 Jan 2025 15:31:36 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b32b5da3dce3863c044521b382ace0242cc9ce2a2320ede57bdc55d2f5b66a`  
		Last Modified: Sat, 01 Feb 2025 00:29:53 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1515bb1d37dc1443aae5f5fd79a0ca708c66ad2a77f5f870a450611ab90e0b1`  
		Last Modified: Sat, 01 Feb 2025 00:29:54 GMT  
		Size: 70.4 MB (70388982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965511531e0bbc073f46829e98d42038b9f33f4b7b39c2d56c1fa8492596ad56`  
		Last Modified: Sat, 01 Feb 2025 00:29:53 GMT  
		Size: 1.2 MB (1166442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bbfeafa83d9c2c298e5924298e86c791374bf95a6bee235c53a5d69278a045`  
		Last Modified: Sat, 01 Feb 2025 00:29:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4d9cb52fa5bf92f089ba424239a181263588d2afcacf5e8ae59891fcadc53b`  
		Last Modified: Sat, 01 Feb 2025 00:29:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239f11438235d0a18ab255895fd15dac109085fbd681748d145ac3e53f9e6cd`  
		Last Modified: Sat, 01 Feb 2025 00:29:56 GMT  
		Size: 4.1 MB (4054562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bb11036a56ec7301b6293339cd46358a028e337f39db59980b12d95e2f9d1d`  
		Last Modified: Sat, 01 Feb 2025 00:29:56 GMT  
		Size: 73.4 MB (73419405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0b5c785cb62f8144858e97c409a01e50fc281b9c79d080df87ac5f80e66da4`  
		Last Modified: Sat, 01 Feb 2025 00:29:54 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:56b9ca1f42566faa8a817825e409928ea12bb715eaa409c038e5faf7230b3f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8c99fb7d7bbee0089dcb0a4b2ebe59c505bd7c2cf5137b77dee34cc92b2d47`

```dockerfile
```

-	Layers:
	-	`sha256:5a4f032fb17d5242a4efd0e1b236e1ccec8c86e99451570818d9a23d3238f494`  
		Last Modified: Sat, 01 Feb 2025 00:29:53 GMT  
		Size: 36.8 KB (36791 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:f43a108953cfc495c89a7387d9595cab7186f9ed791cd9f2cc08d304cc80bb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180168823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265391da1b458e622c076dd525feabffba5866cc660d9ee8a53916953e751214`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646063a45551a61d3aff631507ce28db6d552b256afec6162f53389af67e600a`  
		Last Modified: Tue, 14 Jan 2025 01:42:24 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7746f5356f4d806184842c20dab2f7db298a72c7e16a631e5490bf7734f2074b`  
		Last Modified: Fri, 17 Jan 2025 15:34:13 GMT  
		Size: 31.8 MB (31782519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a670c2951bbf62896ac8e40687939f687043457bdedb36c6ddba4921455f7255`  
		Last Modified: Fri, 17 Jan 2025 15:34:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d67edbd50a84e4ee4106bbed5e12fc8bcf1e4883cc399f2689daf62066aa21`  
		Last Modified: Fri, 17 Jan 2025 16:15:44 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53094262ac905b0e6409c315de5666e068d51ef70419d1c2b3e7f9d9006528c`  
		Last Modified: Thu, 23 Jan 2025 01:51:37 GMT  
		Size: 67.1 MB (67117332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b557630f92665f49dbe73b678ebd08c0b505d4d51fb5606d2d4a37e8dd9526`  
		Last Modified: Thu, 23 Jan 2025 01:51:35 GMT  
		Size: 1.1 MB (1133487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c598fd9b3df764975b2086b7022d33034d9e9a14de1ed5f5d0fff7c4adf7b5b`  
		Last Modified: Thu, 23 Jan 2025 01:51:34 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3b2630ec4e53ccae5e82a2e0dd67a841ad0b9f0f10db98ff3f1a4b49bceda2`  
		Last Modified: Thu, 23 Jan 2025 01:51:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe9f0a682bd918a45d099d35a1b2babbea2f615757bd18fe453c7e9ce38ba1a`  
		Last Modified: Sat, 01 Feb 2025 00:34:15 GMT  
		Size: 4.1 MB (4054571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce98ed2663c8b12f2225efd139f0c05a1c737840fc28804f4e17b535c86b7b34`  
		Last Modified: Sat, 01 Feb 2025 00:34:18 GMT  
		Size: 72.7 MB (72705623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea5a409ce65e55ed1250981ff24ce1f066d178eceea350586df51f76c36c1cb`  
		Last Modified: Sat, 01 Feb 2025 00:34:14 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:aefdd9b7e544d716a2d328013bdecfeccd08337ff4557c00d697913cee227ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ee79d173cb9db9c8660d6d3ff0cf888cbff4de62909b7a31831c73200a15e4`

```dockerfile
```

-	Layers:
	-	`sha256:0c99a67ca51396bcd482cc597ce7a41977ae1e4f0ac0f742ac522f5512c302b7`  
		Last Modified: Sat, 01 Feb 2025 00:34:14 GMT  
		Size: 36.9 KB (36933 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:6117186318c0c0ffa04165e471dc84231e19de7165313685003fae8991808899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176050302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54ea2eaa697d9bd388c628a5b4d274a219522c8ca02a742ad33cb25bfed1538`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04cd14ba7406c54223a25e09ff76f4ed50955d6c12ebda81a014cf1bcb3461`  
		Last Modified: Tue, 14 Jan 2025 01:47:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7857cd8737af9a8eea315935d7d3ad7c3a82e44fffac567ef03f6b497990b7b`  
		Last Modified: Fri, 17 Jan 2025 15:45:23 GMT  
		Size: 31.6 MB (31602052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dc1f2cd02b6bb43fdaf613016e91db8e2234e6ab6224ae35d45a93e6b3dda1`  
		Last Modified: Fri, 17 Jan 2025 15:45:22 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af3884bee542d760f1684cfe543f6f1333bfeb8cee81af45425176ba4ac091d`  
		Last Modified: Sat, 01 Feb 2025 01:31:33 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef2b4668c0ae84e1b1b14614be0d83e2d0bdf7bd3a5a0d50cf3086e4a6faa76`  
		Last Modified: Sat, 01 Feb 2025 01:31:35 GMT  
		Size: 64.5 MB (64459568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca0ff4082d14ec9516b5f8fdd8555cb091b1d33d2e9dab5cece5040715093a`  
		Last Modified: Sat, 01 Feb 2025 01:31:33 GMT  
		Size: 1.1 MB (1133467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b07a57813eff2a952222af5b4985f596b78a96684cd14bd8842b61c5be663e`  
		Last Modified: Sat, 01 Feb 2025 01:31:33 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da9deb7fe0a54334b4d75446b30ce6873848d23064120f251ca5bf78c12d0ff`  
		Last Modified: Sat, 01 Feb 2025 01:31:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3091d17d1fd44c85115ff7ea94bdedce04286e385424aab4559ef2c95f3f85`  
		Last Modified: Sat, 01 Feb 2025 01:31:34 GMT  
		Size: 4.1 MB (4054563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d74faebc334a9c11a6d089abae7bef662ec0c1bdc62d43064ce81b21b792b1`  
		Last Modified: Sat, 01 Feb 2025 01:31:36 GMT  
		Size: 71.7 MB (71701324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9398ea09ed1a08f300edd0dde29c2b7094d1aed93fc232de424d98342f18aa63`  
		Last Modified: Sat, 01 Feb 2025 01:31:35 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:d67eac93361bbb4327e573ed65705abde1c685e8e67de5c69ab10b55e4133e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e05f81c25683abf25ee6b4f866b00e72d90d3716302500279bb58440d55cb43`

```dockerfile
```

-	Layers:
	-	`sha256:5919af15560bed472965504bc304e49348148013fe6ce31ca5a07ae1e03294b6`  
		Last Modified: Sat, 01 Feb 2025 01:31:32 GMT  
		Size: 36.9 KB (36932 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:37f3e60d67d3602fad9336f4e9a89f4e4f109fc28ac6c9ac8db75b44c03732c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188843486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8522f5079818fe6206e1535753b50391e9dda44885fb2406806cd7b9a5cf4c69`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b061e389e1cfaa1b6c20109d4c4f25f3fbc6449802a6b02e00043572ab4bceb`  
		Last Modified: Tue, 14 Jan 2025 01:45:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caafaee6c97383e599c4b611cce429b0e07ba9ad8b337b34b13fcf110834706a`  
		Last Modified: Fri, 17 Jan 2025 15:42:32 GMT  
		Size: 35.3 MB (35269965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1e3f95b7155d84ae3a16166bcfdbd240ccc473b96bc35e0b4aca771410b154`  
		Last Modified: Fri, 17 Jan 2025 15:42:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c0ad987684471e803c1cca18eabbaa241a2003c62f368a82e1df6dd35a7e60`  
		Last Modified: Sat, 01 Feb 2025 01:30:10 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05187ed7d776be18c600be1c7b1c019d7f0a5d42f9e75f8de3f4ac47fb2b739a`  
		Last Modified: Sat, 01 Feb 2025 01:30:12 GMT  
		Size: 70.9 MB (70872469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58523334b98dec6298aa2de697068d6ec33c67c87721faceb6f504c1103e0b23`  
		Last Modified: Sat, 01 Feb 2025 01:30:10 GMT  
		Size: 1.1 MB (1093041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2aff463c76bef5416b31935c7e3c6b846251b6ad797042a84cf21e69c09326`  
		Last Modified: Sat, 01 Feb 2025 01:30:09 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d44aae07d39ee64c8331bd33e2ccb1a2ae71e73c4e2493dca248a35bb86cfa`  
		Last Modified: Sat, 01 Feb 2025 01:30:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8b4b97c1338633069b2a5566974d84a77aa05bd42b0257c24e45884cf4072b`  
		Last Modified: Sat, 01 Feb 2025 01:30:11 GMT  
		Size: 4.1 MB (4054498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a4f042e49a3f5aa02b3733c1ad2c920fd23a8a4abc78b3e6e394fff38d4884`  
		Last Modified: Sat, 01 Feb 2025 01:30:14 GMT  
		Size: 73.5 MB (73458929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b361f32ee2a4f20d24a5c0c95113f70d8cd924d456ad5547043447fe21b8482`  
		Last Modified: Sat, 01 Feb 2025 01:30:11 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:de8296d594ffdf88c86575bad345f841c74595bae5e45bb15a86c586ab06c5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a85f35e3bffde8245ade2f79ca1f258755d43a1bf8b6d0c8f9329044f55341d`

```dockerfile
```

-	Layers:
	-	`sha256:e67ebc4b3e984d9410454a9ae12740c9c5e909ed96455ee9f888e3c7da9ed304`  
		Last Modified: Sat, 01 Feb 2025 01:30:09 GMT  
		Size: 37.0 KB (36971 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:43754140cb76809ff4473c0076a2a2dffc1bd8e8966740be1e13fba62ac2bc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185011788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecdf8477ee1c86f915ea51496cf96eea9e60e84d1cf00efebc9b6116a8cd878`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76e68f0a14398fc38c22fe689ccdbe9efc47dd74545ef7d9a34649f6f391aa0`  
		Last Modified: Fri, 17 Jan 2025 15:31:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0359f30246be2d06710c6987628b7467e90dbabdacc03435c50f73fdf652e0f`  
		Last Modified: Fri, 17 Jan 2025 15:31:12 GMT  
		Size: 31.7 MB (31662256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fc27b86f75f6219d32a6b98fd674cf6828288fd7d26bfbf565789c3c211cdb`  
		Last Modified: Fri, 17 Jan 2025 15:31:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e04250f94249919f9f70a929c06f2291245dd26575404c97c0b9e9a282d134`  
		Last Modified: Sat, 01 Feb 2025 00:30:16 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4057923325f57bb350e08aff1b9af6a592b3820b5e08878368a722694f559a`  
		Last Modified: Sat, 01 Feb 2025 00:30:18 GMT  
		Size: 71.1 MB (71130765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3ef1006bfdfd707cda4002315b6f6e650cc42404234e278697564d6a2107d3`  
		Last Modified: Sat, 01 Feb 2025 00:30:16 GMT  
		Size: 1.1 MB (1141313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd170b1a71057c018f94830a32e7d1af3238a4c8d61ed67c52c26134a232f9b7`  
		Last Modified: Sat, 01 Feb 2025 00:30:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f93a313b3bd982d4313bc82f52c89ebb9e48f296f5a4d682af839add228b07`  
		Last Modified: Sat, 01 Feb 2025 00:30:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab50d8871b3c539eb17e63aa32419a009bc7c3786703e9f5b72241e7a18a1c86`  
		Last Modified: Sat, 01 Feb 2025 00:30:17 GMT  
		Size: 4.1 MB (4054541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4944d3c796c96f9f075c9afb9389f3b151bb69f0d7c0d66b0c67f349e705e0`  
		Last Modified: Sat, 01 Feb 2025 00:30:19 GMT  
		Size: 73.5 MB (73548127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cec814e3ea24bb7c3d8088100664d4f1c5e7ff176d0bfd1bfacbca271a6405d`  
		Last Modified: Sat, 01 Feb 2025 00:30:17 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:419b8980f4bd5fae768f0cb7770ad543bdbeacd7a963623c9da6bcf56e755a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af5b2bfcbbed232efbf51b4eaea04fcff02c96de4bb1a15cde626b949b90599`

```dockerfile
```

-	Layers:
	-	`sha256:a9ac1c5d08a0638266a715a37066d5a4b1284676ef240260d49c1f76a7e2ddd8`  
		Last Modified: Sat, 01 Feb 2025 00:30:16 GMT  
		Size: 36.8 KB (36750 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:629b4f085cf74f6cc2f4c95a8290d6e5705e9e42ef644fa9d1a74be449d2facd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189293320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c94eb87dc986f5b5f3f5b35e6773dbcd127d04747577241e4422a4b953bb4b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd611afdfde6a92b771a8c2f4dd7b096a1311acfb8646e981977bf38912787b`  
		Last Modified: Tue, 14 Jan 2025 01:48:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c209f5498ef3ad8ea7bb504c38f131ba50cf619a1851c75719ed8999b14e1b6d`  
		Last Modified: Fri, 17 Jan 2025 15:40:08 GMT  
		Size: 33.1 MB (33141129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e42e4c0bcbeddf68ab30e361f517c6280df5af0f0ec68a16549e7d1d49b8cf`  
		Last Modified: Fri, 17 Jan 2025 15:40:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e298ca9d4d6158aa574831de48edbf1705c9e3d4c4b2d1ca89a6d6697ecd16`  
		Last Modified: Sat, 01 Feb 2025 00:52:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51dd0efeafca4c0a4c2bd4c4643e1f8358f3b6564decd7f098a5a3ac7129994`  
		Last Modified: Sat, 01 Feb 2025 00:52:09 GMT  
		Size: 72.1 MB (72099303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958c15174b68268da933dadda635882c49ed4b696b706fb40f1697b4278d6d60`  
		Last Modified: Sat, 01 Feb 2025 00:52:07 GMT  
		Size: 1.1 MB (1083651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8640c541da26939bd8ca6c8ed6ea73d0ea0eb31e59deb06f70e50fed99acd39`  
		Last Modified: Sat, 01 Feb 2025 00:52:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25451b0fdc7c9c23918fba624adc77e714f1f3ed40a95f1a717c3f30b0d64aec`  
		Last Modified: Sat, 01 Feb 2025 00:52:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a138f9d603b7729f42804504b2d8939143a67b69fa706c2f6e402462b1c389f`  
		Last Modified: Sat, 01 Feb 2025 00:52:08 GMT  
		Size: 4.1 MB (4054556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89325a26d5ca6cf7816be41249cd634da9f5df7794a3e823df967bdad63fda40`  
		Last Modified: Sat, 01 Feb 2025 00:52:10 GMT  
		Size: 75.3 MB (75336459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f56b7a4e3b1f822646b4b26a5d2fc779cf6c26b47d042ac056beac8a8bb894`  
		Last Modified: Sat, 01 Feb 2025 00:52:08 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:d9ab9541583e551b121f52ecbdc5af6e86af6d1919c03cf8879778fb3d59da47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea572884e018151732cc42e121d489b1c6c71077f726d1c7f121ce8b868b19d6`

```dockerfile
```

-	Layers:
	-	`sha256:fdc745e4bd9b64486f4f91ab592be01395f393c6c635fc620314255a38da4dcb`  
		Last Modified: Sat, 01 Feb 2025 00:52:06 GMT  
		Size: 36.8 KB (36846 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:acc1b4918628a7eb15f53f5a52c96d03204da37f25ddeefc399260c301a950d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187725156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c9f8ca5c59aad640f20dfda2ab22efed686f737359fc2220e033973978576d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb69847f873261cc901364c6e5453bc8ac36796ac8944ffe1685a0c21d2a1f0`  
		Last Modified: Tue, 14 Jan 2025 06:01:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703b13c3738bcfad450312b6c3271d13582ed04a28739b68831f26b53ebd99fa`  
		Last Modified: Fri, 17 Jan 2025 18:26:13 GMT  
		Size: 31.6 MB (31552550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e3724aa281a150ca69aee1f729479410507f445405497dd77a4e15000217e1`  
		Last Modified: Fri, 17 Jan 2025 18:26:08 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a688d6e86b02c1b5abd2145297bad6a85fbd9a5caa82212e113aa9b817b94b2`  
		Last Modified: Thu, 30 Jan 2025 02:21:33 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff714b843434edc307b7658a382a59195576f1cea29fa4450ceeb3f2e190782`  
		Last Modified: Thu, 30 Jan 2025 02:21:43 GMT  
		Size: 70.8 MB (70782375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05105281b11d349fd238aebe1dbd8e7caa4049132f5ae922b88329f5c6c0cec7`  
		Last Modified: Thu, 30 Jan 2025 02:21:34 GMT  
		Size: 1.1 MB (1134858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd69d37c5e50437d33b0770f5187e8f393cd990d0dae33016d487f4611cd946`  
		Last Modified: Thu, 30 Jan 2025 02:21:34 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22deeeb2a2ca9ad31c23a397a3654bf0fea2ebef5e583b5f75e6e630024aeceb`  
		Last Modified: Thu, 30 Jan 2025 02:21:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09adb05eb69839e686975fd18569a1a6290c157663accddd9608a7a2bdc8ded5`  
		Last Modified: Sat, 01 Feb 2025 13:09:29 GMT  
		Size: 4.1 MB (4054589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4814065e3242f3b30efc824665be1ea837e98b36373540a4a36da9975aefde71`  
		Last Modified: Sat, 01 Feb 2025 13:09:41 GMT  
		Size: 76.8 MB (76825035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5951765f5a54be66d36c26cd7b5732ae73dc23e170f50ceaca7774b73c1976c3`  
		Last Modified: Sat, 01 Feb 2025 13:09:28 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:dd729e1045dfd03c4298b19b81225f515497e4d3a61f8eb491caf9cdd4afeca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a6dbe447f5c1f08cebc5da3c49bba7a90a145a4be0c0fc26227393502d7e42`

```dockerfile
```

-	Layers:
	-	`sha256:a79f96814bedcf5bd342faad7cfa3f41ade66edebc09ed79c28867554f2fb680`  
		Last Modified: Sat, 01 Feb 2025 13:09:27 GMT  
		Size: 36.8 KB (36846 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:fb89662567735d9ea742db8104bf0577480c09698b4735d31e6d8ba473353963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188512203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8142d1768705842b74bda6b7b06f18a188ccad9e13d0182b6e1d1d8394cc302`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
CMD ["irb"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GOSU_VERSION=1.17
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 31 Jan 2025 19:49:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27470f160962be7e0327882668c9f8725389d49d37e462a3fd04f6b968da5e0`  
		Last Modified: Tue, 14 Jan 2025 01:47:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f7fb7cf1b7038b6fe65507b9be7797a94cf06f6599371eed9880da50a374ef`  
		Last Modified: Fri, 17 Jan 2025 15:41:00 GMT  
		Size: 33.0 MB (32983647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff43768b36ebe41cbd93411def03ae863c0d7552ca990d44737eb3c2d1b8f9a9`  
		Last Modified: Fri, 17 Jan 2025 15:40:59 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5bd42dfb67f09dca59367f06a5ea61c24da4edf1a0fbe2a7faf601a6b0908b`  
		Last Modified: Sat, 01 Feb 2025 00:59:03 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579b5a17949f1bccc6a40faf5f392459d1cdca307064315208ce0858d36805a8`  
		Last Modified: Sat, 01 Feb 2025 00:59:05 GMT  
		Size: 72.3 MB (72288398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5375db8efa8e3a0e967a645fb51504aafc87fe440ad82fc36c1bbd5ac656afa`  
		Last Modified: Sat, 01 Feb 2025 00:59:03 GMT  
		Size: 1.1 MB (1131107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4eed93012f076c8739edb979fe3700e4fe6b2605a40d745beba5d0ee00a6ee`  
		Last Modified: Sat, 01 Feb 2025 00:59:03 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a559b9b8d7817b746d9cccfaf07b760981db02ead46b9942351d24da92b08`  
		Last Modified: Sat, 01 Feb 2025 00:59:04 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b624be90222247c3898f8e857c85b4b96f6dfbdc144a96e4205faff3c4002b`  
		Last Modified: Sat, 01 Feb 2025 00:59:04 GMT  
		Size: 4.1 MB (4054566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed2ffd335db8e07e281dbc9148517bfb07d336a5641a4fd7eb8f7ff04217577`  
		Last Modified: Sat, 01 Feb 2025 00:59:07 GMT  
		Size: 74.6 MB (74587343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aec6f55e4a779986e565639f387ff08f3833cbfdbec611b5e18236294e2d3d`  
		Last Modified: Sat, 01 Feb 2025 00:59:05 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:959c5fc5560a03ab5e946cedf369d9f4103994962bd81a3bc9fa89e5f443d5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f1a9bb2f2cf95df772a5c5a498984bbd2550eac03a1c9900a3da589971487f`

```dockerfile
```

-	Layers:
	-	`sha256:9450ed7d4d6c1289c86ee98e59754d385f5856929e88e95b8a753a5d004e3809`  
		Last Modified: Sat, 01 Feb 2025 00:59:03 GMT  
		Size: 36.8 KB (36792 bytes)  
		MIME: application/vnd.in-toto+json
