## `redmine:6-alpine3.19`

```console
$ docker pull redmine@sha256:b6df1b79682fa8d7a829ec835d3ad51718e93c9bc4a43ed87d67cd3eba245a74
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

### `redmine:6-alpine3.19` - linux; amd64

```console
$ docker pull redmine@sha256:197442f1b8843d8eeec7c0e393a8f03fff22de8d933a7c821e5a30943f7fff8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198541713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8e4de4d2359296c2e5f0735c7496bfdd88e258438f7b850fc87b52be9ef8fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f22fa0b8399fbfbe079c4814770b6842bfa2afec4816a5a924c16bf7261c075`  
		Last Modified: Tue, 12 Nov 2024 02:51:10 GMT  
		Size: 6.7 MB (6676606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5753f84b1f14f0742baeabb79a1b9a5e6ebfd8020f9a0a9475310a122260602a`  
		Last Modified: Tue, 12 Nov 2024 02:51:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f76a1477a6df61de9409b75d6dd3eb02881425b9a7fe57cba635d9f36c5a5a6`  
		Last Modified: Tue, 12 Nov 2024 02:51:10 GMT  
		Size: 37.2 MB (37200344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104bd0866433baf80ee026741081f6ed41b5211125c88649d40ddb5d66aad66d`  
		Last Modified: Tue, 12 Nov 2024 02:51:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84e14ed01646acb47bcde4676ff8a03bb56fe2323f925a04aef42fa993753fa`  
		Last Modified: Sat, 16 Nov 2024 02:11:35 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590fe555e1eeb9e3af7ac1a79795fcdfb5744581e122afd3cb6a95589d3aeb50`  
		Last Modified: Sat, 16 Nov 2024 02:11:36 GMT  
		Size: 71.3 MB (71314446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7802ccacf48a39d63da6a1dc2b76240c82b868914ae7223049932371ebdcfa53`  
		Last Modified: Sat, 16 Nov 2024 02:11:36 GMT  
		Size: 1.2 MB (1205506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313a3e82c7b181e57eb598b6d61d7e9870989b747676d4cabb5449e1d76bd2c7`  
		Last Modified: Sat, 16 Nov 2024 02:11:35 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e8923ec628533def1c34dac4bd632be82fffeaf503b90f916ffa98a602995c`  
		Last Modified: Sat, 16 Nov 2024 02:11:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdafea89dafe7825bbe7eae9085c7c1ceb12440c60b5dc8f72688958c4c933b`  
		Last Modified: Sat, 16 Nov 2024 02:11:36 GMT  
		Size: 5.4 MB (5357029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f8d138329b08323c8dcf17df5c2d14471c0eb5fe7d718aebc76473bb5c8639`  
		Last Modified: Sat, 16 Nov 2024 02:11:38 GMT  
		Size: 73.4 MB (73364280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4a110164f6f26a85235fa31e8157575877da19f3dcb490c587719277ee2c24`  
		Last Modified: Sat, 16 Nov 2024 02:10:57 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:1a428bf3d9eab83ff03f669e333fb1aba986e09ca51a1397f04ae10f109cf8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dcbbb28497f15a142e553436643d5ad746249f94dd52b3650935ddca00af253`

```dockerfile
```

-	Layers:
	-	`sha256:8cecdeb0eb5a9fd2fcbd02215d53ad4ccf3960164aab448790beafa962fe63bc`  
		Last Modified: Sat, 16 Nov 2024 02:11:35 GMT  
		Size: 38.9 KB (38908 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.19` - linux; arm variant v6

```console
$ docker pull redmine@sha256:85b0754f08013a93032bfcef32ec718c0cd2665db7ee5c256fca302400277339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190399947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeec1aa0a5275a21dea0b05448bec410f24db2a9077398dfe118d7b9e523897f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
	-	`sha256:6bb9d5f58a7573d32edb5dff3cf53b5be0bb729a8c11f5e5375873e0d5e6d3dd`  
		Last Modified: Tue, 12 Nov 2024 15:17:46 GMT  
		Size: 33.2 MB (33234805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3cc57c92ca90e8176105fe657e31638be9385ad6b4d5d262381e32f0b88acb`  
		Last Modified: Tue, 12 Nov 2024 15:17:45 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2386df7532cc5f69f0248e5c8839ee9a080a5f6b575b76bc7626c1e671227498`  
		Last Modified: Sat, 16 Nov 2024 02:20:23 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c8589d7c96fe9d50da908fc51c828c7b69898ef317cbec6824cc29656816fd`  
		Last Modified: Sat, 16 Nov 2024 02:20:26 GMT  
		Size: 68.3 MB (68261046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967498d3633e98ee4c018ebd771fd77895fd4b5f4874b121ebac54300af11df`  
		Last Modified: Sat, 16 Nov 2024 02:20:24 GMT  
		Size: 1.2 MB (1173524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b6a72a84b22ef3f96bef60e2dea5b7bdff2055afeb3b088d50cb8ddc600444`  
		Last Modified: Sat, 16 Nov 2024 02:20:23 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c79a7d10eefc085952518a374575aebc82fe2bda2f0a66093a97bc5c25514`  
		Last Modified: Sat, 16 Nov 2024 02:20:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdb60c6d527e8a1d8c800d20ce26d2757d5ea57681c325293ef3a1ebfea29ab`  
		Last Modified: Sat, 16 Nov 2024 02:20:25 GMT  
		Size: 5.4 MB (5357041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409b07f0f92476ef315251b76fc14b7f404cc057296400455e3b321cbb2d72bb`  
		Last Modified: Sat, 16 Nov 2024 02:20:27 GMT  
		Size: 72.7 MB (72665751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c927151149359855af1d901f9a82aee85aa49bf9113994022135c064970e890`  
		Last Modified: Sat, 16 Nov 2024 02:20:26 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:4ffdcd51117caa3a5bef7707e13b078bf9271743baddac78e5b0139a2b35378a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (39048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f48649f7e55b590d6a068296bdfc6e48fce12a3d039fce31ec0a90f0da241de`

```dockerfile
```

-	Layers:
	-	`sha256:6a00ec13d85874220db81b3bf125378fc29cf557c9fd77747901b26c4c96e4f0`  
		Last Modified: Sat, 16 Nov 2024 02:20:23 GMT  
		Size: 39.0 KB (39048 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.19` - linux; arm variant v7

```console
$ docker pull redmine@sha256:ede499c2e445a95748a3929faab86b2ab0c00e03a412ba76dd6b2a34ef97ad6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186018622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a406ab3007a1617071718d4f0702c895a93ae4fed1edf9b81f57d7dcaf1edb6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
	-	`sha256:5054701f4e8f07b7b59926d83ad5ecb593ac26fdb43784ad66a5b5a84e12581b`  
		Last Modified: Wed, 13 Nov 2024 06:24:01 GMT  
		Size: 33.0 MB (32952141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a31c694824e71e2b6373cc6fd1d2061e81b3461fc054787603ae364c9bf10`  
		Last Modified: Wed, 13 Nov 2024 06:24:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2b884ec017766ea4b2430862363f62fc3b39c52c875b25d2057bfd240efa8e`  
		Last Modified: Sat, 16 Nov 2024 02:25:20 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96327bc44e148877809adc5824716913715c7466cf607db13f0c87e0371edf3f`  
		Last Modified: Sat, 16 Nov 2024 02:25:22 GMT  
		Size: 65.6 MB (65576162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee759217c5c08c8a5ae0c0a24a179de60686f7d7636f5e01e65aeb1d51fff18e`  
		Last Modified: Sat, 16 Nov 2024 02:25:20 GMT  
		Size: 1.2 MB (1173489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ef2453b4dad26b007f71a267b13b9cfec6c9d96c59a1b4eb33be9cc5065ac8`  
		Last Modified: Sat, 16 Nov 2024 02:25:20 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff4eaefaf4b135e8c91ce0730b2b134f8779481f330efd4ce58f1647285463`  
		Last Modified: Sat, 16 Nov 2024 02:25:21 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f84c4b5855b59e34fcc3036a3bf3f6c902dbcbdf41097b39ce1016e2c44313`  
		Last Modified: Sat, 16 Nov 2024 02:25:21 GMT  
		Size: 5.4 MB (5356914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726814fa9d2a209c60b0075c6fb8905147306dc7e08fd8387b73fca4fe64490e`  
		Last Modified: Sat, 16 Nov 2024 02:25:23 GMT  
		Size: 71.7 MB (71658853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a117dd37bc6b193ad9953c710ea9403788c6bb5d7ac9cedb051450e477c44e7`  
		Last Modified: Sat, 16 Nov 2024 02:25:22 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:111323937d8acc96e80d2f19dd45cc08259b88269c96a9bd96de5615568900d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (39049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee852eef898a36259f5bfd76f98af7f05f5148d1bd139313c1d6cddbc7215d5`

```dockerfile
```

-	Layers:
	-	`sha256:8edb2d138da589b98106a19205ece9ba7a020b29c158a97899e750d700c53036`  
		Last Modified: Sat, 16 Nov 2024 02:25:19 GMT  
		Size: 39.0 KB (39049 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:a50c22e891f42f7845bd58ee9eaa686cb7ee5300b4e6ebcba080311e83f02f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (199007637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d596907d335096a7223da09baa8822f584f8a817d46e4c5335b1605414c0a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
	-	`sha256:5d753d92787f2e4bbe82878267be66e0bf112db7d6478dafd9ff8668a2cc645c`  
		Last Modified: Wed, 13 Nov 2024 00:14:13 GMT  
		Size: 37.2 MB (37179502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e6a4b24e0411678bd493d0efe228e1eb2b36f8931dcf4242fd42d853ea27f8`  
		Last Modified: Wed, 13 Nov 2024 00:14:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f1ccf6a1dac9382ad627baec65b58b094f85ec4f684fd49c2734eee1b0a720`  
		Last Modified: Sat, 16 Nov 2024 03:03:52 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c8adb4c3293a507ecf4910e3c4fadafcb8646316a52b2f47a03ba47a2a2805`  
		Last Modified: Sat, 16 Nov 2024 03:03:54 GMT  
		Size: 71.8 MB (71809517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195e9a708323e3d56b85520effebaeaa2befa2086bfe0e8cff7abbe5cd0d6e77`  
		Last Modified: Sat, 16 Nov 2024 03:03:52 GMT  
		Size: 1.1 MB (1135598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d946f26f1124150bb94f33280d68cdfdce886751cb2f802ec717c33f4e10b02`  
		Last Modified: Sat, 16 Nov 2024 03:03:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7165b791857a511496c8759457764be12a95b1f91bd97b727b41c941a0494c70`  
		Last Modified: Sat, 16 Nov 2024 03:03:53 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8dc99f729cb50fa0ebf5c8c6c083c345afe4a23e44410d9434f2323f79815f`  
		Last Modified: Sat, 16 Nov 2024 03:03:54 GMT  
		Size: 5.4 MB (5357043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079e4b88ffd39f6d7d7f05dd11c4007b5a5c1b4c94937fa32beff8258b272920`  
		Last Modified: Sat, 16 Nov 2024 03:03:56 GMT  
		Size: 73.4 MB (73421547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80004c7164de6bef8f942b0759aa5b5b072032591414a2c6563d3bfda0948f`  
		Last Modified: Sat, 16 Nov 2024 03:03:55 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:42e8cb2a734935fff935319e9f32ea7ba8199b1d84b503ba74756b77345cc0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50dde76cf58f5448051ec7489c8da9554eeadd824ade8b986d2fb8567e018e80`

```dockerfile
```

-	Layers:
	-	`sha256:11287b15261583f39331f03650160583b00339123d908d27a9a680c5b37e075a`  
		Last Modified: Sat, 16 Nov 2024 03:03:52 GMT  
		Size: 39.1 KB (39086 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.19` - linux; 386

```console
$ docker pull redmine@sha256:fcbe81e762a58900aed1daa3d7db5b4b9676f96c178fcd6f5cbe48ee7cd275ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195147639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a989a7810389dde39268c3399d916c3e58f9f0fe79c4c8edcd3f26d0f66f4c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386a1c27d809a5e664cc668edc416f21d50936ee3ce1c69821344b812b4ff8cf`  
		Last Modified: Tue, 12 Nov 2024 02:50:54 GMT  
		Size: 6.7 MB (6743141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a9a7cf146bc9c5dcb68cd098c46325f8e5327134d6c13cb49bec114ad18b69`  
		Last Modified: Tue, 12 Nov 2024 02:50:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b18713502002691dc589378c9af7b30a5345089986ee9d866ed1bdcc78c17a9`  
		Last Modified: Tue, 12 Nov 2024 02:50:54 GMT  
		Size: 33.3 MB (33266671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ffcd4baccdf31a70131310f025186f82f4f73884cc9df4cd8ada2f8ad5fc13`  
		Last Modified: Tue, 12 Nov 2024 02:50:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aca290743c0ceb90b505ed15717c9c11d5501db7012c9ab41b9158a4cf6b047`  
		Last Modified: Sat, 16 Nov 2024 02:11:49 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb25e61ce5a142452ca10b14eeee3b19503e6a87e6881bf39a3a893b53beec9`  
		Last Modified: Sat, 16 Nov 2024 02:11:51 GMT  
		Size: 71.8 MB (71832784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03b3690d234626accb4336807f35c610c9bbbf44fbf270edbb1ab53e19516b0`  
		Last Modified: Sat, 16 Nov 2024 02:11:49 GMT  
		Size: 1.2 MB (1182458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e22b6624172635771fda8a0444ba7146f8faad976a3d9669685c266634a42c`  
		Last Modified: Sat, 16 Nov 2024 02:11:49 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e814588e8bc28d31e3271ba7efd9b2d7dc915940e666b626f025edba5aa84b7`  
		Last Modified: Sat, 16 Nov 2024 02:11:50 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a203aed83c8cbed897eaffc412d10eff1f34598d3d65033bd60e94639c8400e1`  
		Last Modified: Sat, 16 Nov 2024 02:11:50 GMT  
		Size: 5.4 MB (5357029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d892df64abdce28352e1c38819b1c99a6552d81536c40791230d2afe14ed3826`  
		Last Modified: Sat, 16 Nov 2024 02:11:52 GMT  
		Size: 73.5 MB (73508121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2f8ff9cdd14c1bdb357a6ca296ae320dd1d20ddeddfda507ca52f240d66ce5`  
		Last Modified: Sat, 16 Nov 2024 02:11:50 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:e2c0d0d59b22fadb9a31ab382f3211f7bc08c3436e1f52549256953d471a2119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980479a54cb7ac9f2041c0f68d18e986cf4b403e263d3857e7b1be04411dc87f`

```dockerfile
```

-	Layers:
	-	`sha256:cdbac90bcbbae80df23802b2d67b475eac8eac546be393852dd7676eeb2e2ad3`  
		Last Modified: Sat, 16 Nov 2024 02:11:49 GMT  
		Size: 38.9 KB (38866 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.19` - linux; ppc64le

```console
$ docker pull redmine@sha256:03da87835eca2fe692403686497af2be41ab13a056ea618e8d3e00a2b21a75e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199751098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1dd1703c1d085b517f9f360f2f70abc8141a5fc90258535c2e69db12280aa9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
	-	`sha256:4d4af0a1b423a7c6ebee1c73d15b57b9929f2900bc1ae8ac77d9cb2fdb0c681e`  
		Last Modified: Tue, 12 Nov 2024 14:26:12 GMT  
		Size: 34.7 MB (34749893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70baa17ab3620887cf19840b36596d9d3367f5382b52b63c75c06ffd21bf1da5`  
		Last Modified: Tue, 12 Nov 2024 14:26:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c55f961159ce606e0f2de17be6950aaa10e334bd5223241204df023d2bdb694`  
		Last Modified: Sat, 16 Nov 2024 02:47:59 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1070fc411b7d2b0e9ca7aaef89eb999564950c1b00fd9b3f01ef8643226d0aa2`  
		Last Modified: Sat, 16 Nov 2024 02:48:02 GMT  
		Size: 73.0 MB (72952890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b14983f6f91129d41f450a048df0d55ed0130d67080b52783377ac0d054cca2`  
		Last Modified: Sat, 16 Nov 2024 02:47:59 GMT  
		Size: 1.1 MB (1123268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0ea3899550a87a245a3a0d5116823a7aff8e14275b98ef335379d2f02c698f`  
		Last Modified: Sat, 16 Nov 2024 02:47:59 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18579ad8542aafad4bdde9a739828b46a7b536d346663fa847830964bb07490`  
		Last Modified: Sat, 16 Nov 2024 02:48:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e941bae0efb184c70a0fb31d9039713045c7bd15ad3f039ed5ca8df744e4d4b`  
		Last Modified: Sat, 16 Nov 2024 02:48:01 GMT  
		Size: 5.4 MB (5357044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58cbf934c4bb265ef50a66c00e8a76699331698a1a5cf963f3c132b44f04a7b`  
		Last Modified: Sat, 16 Nov 2024 02:48:03 GMT  
		Size: 75.3 MB (75296375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8babf877656dfc3a03f984c8b654a955778bd22d957ab6ba0027c8c8aa638860`  
		Last Modified: Sat, 16 Nov 2024 02:48:01 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:c347fef9709ef78bb9a523ba3898fdc33449ad10a0fd5dc22664243f1d18e1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (38962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcaf75dba7fd9bb434ed4ce2fbb8483bf79724d6365633872b258116f3d7e90`

```dockerfile
```

-	Layers:
	-	`sha256:7c42e65827f11e0deeb302b746b1ac8b2ac44cabdab4a03d09a9ed7456bb7df7`  
		Last Modified: Sat, 16 Nov 2024 02:47:59 GMT  
		Size: 39.0 KB (38962 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.19` - linux; s390x

```console
$ docker pull redmine@sha256:02d00b28f823eea8ef544a5b4dd33a6672d00b1e04fff548cdc73949d2b3cab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198057480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256affb81c7e11ee5a7edbe7111aab8f22dc461c42a27b88289a58b7223a72e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
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
	-	`sha256:48ec692b635ea07e18e524e580ddd6e03066ef865687d2e934960b236806475f`  
		Last Modified: Tue, 12 Nov 2024 21:51:13 GMT  
		Size: 34.5 MB (34485105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f8dcc2aab4e7603fd94441f9a3b660c82f14818fa83e646e8ad9bec5cef0e1`  
		Last Modified: Tue, 12 Nov 2024 21:51:13 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc4e45d333095b735c38abc081da5506a834a8fe7c4136f0f4ac78fcbf5fa3b`  
		Last Modified: Sat, 16 Nov 2024 02:40:48 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa1c844e37a3c00733a212149c60620f766164ab075ed01f135277b3ee60d48`  
		Last Modified: Sat, 16 Nov 2024 02:40:49 GMT  
		Size: 72.2 MB (72192148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1592f882b2f2580abcdea66d3ca0906afa7e0985ef742d7ddd932987b3f22612`  
		Last Modified: Sat, 16 Nov 2024 02:40:48 GMT  
		Size: 1.2 MB (1172741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3575b0c5ec7ae09a753a0e2f3467fde38c80875a3253a1a0cef8659ba75dfc23`  
		Last Modified: Sat, 16 Nov 2024 02:40:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922c2ac7664da7548db04f5a887dfa0691dab2898754d6300b6c5f03e2a9641a`  
		Last Modified: Sat, 16 Nov 2024 02:40:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96048650ef7d9abf032e0e93196edb9177243454e0fbf76d9adfe812e63f4780`  
		Last Modified: Sat, 16 Nov 2024 02:40:49 GMT  
		Size: 5.4 MB (5356988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2315c2b05b90372e3e10ede9ec6f3b9cb44ffca83529c5da079b2e941db490`  
		Last Modified: Sat, 16 Nov 2024 02:40:51 GMT  
		Size: 74.5 MB (74541450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c57d815f5732cee9074c31122a4877945947d52494c9f1917d9670c9a9083b`  
		Last Modified: Sat, 16 Nov 2024 02:40:49 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:44fa7d15c7a4564442a7cf22abd2367014ed99aeb91a8e05953999dd5ea3a384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 KB (38907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182edf9f9d13032d2bd57af0207b03adf9e2135e1d2fd3eca612fb66b1382733`

```dockerfile
```

-	Layers:
	-	`sha256:dd032eec06bc430b56245703b5e69658a5ef7b342bdc19bf3996d1c61f86d0d8`  
		Last Modified: Sat, 16 Nov 2024 02:40:47 GMT  
		Size: 38.9 KB (38907 bytes)  
		MIME: application/vnd.in-toto+json
