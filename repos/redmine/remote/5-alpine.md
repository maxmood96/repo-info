## `redmine:5-alpine`

```console
$ docker pull redmine@sha256:f3e9bd1294b56ada9e1a22594279c3bdce588805ec3983a1b696d22fd90944fe
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
$ docker pull redmine@sha256:2c9ea32609988055bac9f7375fd7a4260cc0782c531d4802d4f18d6b38bc2772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188451846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ce5fcb73873542ec1f37b9b190af7a3c5e79e8d24c75cd0c09c937421e99fb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 12 Jun 2024 02:38:54 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV RAILS_ENV=production
# Wed, 12 Jun 2024 02:38:54 GMT
WORKDIR /usr/src/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
ENV HOME=/home/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_VERSION=5.1.3
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 12 Jun 2024 02:38:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 02:38:54 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 12 Jun 2024 02:38:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a78ef59060f3f9982a40978bcf075f74504bbb0af32248ee79ad51f0ce54be1`  
		Last Modified: Wed, 22 May 2024 22:58:28 GMT  
		Size: 6.7 MB (6686041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6898f7a531277cf5705741be398abc8711f7505fd9d6185765b43d89913053`  
		Last Modified: Wed, 22 May 2024 22:58:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d6bc5296deeebda15a473f06132e7871bbaec9a52f1f71789e81f4448f028e`  
		Last Modified: Wed, 22 May 2024 22:58:28 GMT  
		Size: 32.1 MB (32104623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7b555ad78e3b45dbfe496278dfd744c045965720e892755832b38f3671f94c`  
		Last Modified: Wed, 22 May 2024 22:58:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d076f1e1b4f06650e35b5930b018484184b18a74425f7104a69ca2510e73cf8f`  
		Last Modified: Wed, 12 Jun 2024 18:04:48 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b72071037082d2734a3f861ee717cf1d0dac6e3a40abd051dfe9fbfe55fb9ad`  
		Last Modified: Wed, 12 Jun 2024 18:04:50 GMT  
		Size: 69.6 MB (69606827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4982c2bd8003905b67806baf9bdcc0d42c79b95fafc303e8ad1c7617d43ae7c3`  
		Last Modified: Wed, 12 Jun 2024 18:04:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c47156b05cf2c7e71328a9741b20021834616da3a36bd06940b99597642fa`  
		Last Modified: Wed, 12 Jun 2024 18:04:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765f92a4c5e87862e0a49f88af457830d5f6c91216f8385b5b51fa86603289ae`  
		Last Modified: Wed, 12 Jun 2024 18:04:49 GMT  
		Size: 3.2 MB (3243427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b466d7e59a84cd86c2ba95ebc54bb785923a14d83f523865a90956f63dc7082e`  
		Last Modified: Wed, 12 Jun 2024 18:04:51 GMT  
		Size: 73.2 MB (73185301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33383ee283031d27054a37d5a3941b4cef0425c35f6012609d491a24ded7cdb0`  
		Last Modified: Wed, 12 Jun 2024 18:04:49 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:38a9189a683228bd72eee68c35069acba45865d7690760f89d3f099fc8a65fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e68ce8acc1b279533d5751a0302d49a8593a872d1075dae91a789013442f08`

```dockerfile
```

-	Layers:
	-	`sha256:9d56e5b2a935da9872463b114d6b3532864ec7e6f65c78109268e47c33b9ada4`  
		Last Modified: Wed, 12 Jun 2024 18:04:47 GMT  
		Size: 34.3 KB (34265 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:80ed88395366705eea9d326cf3bd9272c2f2938e0b87225d1a1952f20a26d209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182419027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec86f1718bb1873777d657b33f0e627929487b6b2ab226907b56215770f283a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 12 Jun 2024 02:38:54 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV RAILS_ENV=production
# Wed, 12 Jun 2024 02:38:54 GMT
WORKDIR /usr/src/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
ENV HOME=/home/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_VERSION=5.1.3
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 12 Jun 2024 02:38:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 02:38:54 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 12 Jun 2024 02:38:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba601ab84a54fbd88961a2445fe3844aa545bb92bceb0a919bbf9c4416bc413e`  
		Last Modified: Wed, 29 May 2024 00:39:01 GMT  
		Size: 6.5 MB (6533788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb6864cb0b33a079eb5dd296147ff306afee376b622082f53b002425c6acb48`  
		Last Modified: Wed, 29 May 2024 00:39:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95034f7f916814c7d2a405c96a859607debcbc56115a28d3c15962f45f222016`  
		Last Modified: Wed, 29 May 2024 00:43:38 GMT  
		Size: 28.2 MB (28244111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e150d1811856ad961fec6b7806efadfd550ccd8171b6564db13a681165e678b2`  
		Last Modified: Wed, 29 May 2024 00:43:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29760566cb4f5ffa5e533ef0f6c461f519a575f4214d604c9e25efdf636fb87`  
		Last Modified: Wed, 12 Jun 2024 18:13:36 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c03ba76c20866bf9d67e7bc5a0482949586e8a71dc24b3b60efa3941bf26b8`  
		Last Modified: Wed, 12 Jun 2024 18:13:39 GMT  
		Size: 68.9 MB (68853515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729fde5397d345cec926ff4b3b3f73414de4872af73a1aea9af25f7df4c8eebc`  
		Last Modified: Wed, 12 Jun 2024 18:13:36 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b862d365beaa024052303621763e3423a21f59e414320b036a2951aae450`  
		Last Modified: Wed, 12 Jun 2024 18:13:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977bdd74595f519a5ae68d19a9620f803fbc183853e6858cdcdd4da0985c8450`  
		Last Modified: Wed, 12 Jun 2024 18:13:38 GMT  
		Size: 3.2 MB (3243592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c35f7612d03e39ab49ead3c7b9534e3380630b3bf2665de72696fa4bf864143`  
		Last Modified: Wed, 12 Jun 2024 18:13:40 GMT  
		Size: 72.2 MB (72175431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c89550512cfe42c6801de941a7c209ad785fa327ceb8aefeb3b1811a17fdfb`  
		Last Modified: Wed, 12 Jun 2024 18:13:38 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:9781688cf8c349e16bedfd51af2522d0fafa39fac1978de6bf934e32d3039d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eac8fef9a96a29debca8b3c260ea731d67916091754d487f876528c8bb7b6eb`

```dockerfile
```

-	Layers:
	-	`sha256:05f5fa1debd728e9d0047003f0c69ebfb2d0372e53a0311759976c52cf00c0c9`  
		Last Modified: Wed, 12 Jun 2024 18:13:36 GMT  
		Size: 34.5 KB (34473 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0f5b88bae7e9421674a64dc379b4359e4fd526e0b1fefbf1f048287e77684698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177876745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4711e713900ec59ac7b3f61b76dd84cc04ac3510a417a7551251802f979f7bb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 12 Jun 2024 02:38:54 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV RAILS_ENV=production
# Wed, 12 Jun 2024 02:38:54 GMT
WORKDIR /usr/src/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
ENV HOME=/home/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_VERSION=5.1.3
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 12 Jun 2024 02:38:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 02:38:54 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 12 Jun 2024 02:38:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35990c7f6457fb80d05b620b66bf47e94b2905dcf6f639a5c2f91bb56f4e8113`  
		Last Modified: Wed, 29 May 2024 01:42:20 GMT  
		Size: 6.4 MB (6377927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd0ba94321dc05bd6d277221987f3c7fd6546ccee8e1c8a7688bfa276a9524e`  
		Last Modified: Wed, 29 May 2024 01:42:20 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d13d738a5d34839ed5419ac9e878593d9aeb404c12e03601590bead38482018`  
		Last Modified: Wed, 29 May 2024 01:47:27 GMT  
		Size: 28.1 MB (28118576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94132a32bc156a50aebb4f71705fae3fe561eb5c91d8430fa6fba82e7e54924e`  
		Last Modified: Wed, 29 May 2024 01:47:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417aafe0bf959065bff2f4e71f6bb6a679cac2cf6233a23766cc5995e402df05`  
		Last Modified: Wed, 12 Jun 2024 18:49:22 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfa37fd5c951b250bf3c6ae8e0cde7210aed11b5fb092c3c897a215752f426a`  
		Last Modified: Wed, 12 Jun 2024 18:49:24 GMT  
		Size: 66.0 MB (66005325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e63ef3125d3102f368f7115374c8b8ff76d5705c0251cc46c90a72ad460ff91`  
		Last Modified: Wed, 12 Jun 2024 18:49:22 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bcacdabed00c222ee9588f2b42d1add59347b83265dc49cf2d3fd5367f7554`  
		Last Modified: Wed, 12 Jun 2024 18:49:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb6f6984df28e1c5bb8352ea96ca141d5260b9506248d140c3efabea0091b30`  
		Last Modified: Wed, 12 Jun 2024 18:49:23 GMT  
		Size: 3.2 MB (3243532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2dad053cfc010337ea93527ec0c7fa51f38316c7f2df31b8a219374b44637`  
		Last Modified: Wed, 12 Jun 2024 18:49:25 GMT  
		Size: 71.0 MB (71033817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe31842985b4005635ac38841a48ef98333dd22e422b0b99b58453f41449a1ea`  
		Last Modified: Wed, 12 Jun 2024 18:49:23 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:f5fd3ba6e24d542c3d9834c793b347042c37bfc4348a241f498322b8ebb1c2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21af48b11655b102b54f6f01ba1ac414d3556b894169bb78eb7a34d1a219bef0`

```dockerfile
```

-	Layers:
	-	`sha256:dc4ecd4290867698975232093652f6968526624d41ad696e23a1d9b09eaffefe`  
		Last Modified: Wed, 12 Jun 2024 18:49:22 GMT  
		Size: 34.5 KB (34473 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:089f8c4cad5d7b5cd646173260bc04742bd85d44042208cefa9150c1fd80caf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190050674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92aa6e694d34b16647d964e0ae92e1ccc95450f904fef874579d37d5b8f2a2d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 12 Jun 2024 02:38:54 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV RAILS_ENV=production
# Wed, 12 Jun 2024 02:38:54 GMT
WORKDIR /usr/src/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
ENV HOME=/home/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_VERSION=5.1.3
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 12 Jun 2024 02:38:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 02:38:54 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 12 Jun 2024 02:38:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dc0b23bb0ccafe3ed03e575ee0519f09326f0f1465ee14f7fae72260edfdfb`  
		Last Modified: Thu, 23 May 2024 06:32:41 GMT  
		Size: 6.8 MB (6752283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30338ab469152a49fba6e1ce9f134ab631653654f5d7440ad8cf1a77ba27f21`  
		Last Modified: Thu, 23 May 2024 06:32:41 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be611d8a6a3c6f0cbd9e158f6afa75e1e1daf2f25ae38c61f59f3fce371303f`  
		Last Modified: Thu, 23 May 2024 06:37:52 GMT  
		Size: 32.2 MB (32169238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffd4df9b09eaf6bcbc5539ac337bf8211660d7b67af82fb130e7d09c8f55b2e`  
		Last Modified: Thu, 23 May 2024 06:37:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d43ac8a0f9dee9a56cbe01dc3683e7b9bb294995c4dbbb3c3b82c40cce8e5a`  
		Last Modified: Wed, 12 Jun 2024 19:32:12 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d291f6216724b13edb2d874fc666a4d614546fc601ed87cdd29cdc2b82262637`  
		Last Modified: Wed, 12 Jun 2024 19:32:14 GMT  
		Size: 70.1 MB (70109515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1a2073b9048db3da11a7cb493632d6025b2c7d52f726abf4ea82bcab55bb1a`  
		Last Modified: Wed, 12 Jun 2024 19:32:12 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dbf4b0efb066587cf216bef2c09cc384150d3e5172c5f297c49a0f4c23d79b`  
		Last Modified: Wed, 12 Jun 2024 19:32:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72597ceb277f940af0af30071bd13aea05da8c061396c6545f2ca0ab02c81b2`  
		Last Modified: Wed, 12 Jun 2024 19:32:13 GMT  
		Size: 3.2 MB (3243597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aa94507583f4d22516979fb5f0d70551dd8a706268c7f81e8f7b342b50b9d1`  
		Last Modified: Wed, 12 Jun 2024 19:32:16 GMT  
		Size: 73.7 MB (73685732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75da0354734d37fec8f532b014dd278e17ac667d2cd442a4fe4083be22692f4`  
		Last Modified: Wed, 12 Jun 2024 19:32:13 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:90710c892726ef2172c34d9db64ec2eea743b140d323e22b4547d7aa178f50cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946a176f1b6b1d7bb47b569865469a35f24c09a66cde404ccfd2c37ef4f86905`

```dockerfile
```

-	Layers:
	-	`sha256:d26ccf1bc8fc35b10e1a3c7cc397fc8e7ca86817ca3699e29918c373312920b5`  
		Last Modified: Wed, 12 Jun 2024 19:32:11 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; 386

```console
$ docker pull redmine@sha256:263e2232bf0bf5541005b8c0d5119b000db47360ad52357fd6cc9aad29ebdb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184905311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e08f37b28e9beb530f97c5e277dffe224b0c064cd39ee33d816e817b53403d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 12 Jun 2024 02:38:54 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV RAILS_ENV=production
# Wed, 12 Jun 2024 02:38:54 GMT
WORKDIR /usr/src/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
ENV HOME=/home/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_VERSION=5.1.3
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 12 Jun 2024 02:38:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 02:38:54 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 12 Jun 2024 02:38:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb08ac503ebcf4397d4fa11e0520a0938a3e976fc45f1d61f538e2ba6d9911a`  
		Last Modified: Wed, 22 May 2024 23:00:44 GMT  
		Size: 6.8 MB (6751140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f043e3055c861ca938580df08a0bfc51f14c7f372b61a210a1d19f50f50d79`  
		Last Modified: Wed, 22 May 2024 23:00:44 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d056aa172db88a373137c3b3b98420cb7fde198275cf4605dd131723a906385`  
		Last Modified: Wed, 22 May 2024 23:00:45 GMT  
		Size: 28.1 MB (28098911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6d1555cad442fc1af56fcf70ca34a042cf1c021ea06161d2705e258a9b0e12`  
		Last Modified: Wed, 22 May 2024 23:00:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7c25c47378087b4b4dbd923464cc560ba020b851ea8b5d67ce708d1be6258f`  
		Last Modified: Wed, 12 Jun 2024 18:04:51 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917bf90672b9190c037ba2204340977e7a1a974b8a2557b3abc7f091eae59653`  
		Last Modified: Wed, 12 Jun 2024 18:04:54 GMT  
		Size: 70.2 MB (70190228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4adf962da61d3b465b2a51cfae877a97bc2ea3ecd169b1ebe4200eccafa5270`  
		Last Modified: Wed, 12 Jun 2024 18:04:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5b5d5c0cf294b4deec147533f240f84af50017ca9703b0e43aceebca676c34`  
		Last Modified: Wed, 12 Jun 2024 18:04:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc7e7e276b1ffb63c6689b9f92782f3aa6cd062e5e0cb9be6776f1160403116`  
		Last Modified: Wed, 12 Jun 2024 18:04:53 GMT  
		Size: 3.2 MB (3243620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e67d76c0b1032727217e40bd33e76f75d084c2b8caca24374641a5bbdf0cf3`  
		Last Modified: Wed, 12 Jun 2024 18:04:58 GMT  
		Size: 73.2 MB (73150698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b0f5bd1c1bbafcb08c83356f7d35c02524ff1ac9a6123e56fb553ae944de7a`  
		Last Modified: Wed, 12 Jun 2024 18:04:53 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:e5cf32bed87a97de63fda082a07f8c1411440daadca8e44ec522f75bf3fb3a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0412a2d15066ed64c27784ed3845e4d5980255437ab8c8c7adc65a026af7c635`

```dockerfile
```

-	Layers:
	-	`sha256:f90473d227f7451c0132069c16ce8ad38aa95ac9943a210375ad5f83a279ed81`  
		Last Modified: Wed, 12 Jun 2024 18:04:51 GMT  
		Size: 34.2 KB (34205 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:5d6adf2d752e56e986ff9c36fd59e7d0699a299b3a08b8cb86c46fb58b11c35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187067399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d993d387b437ce932d305df602e20c06bca04defd8a880f24a88ddfc834c865`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 29 May 2024 20:43:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV RAILS_ENV=production
# Wed, 29 May 2024 20:43:51 GMT
WORKDIR /usr/src/redmine
# Wed, 29 May 2024 20:43:51 GMT
ENV HOME=/home/redmine
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_VERSION=5.1.2
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 May 2024 20:43:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 May 2024 20:43:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 20:43:51 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 May 2024 20:43:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0997e3ffaeea3ef5004176a257737f82a2d5daf9535aab7bb6119241c2cc91`  
		Last Modified: Tue, 28 May 2024 23:41:38 GMT  
		Size: 6.9 MB (6912997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a01ca7c875962fd1f1614e374216b5de18751dba1db60ed031c204e367c189b`  
		Last Modified: Tue, 28 May 2024 23:41:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c240bb216be273d59aa2ebd72a95807eabcc08e4b48caa3571f0a6c974d299b`  
		Last Modified: Tue, 28 May 2024 23:46:47 GMT  
		Size: 29.4 MB (29408519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9f2811c2e9c62bcedeea2319937539919b248145487df1781fbeae3c2188ee`  
		Last Modified: Tue, 28 May 2024 23:46:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f352bc0f13890ccbe87b9159da79c899865d0731e9304b16ab1aca1016ab29a`  
		Last Modified: Thu, 30 May 2024 04:16:42 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a0e3898712c6a936911a8889023aacbfd075a20b1a0bfb8568b25f7e23a6c`  
		Last Modified: Thu, 30 May 2024 04:16:45 GMT  
		Size: 71.2 MB (71227327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c914a8261aa0b2df455f1c8e2da260a94dce9e9986cb13b01ec9a748300ab1`  
		Last Modified: Thu, 30 May 2024 04:16:42 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b91f4d8dfd8751122812508e643249e3914152ecaad74721771047acfb4f47`  
		Last Modified: Thu, 30 May 2024 04:16:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fe594202bfdfbb4dccc5ad16262fba07297f2406678514f6665f3684a702c`  
		Last Modified: Thu, 30 May 2024 04:16:44 GMT  
		Size: 3.2 MB (3242949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4022d360a4fd009904e3c7305be8dba70bc7663c0f9100d267680af6a2256ec9`  
		Last Modified: Thu, 30 May 2024 04:16:46 GMT  
		Size: 72.7 MB (72702224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642bb6b3213b269308261c4b3823e435def566e095a38a3ac50601469fba3c3a`  
		Last Modified: Thu, 30 May 2024 04:16:44 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:ba23481a24c96c0d4ccb998715c62d24fbe00599e3be0b78106abffb2c70fde3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b86e0685b38fb106efbce0dafa869765cb0d23dbc569857b25efeed210b644b`

```dockerfile
```

-	Layers:
	-	`sha256:0535a0a19b4effed6d2082a8d7e084246c39ae1f3fe700ec4a3d59712449a467`  
		Last Modified: Thu, 30 May 2024 04:16:42 GMT  
		Size: 34.3 KB (34340 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:1ef7e71b33404e8c48904d64b1d2c4deb8f1618b60cca65e9463b5a859304568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185037629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68acab4bdc3db6c9795b7b62a4d73c33a2a926370217517355f16546f21db10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 29 May 2024 20:43:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV RAILS_ENV=production
# Wed, 29 May 2024 20:43:51 GMT
WORKDIR /usr/src/redmine
# Wed, 29 May 2024 20:43:51 GMT
ENV HOME=/home/redmine
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_VERSION=5.1.2
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 May 2024 20:43:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 May 2024 20:43:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 20:43:51 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 May 2024 20:43:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db7ef78b6527c4eb6cb6da7f7fe35584a5d3f9c1b77b2e556cbeede3c81fdcf`  
		Last Modified: Thu, 30 May 2024 18:40:40 GMT  
		Size: 6.9 MB (6947806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c48b7667643f259fd9b2afb26403781c93e5b488d3d6fabf63e185cd79250f`  
		Last Modified: Thu, 30 May 2024 18:40:39 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567eafe826bed6598b2aba2db9285732134c310c8ff7aab913e90ab1ec370e1b`  
		Last Modified: Thu, 30 May 2024 18:40:44 GMT  
		Size: 27.3 MB (27330614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85d258ce816d752813649f61cd9b2e04174b7fd289e7d335330f0625718c03`  
		Last Modified: Thu, 30 May 2024 18:40:40 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9386091a0a9818d19bc9bb1794b14e2571605755b20e713757e5278375ea99d`  
		Last Modified: Fri, 31 May 2024 04:29:19 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b105a17065786e05c7c10b7e13daade16cbf40ec418d0d2a4759e9c69ce609ff`  
		Last Modified: Fri, 31 May 2024 04:29:29 GMT  
		Size: 69.9 MB (69946865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a2b9383100c19a0336e5157e39ddc763fce64b4e5997cd85b3505707c1a694`  
		Last Modified: Fri, 31 May 2024 04:29:19 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3017cd1d7dc96bc98b788a544a744ca98888454eeb532e5c721e7ada942e45a9`  
		Last Modified: Fri, 31 May 2024 04:29:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0073dab19ca86078aa414658d5ace17a0f69c0840f798d06c317737df986a858`  
		Last Modified: Fri, 31 May 2024 04:29:21 GMT  
		Size: 3.2 MB (3242976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f29662abc2b997a3708afa8f314023a21d811f8713b488edea903f8bc64924`  
		Last Modified: Fri, 31 May 2024 04:29:32 GMT  
		Size: 74.2 MB (74197270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308e1824dca718df4b0c2d3cd77d798857717a2eebcd24f73224c141c1425437`  
		Last Modified: Fri, 31 May 2024 04:29:20 GMT  
		Size: 2.0 KB (2011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:e5309fc1b230249acf2955176e1a44aacdbc5fcbaede469481e948036bc228ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a399b1c4d9f0527034736a2a2f0051d659c2855beeab333448b6122fadb2b4ff`

```dockerfile
```

-	Layers:
	-	`sha256:9843d6c41535a6ab544ee55ec98b210e3ca3b10d86bf54d9634ae95d9182acdd`  
		Last Modified: Fri, 31 May 2024 04:29:19 GMT  
		Size: 34.3 KB (34339 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:ebe355e6e900ee949f4cfc779b0a989276ad71853f2c5825f50643ef9e117051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188436471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490b80c8abd701a325c3765c1135d704dc18188023f9b337996e333613cc7cbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 12 Jun 2024 02:38:54 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV RAILS_ENV=production
# Wed, 12 Jun 2024 02:38:54 GMT
WORKDIR /usr/src/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
ENV HOME=/home/redmine
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_VERSION=5.1.3
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Wed, 12 Jun 2024 02:38:54 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 12 Jun 2024 02:38:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 12 Jun 2024 02:38:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 12 Jun 2024 02:38:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 12 Jun 2024 02:38:54 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 12 Jun 2024 02:38:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe04587d67a77c068d15e0aae54bea82e27ce2196da5830bb733e1485199fe8`  
		Last Modified: Thu, 23 May 2024 03:23:09 GMT  
		Size: 7.1 MB (7063173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1781a16f232f5d025bb0b2e544a1826920fb8daec80f55ba678c7d7db6bdc4`  
		Last Modified: Thu, 23 May 2024 03:23:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565733c34c617aba5fb20e8d86b20d297e2e2bee12d185287cd0b4e9963722dc`  
		Last Modified: Thu, 23 May 2024 03:31:41 GMT  
		Size: 29.3 MB (29261564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193f98c2e7626bdf49c6f9f012f9ad50d03e50854b3b8461f6c8cada54e79bb`  
		Last Modified: Thu, 23 May 2024 03:31:40 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f9a0572abb0476c18b0915fb049df931cb78ed57254c2b817008e5c95e2ace`  
		Last Modified: Wed, 12 Jun 2024 18:46:20 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71d779d5ed905ab6d9c53383aed648bdf04d74338e29165f0f9baaf834f8637`  
		Last Modified: Wed, 12 Jun 2024 18:46:21 GMT  
		Size: 71.3 MB (71289268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf52842ee344d926182553b1841cf143338512414a0e97af1643807362c7f057`  
		Last Modified: Wed, 12 Jun 2024 18:46:20 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef909728f91ee7d0e5ce8d575a72c049d41782fa803a525cb51a4254482c4ae`  
		Last Modified: Wed, 12 Jun 2024 18:46:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6a19f53606e630d4be3461849705c94d1f5c57bf7172b91c68c4ed6ff1edd3`  
		Last Modified: Wed, 12 Jun 2024 18:46:21 GMT  
		Size: 3.2 MB (3243540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6b2905d72fc5b22ade3bd7ef68011baf44f5d9ca705752000f5eac0339f5ee`  
		Last Modified: Wed, 12 Jun 2024 18:46:22 GMT  
		Size: 74.1 MB (74115050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294b363783ced3ddb8cf29e2b03de9911690ff0488a325b4c350fc4e66775b86`  
		Last Modified: Wed, 12 Jun 2024 18:46:21 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:cd510caf2bb43627e931e46bdc7fbe8d5c19c5227b41aa1574c931a055d9ab05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace42339f187ddea4913b5367ad021cd0a67dc864d695f66046e7d431e9b458c`

```dockerfile
```

-	Layers:
	-	`sha256:f419beb357815e0d4562923385788b2d181f16973f6987ecae04e01f1617c9c4`  
		Last Modified: Wed, 12 Jun 2024 18:46:20 GMT  
		Size: 34.3 KB (34312 bytes)  
		MIME: application/vnd.in-toto+json
