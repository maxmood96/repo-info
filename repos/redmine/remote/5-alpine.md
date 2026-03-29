## `redmine:5-alpine`

```console
$ docker pull redmine@sha256:34ae18331d0a43529ab7f9003502cddc3a7caba5aebc8704d421bd5e19a805e4
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
$ docker pull redmine@sha256:547ac967a7653a9fd923f6a8446fb4bf101944e188a83b122b3a3884e7154cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191608067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee77fc110839c040842f3b99913256e637a9ea1c04141c6b2f407b1aa0387a45`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 27 Mar 2026 18:30:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:33:00 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:33:00 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:33:00 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:33:00 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:33:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:33:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:33:00 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:33:00 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:13:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:13:09 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 27 Mar 2026 19:13:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:13:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:13:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 27 Mar 2026 19:13:12 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:13:12 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:13:12 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:13:12 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:13:12 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:13:12 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:13:12 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:13:12 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:13:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:13:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 27 Mar 2026 19:15:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 27 Mar 2026 19:15:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:15:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:15:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:15:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:15:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f139e3d332027d11d39a0c8ee9ba41cb8b795552507993d70b9de68322a755`  
		Last Modified: Fri, 27 Mar 2026 18:33:07 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d22c9a3238f42d1ab1ecf81a80c03c236239a1f9d81dc7f12ccd42aa1b04de`  
		Last Modified: Fri, 27 Mar 2026 18:33:08 GMT  
		Size: 33.6 MB (33633965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882ca6122ff973cfbf634c18d6725ec4cb3c8e4ba4926b5d5cee01bb09204759`  
		Last Modified: Fri, 27 Mar 2026 18:33:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010aaa9a9dc8a770c4028346215a0faba780058566193ad862379fdef34e6235`  
		Last Modified: Fri, 27 Mar 2026 19:15:18 GMT  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21376d1c3b9ad439a420cd0343948b68b1945300b0e140f5be85aba5eef7def0`  
		Last Modified: Fri, 27 Mar 2026 19:15:21 GMT  
		Size: 78.7 MB (78721617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1a378f3c7e2b94d4c473fffea590114762fccebb514507d808b15b6bad8e3b`  
		Last Modified: Fri, 27 Mar 2026 19:15:18 GMT  
		Size: 976.1 KB (976065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cd9f817f83f2544680146e66922a3c441bdf20651fb9be49744602ef508494`  
		Last Modified: Fri, 27 Mar 2026 19:15:18 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad178c9658705570396efc220edae8ae16fe674169503a5904f53ebc445f82f`  
		Last Modified: Fri, 27 Mar 2026 19:15:20 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3272fa146dd0baa1f19aa6f96c1102abc338c3738ad84bb3b914441f20f737c6`  
		Last Modified: Fri, 27 Mar 2026 19:15:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd587f5c63642d7c02ebaf00bf88f840b7d7c7f7283f42ef0a70f40ccace37a`  
		Last Modified: Fri, 27 Mar 2026 19:15:20 GMT  
		Size: 3.3 MB (3254627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df4c820eb74ee39a7457a45d270d19aa4034b1a382c7cb728df07b91913b5fc`  
		Last Modified: Fri, 27 Mar 2026 19:15:23 GMT  
		Size: 71.2 MB (71155884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed4778badedcc396c42032fdb93ef6000bf4df04d15c9118f04f0c5c81ce9f5`  
		Last Modified: Fri, 27 Mar 2026 19:15:21 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:e430ac71516c6165022f96bcb144a63c99974459bb834f830fd4c5029b6ca4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf7874bee5a482205a140532b896adfbcdac2bc3f9c5f10ce620606441e5a22`

```dockerfile
```

-	Layers:
	-	`sha256:50ec0f27616adc7d1e1712635dc73d17f8c0722f8eb9db1554742a5ad7ab9e18`  
		Last Modified: Fri, 27 Mar 2026 19:15:18 GMT  
		Size: 40.8 KB (40787 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:e26263077d3fc844f916a2e8fd18ee1cfca948471f83ec8a18c3b79daebde0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183028204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c3e8853055c027dd2b170910af2bfbe7b8df657bceb94d382a822f06013f93`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 27 Mar 2026 18:28:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:30:43 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:30:43 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:30:43 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:30:43 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:30:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:30:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:30:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:30:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:30:43 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:30:43 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:15:48 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:15:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 27 Mar 2026 19:15:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:15:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:15:57 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 27 Mar 2026 19:15:57 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:15:57 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:15:57 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:15:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:15:57 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:15:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:15:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:15:57 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:16:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:16:00 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 27 Mar 2026 19:18:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 27 Mar 2026 19:18:43 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:18:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:18:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:18:43 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:18:43 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c9e3059c14c8805aa9882e8f62c99c15bbf7d87f524a38a81641928ffac980`  
		Last Modified: Fri, 27 Mar 2026 18:30:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafaea441d124568645e23343c218d8de3f96c94fa88718d243d7e3231d10d5e`  
		Last Modified: Fri, 27 Mar 2026 18:30:50 GMT  
		Size: 29.8 MB (29775299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e793053ba9d5770f799b8edf808763744e468b7c5fe13ea1dd29cf89e101150`  
		Last Modified: Fri, 27 Mar 2026 18:30:49 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0356d7e21755e19d7d42f774ed835626ef2d4a29173222cacf26e4b0e6fb9c3b`  
		Last Modified: Fri, 27 Mar 2026 19:18:54 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69b76b2efb8b2a7e09aea7c53a8c8612b8262b1be1b011f2bb76273c24d5d09`  
		Last Modified: Fri, 27 Mar 2026 19:18:57 GMT  
		Size: 75.1 MB (75146155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a27a70f892f87ed25b979c24b4f98127dbf5bccc045a44e0a1b75b2070a122c`  
		Last Modified: Fri, 27 Mar 2026 19:18:55 GMT  
		Size: 942.5 KB (942453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b526d1b75c59ef1d5317d7bd8b90f598935be878b4eb812959619d70ee98458b`  
		Last Modified: Fri, 27 Mar 2026 19:18:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327fbd2f102dd3f4d6faf901d68a63cf4ad24a950276706bb5525a7189486a52`  
		Last Modified: Fri, 27 Mar 2026 19:18:56 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2bc11a772d7c5210e4237e26a0e110e39193cb4d2d258b1e28de058c9fd1b6`  
		Last Modified: Fri, 27 Mar 2026 19:18:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844d9bdacc24b7eed645f29a854118a3cb2a8c2794e4c5b8c4a92f31b523981b`  
		Last Modified: Fri, 27 Mar 2026 19:18:56 GMT  
		Size: 3.3 MB (3254691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60ba11b34d270cd32a93ec9cb1fee6e981fa21afc03ece9c544a77c0f2d97ae`  
		Last Modified: Fri, 27 Mar 2026 19:18:59 GMT  
		Size: 70.3 MB (70335691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6455e54e26cadf3e4e660c96ad33457949304cd7f862649600da0024b0ee6b15`  
		Last Modified: Fri, 27 Mar 2026 19:18:57 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:3efa6055dbc0746f940c38e92161e7b1596428419194bc8f646694d7d9d528dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (40961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2010838a5bbbdd108a559e30d90b116a0b38bf166c5f62f2f4a11a80ba2856`

```dockerfile
```

-	Layers:
	-	`sha256:f91e671ffd8d61951bb7a4b5ce6056d58e5551ace2d8a2f1107a8e5b8936783f`  
		Last Modified: Fri, 27 Mar 2026 19:18:54 GMT  
		Size: 41.0 KB (40961 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:8a532746e96d61b98dbef6098f4857c3557d59d82430215d8b4aa3c8a6e2b1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178201717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9b1fd755fbaff7acb78d549ad0f1a3df937ed386b0d6c8142337b12d1a410b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 27 Mar 2026 18:29:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:01 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:01 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:01 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:01 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:15:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:15:18 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 27 Mar 2026 19:15:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:15:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:15:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 27 Mar 2026 19:15:21 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:15:21 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:15:21 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:15:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:15:21 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:15:21 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:15:21 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:15:21 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:15:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:15:24 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 27 Mar 2026 19:18:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 27 Mar 2026 19:18:07 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:18:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:18:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:18:07 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:18:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b1a7122fb475370726501e7d7eede600bc142474bd65fbd8bebafa70c4ca51`  
		Last Modified: Fri, 27 Mar 2026 18:32:08 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82e0c7ab7b7d81e4d82b1dbcc69bc8aff650c4cab21075d1333afd24553fa4d`  
		Last Modified: Fri, 27 Mar 2026 18:32:10 GMT  
		Size: 29.6 MB (29638983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b26e322273ed2c0c104f81d7e91094eb6afc91a7491a031107badea30482d7`  
		Last Modified: Fri, 27 Mar 2026 18:32:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9254499e41a6c2e8168b9b85ecf557cb790d79e536981381cc54d2122b8bc6f7`  
		Last Modified: Fri, 27 Mar 2026 19:18:17 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbf9b3f75d4bf9d682c721c34bb52dd81417c47ad67f9a847b78b11e2bfff9`  
		Last Modified: Fri, 27 Mar 2026 19:18:20 GMT  
		Size: 71.7 MB (71695746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894a79daf0f5417da1dbd444d2fd6d8bfc88a493949ea1fa8e63131caf612e50`  
		Last Modified: Fri, 27 Mar 2026 19:18:17 GMT  
		Size: 942.4 KB (942410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680231e887fde5433160682ead8b7f3225e422d15fa272ee72be408c1666a64c`  
		Last Modified: Fri, 27 Mar 2026 19:18:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c3a315fe74a927887060b6aa5930de9a11ee7961855ba82040e05f49923a26`  
		Last Modified: Fri, 27 Mar 2026 19:18:19 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85aacf23f2237235ffaea3817ee7f2d4cfb13542e6a5515162c3d667d50708e`  
		Last Modified: Fri, 27 Mar 2026 19:18:19 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178e57c9bb20e7d34fbb40e7bdaf40c21ad07b501235a0d5470b88f3c95b8160`  
		Last Modified: Fri, 27 Mar 2026 19:18:19 GMT  
		Size: 3.3 MB (3254658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc86b289dc7989c7d5c5911bd0a19b76121e61abe1c86788249f7c680712863`  
		Last Modified: Fri, 27 Mar 2026 19:18:22 GMT  
		Size: 69.4 MB (69384111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32accf25e018e447dcc6f2d6305924861f77299fe30f98f7702d016c7fd6fa94`  
		Last Modified: Fri, 27 Mar 2026 19:18:20 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:d8420afc3a5dec021e585a43a1c9725a25852c34acd5bdb7f59916d499f22622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (40961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70359a9795486f6648f3fda43b234b8172ffc92e6edf47ce9cb51c4bfe4d91ff`

```dockerfile
```

-	Layers:
	-	`sha256:0a47edaa68605f0951f3c4c0edeb97f52f00df036a88daf55b37ce6f7316582c`  
		Last Modified: Fri, 27 Mar 2026 19:18:17 GMT  
		Size: 41.0 KB (40961 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:ae5e8f2d2732426e4a9fcb702185f8952eca7c3face8b1e4fe4142e3290858ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191492501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6ffa030f596146ab14ab217ff3547f9373b107c636c48269326cbecd3cfa6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 27 Mar 2026 18:30:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:32:45 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:32:45 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:32:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:32:45 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:32:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:32:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:32:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:32:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:32:45 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:12:42 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:12:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 27 Mar 2026 19:12:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:12:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:12:49 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 27 Mar 2026 19:12:49 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:12:49 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:12:49 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:12:49 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:12:49 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:12:49 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:12:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:12:49 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:12:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:12:52 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 27 Mar 2026 19:15:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 27 Mar 2026 19:15:11 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:15:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:15:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:15:12 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:15:12 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e81fb045d6fe9b5897aeb9ceee175432751f6a37caef3e9b3d65bdeda2bc9e1`  
		Last Modified: Fri, 27 Mar 2026 18:32:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fa1dff9c45d01c92467e43f4e6593f3fca8737e355c853d12774a4539c9e0`  
		Last Modified: Fri, 27 Mar 2026 18:32:54 GMT  
		Size: 33.7 MB (33714340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d99c033235caef667becb0c86e9201cb00fbb2c874efef3cf67b6e51899fdcf`  
		Last Modified: Fri, 27 Mar 2026 18:32:53 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edf4d9729376f23454a3eb3f148ea5c8e3c850b6333ae4d41ae173f675ef4a`  
		Last Modified: Fri, 27 Mar 2026 19:15:23 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae0c8003be07600e4eb01c4d8f4d26029f3b738279011da22088f20dd153058`  
		Last Modified: Fri, 27 Mar 2026 19:15:26 GMT  
		Size: 78.2 MB (78236134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9df634e25753088ed44f17436cb61d08c87f03a57a2459e8d26d5543c7c347`  
		Last Modified: Fri, 27 Mar 2026 19:15:23 GMT  
		Size: 929.5 KB (929498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2930b3fc6e482d540cbea8d614636fa0b8cc9dbf1d779084e26e772f1a9d2860`  
		Last Modified: Fri, 27 Mar 2026 19:15:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69186934a2fa095899f01fdba921143a57c802d9b9f2c5b073e18d2d3e8760e9`  
		Last Modified: Fri, 27 Mar 2026 19:15:25 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ca1a0d9d11cf03188effd78a40f904d6b148f1b5219d6141fe284250fbb8b`  
		Last Modified: Fri, 27 Mar 2026 19:15:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c2611134ff146e5acd3d40ac2833adcf3379417ab279fe2fe535f1645e99f4`  
		Last Modified: Fri, 27 Mar 2026 19:15:25 GMT  
		Size: 3.3 MB (3254671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952d58151930db04eea05c168e11617eeeb36738b3563af0d22646f01b034843`  
		Last Modified: Fri, 27 Mar 2026 19:15:28 GMT  
		Size: 71.2 MB (71156681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996476002f995273df8db0cea8de224073f4c6d8133fcb23799d1bf83392c991`  
		Last Modified: Fri, 27 Mar 2026 19:15:26 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:218918135cce429ec6eae059a1d7b09aace062910c5c37e1541e6954fcb51310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (41005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5ee37bec660fdfe81dbe2500324efc67b105b42f1ac241b05d86ea53896470`

```dockerfile
```

-	Layers:
	-	`sha256:44f40febb32af17c4d3d26b487ba6299ad34bd8c05fb604af4517530646851de`  
		Last Modified: Fri, 27 Mar 2026 19:15:23 GMT  
		Size: 41.0 KB (41005 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; 386

```console
$ docker pull redmine@sha256:2714592354aeab79d03e0e1f4d156b0e066214aa304a74c55c918670b8a734c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188671567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96347da6a1e45c898dd5605e781c6231e614c3044b9f8e3e25601b8b5ab4b742`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 27 Mar 2026 18:31:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:33:17 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:33:17 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:33:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:33:17 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:33:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:33:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:33:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:33:17 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:13:06 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:13:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 27 Mar 2026 19:13:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:13:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:13:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 27 Mar 2026 19:13:13 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:13:13 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:13:13 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:13:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:13:13 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:13:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:13:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:13:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:13:16 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:13:16 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 27 Mar 2026 19:15:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 27 Mar 2026 19:15:21 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:15:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:15:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:15:22 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:15:22 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe62aaf956c72bda9209a40919e78f1b5cfbaea86ab002f94a1c3df5d5038405`  
		Last Modified: Fri, 27 Mar 2026 18:33:24 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45a2d90a35f71f6f1560a23e099d6987f607aa4c90e87d7fc46f7d7d9b0dcb8`  
		Last Modified: Fri, 27 Mar 2026 18:33:25 GMT  
		Size: 29.9 MB (29914972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63c044e648569e5d3478bb3b881b02bab863c0a1e5b65b9b72e7a33915f8043`  
		Last Modified: Fri, 27 Mar 2026 18:33:24 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af89cf6c637cfdb1ba55f1f24c7c20d25a6157228636f738f5cb2b134a0dc40`  
		Last Modified: Fri, 27 Mar 2026 19:15:33 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ff1bebf3e2fbfd246bc25930c5ca3573588829146eb0da3d6bbf71635baa2`  
		Last Modified: Fri, 27 Mar 2026 19:15:36 GMT  
		Size: 79.8 MB (79752344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109170da8c7d334377e44e1efb3127f54705ce10e054fea204fca302f06f1f8c`  
		Last Modified: Fri, 27 Mar 2026 19:15:34 GMT  
		Size: 946.0 KB (946025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7baaba745e04be7798b382f14d4ea5c14df877675b218b935a2405d2a7f3d7`  
		Last Modified: Fri, 27 Mar 2026 19:15:33 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77029742a02100c11e6214881de10a18cb8f6ae49ae6323cf0a3171efb47b13`  
		Last Modified: Fri, 27 Mar 2026 19:15:35 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac1ee86ebaf1c6bfd40de1cd94497ed1756c4f791030d0ec69930b4142e1b95`  
		Last Modified: Fri, 27 Mar 2026 19:15:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db06d30d9fe1b6ba135f0067f460c56f4d0ce0902dcebba3ac796b0464e2f99`  
		Last Modified: Fri, 27 Mar 2026 19:15:35 GMT  
		Size: 3.3 MB (3254678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a82dc7f0bf3f6cfd4f959c5a62817af7c27029fbb9cab0b73a14d1467fc80ef`  
		Last Modified: Fri, 27 Mar 2026 19:15:38 GMT  
		Size: 71.1 MB (71112468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab9c255b608e2f76611e09ed9ee5222e008d649b9c6031095f0821f338d3d6`  
		Last Modified: Fri, 27 Mar 2026 19:15:36 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:4640e02fabed8276d1ce2c39d4fcdec94e1b2596920b33814cba8f74ffd780a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7925a38bc38c1d5cb33d2b0210949ede9bc4405f30bab1493f8b8b2f4244eb`

```dockerfile
```

-	Layers:
	-	`sha256:cb10df6d0782c159dc5596b3fc8a33c8c5c39d3e46c55ae9713e2efc2e5f9b2f`  
		Last Modified: Fri, 27 Mar 2026 19:15:33 GMT  
		Size: 40.7 KB (40733 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:f067f5b240de6261250cb1e6ce0e7da3c739b44c5a043fbaca816987e9fb2de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193879961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72642a27c462834672f26adafa0cb61b9b7df98206329ecec158aecff1c96d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 26 Mar 2026 18:34:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:40:34 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:40:34 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:40:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:40:34 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:40:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:40:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:40:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:40:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:40:34 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:40:34 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:39:46 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:39:57 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 27 Mar 2026 19:40:02 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:40:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:40:03 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 27 Mar 2026 19:40:03 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:40:03 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:40:03 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:40:03 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:40:03 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:40:03 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:40:03 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:40:03 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:40:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:40:06 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 27 Mar 2026 19:44:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 27 Mar 2026 19:44:00 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:44:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:44:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:44:01 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:44:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a97b0a36dbb50731bca14fb29ac81d179cd2af8c835ae8c12f79d944f2eac4`  
		Last Modified: Thu, 26 Mar 2026 18:37:47 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c547b8b66096fa3a6ad7325d643a7636ef04a242951a276e05aafae09638225`  
		Last Modified: Fri, 27 Mar 2026 18:40:52 GMT  
		Size: 31.3 MB (31347943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024269172d5e545eb533d062a85d95b3563f2d3bb7b0c40a1efec948c0dac7b9`  
		Last Modified: Fri, 27 Mar 2026 18:40:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f080a6f41c0cfc96033206f69de9c7bb353d1e083b6f284c124800bcb88bac`  
		Last Modified: Fri, 27 Mar 2026 19:44:29 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f25d4f48c0584e35b84ec500a01fde292fd121288ea07a524854fb2f3bffecb`  
		Last Modified: Fri, 27 Mar 2026 19:44:32 GMT  
		Size: 81.3 MB (81311377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2448ac8090dc6f66634fa3fe6f0c706a6f6ecd6168c96f808d0b0492372e972`  
		Last Modified: Fri, 27 Mar 2026 19:44:30 GMT  
		Size: 934.6 KB (934574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd391604abf216b6ba2a6bc1f6d2ffd0d32c57ac51fe17b9e01d2d7512ed0b`  
		Last Modified: Fri, 27 Mar 2026 19:44:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1000c85ea1b82957d1fdbacf4b758c5a626170a0970a5e8692ff217b06b8138`  
		Last Modified: Fri, 27 Mar 2026 19:44:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40259dc72c9252dbbc466ef30dbad7691fbacd1abed1118424a2b025c343ecb9`  
		Last Modified: Fri, 27 Mar 2026 19:44:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764af038eb5ea97122e2a15adcce693abf78d83a9588a1b1ca772227421486c4`  
		Last Modified: Fri, 27 Mar 2026 19:44:31 GMT  
		Size: 3.3 MB (3254698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135864c8f794cfc6a36d30d11ad768f156c800f03b4a9b42fb1df311877c7489`  
		Last Modified: Fri, 27 Mar 2026 19:44:35 GMT  
		Size: 73.2 MB (73197639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b66b98502674ad5336a3d1da4c8e86409cf0d14941a3121056b34beb77bc1f0`  
		Last Modified: Fri, 27 Mar 2026 19:44:32 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:89caaed6e2e7da78ea84f05efc6a7b78b6261ebb39bfbc2568e8531d92dc2944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cee340f6e5da141358441f341904fadf00995bc522189e5b1cd29794898932`

```dockerfile
```

-	Layers:
	-	`sha256:a5c69e0b25873d1fb85d8780963242b95b4d4307b0017a11626b088b5bb0d16b`  
		Last Modified: Fri, 27 Mar 2026 19:44:29 GMT  
		Size: 40.9 KB (40855 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:a7b102230fe8eb8832d06d2bed92b72f12e1d89b25e7701b367e3d708321a28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193237495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99624b3156dffaa8f5defa9a65ce54cc27ec983e15098c13feeaa018c48146da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 20 Mar 2026 03:56:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 28 Mar 2026 22:08:31 GMT
ENV LANG=C.UTF-8
# Sat, 28 Mar 2026 22:08:31 GMT
ENV RUBY_VERSION=3.2.11
# Sat, 28 Mar 2026 22:08:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Sat, 28 Mar 2026 22:08:31 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Sat, 28 Mar 2026 22:08:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 28 Mar 2026 22:08:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 28 Mar 2026 22:08:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 28 Mar 2026 22:08:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Mar 2026 22:08:32 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 28 Mar 2026 22:08:32 GMT
CMD ["irb"]
# Sat, 28 Mar 2026 23:09:04 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 28 Mar 2026 23:09:38 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sat, 28 Mar 2026 23:09:48 GMT
ENV GOSU_VERSION=1.19
# Sat, 28 Mar 2026 23:09:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 28 Mar 2026 23:09:48 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sat, 28 Mar 2026 23:09:48 GMT
ENV RAILS_ENV=production
# Sat, 28 Mar 2026 23:09:48 GMT
WORKDIR /usr/src/redmine
# Sat, 28 Mar 2026 23:09:48 GMT
ENV HOME=/home/redmine
# Sat, 28 Mar 2026 23:09:49 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 28 Mar 2026 23:09:49 GMT
ENV REDMINE_VERSION=5.1.12
# Sat, 28 Mar 2026 23:09:49 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Sat, 28 Mar 2026 23:09:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Sat, 28 Mar 2026 23:09:49 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 28 Mar 2026 23:09:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 28 Mar 2026 23:09:54 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 29 Mar 2026 00:09:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 29 Mar 2026 00:09:09 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 29 Mar 2026 00:09:10 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 29 Mar 2026 00:09:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 29 Mar 2026 00:09:10 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 29 Mar 2026 00:09:10 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efa6bf1e70e288fe8840de5f584b4b4821864fcce54bff52f681d2441413a2a`  
		Last Modified: Fri, 20 Mar 2026 06:17:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686ad3b74df2eb1553854e0775845a1581ab06bb7bdac44ed5614447727a0478`  
		Last Modified: Sat, 28 Mar 2026 22:09:37 GMT  
		Size: 32.3 MB (32294796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3719ed346201cb1236541b4e6f6363d9fb6752c43b7b8d516249cc64cc2e4a`  
		Last Modified: Sat, 28 Mar 2026 22:09:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1bc8bbd9c0795e07948957230eb3f9e7c0d19c6c8107cab0966a3dc25ad331`  
		Last Modified: Sun, 29 Mar 2026 00:11:08 GMT  
		Size: 907.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18c421d8b91003bc09feb2d72d90f5d4b5de3ad537b4a92813dfb68ba39739d`  
		Last Modified: Sun, 29 Mar 2026 00:11:29 GMT  
		Size: 77.0 MB (76963462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bd39ba9b6cb848986782f76c5cb30c2f40472ee2e2cecd143f408df0066b4c`  
		Last Modified: Sun, 29 Mar 2026 00:11:08 GMT  
		Size: 921.9 KB (921858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cc9790989f1cd4b45d9d7110452e136ee605772fb4f5aff9ecb2b01f702825`  
		Last Modified: Sun, 29 Mar 2026 00:11:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bb2ee2c813cd8d0a26139fea8727ca57c928e0bb4f34f511b913a76800bc44`  
		Last Modified: Sun, 29 Mar 2026 00:11:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3c961d76bb7814c1aae32be329fb43ff7b1da07ca3bfdecedf3eca3657eef0`  
		Last Modified: Sun, 29 Mar 2026 00:11:09 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3aee16a12095491f2d9bce9c22044d4c8c2b73ae4a4382dc70878d3417341c`  
		Last Modified: Sun, 29 Mar 2026 00:11:10 GMT  
		Size: 3.3 MB (3254702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc74925c033f9b56f6c64c266b015d8a1e2db9a8e0c6be66cf1dab11bfd3b1`  
		Last Modified: Sun, 29 Mar 2026 00:11:31 GMT  
		Size: 76.2 MB (76213310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055a0fd69b15242dcc311c87f6f7943a5bd5fc9ef9a82332861cdfcb8e91a02a`  
		Last Modified: Sun, 29 Mar 2026 00:11:11 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:e63baad5408d524f3c118a1863e8ca8c63009826f84a476af7a5448864797e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74c494feced6677e4776950bb1db1e63cf65d751c423ecab916df32cc878cca`

```dockerfile
```

-	Layers:
	-	`sha256:b14e64e12f6aede534fdcdcdb5375eae249daa674e62b91aef1aec7220b66030`  
		Last Modified: Sun, 29 Mar 2026 00:11:08 GMT  
		Size: 40.9 KB (40855 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:6a2706d5eabf0950160386d34719c32671d4f600d0d47cff1471441e9570eea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190071902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6da34e78564d7f0fafae4f0c9f8f956ac4b4ea2fb6cccbcc2bb6d1efeeea314`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 27 Mar 2026 18:31:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:33:44 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:33:44 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:33:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:33:44 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:33:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:33:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:33:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:33:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:33:44 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:11:38 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:11:43 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 27 Mar 2026 19:11:46 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:11:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:11:46 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 27 Mar 2026 19:11:46 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:11:46 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:11:46 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:11:46 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:11:46 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:11:46 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:11:46 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:11:46 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:11:48 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:11:48 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 27 Mar 2026 19:14:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 27 Mar 2026 19:14:13 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:14:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:14:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:14:14 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:14:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2183342bea907f15163637d6c7108e5bb98437f431f69d2378abd3f5313c9ccd`  
		Last Modified: Fri, 27 Mar 2026 18:33:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f4a5b359602aac9e230e23653b01d31444fc4bb0bb56e76f3bf7a2a3caef25`  
		Last Modified: Fri, 27 Mar 2026 18:33:57 GMT  
		Size: 30.9 MB (30936029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4344936c98c1170dab91eddd0de6ef16ec901de90f58b88028be2455f5ef0d60`  
		Last Modified: Fri, 27 Mar 2026 18:33:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea793d177073dab73fd36434791a642d31d5ebe29e84e93bde0f244bfcdc0d16`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46f1986719a85ee2b6f3b8a905d3f15627dff284a73666471ed0ef6befa590b`  
		Last Modified: Fri, 27 Mar 2026 19:14:35 GMT  
		Size: 79.0 MB (78995883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c92925e7b4379a3b8cc03c6d6ffe12335a1d61b3f03017fc633a9946dd58dba`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 950.3 KB (950309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5c14f734d80d0f44496438094868d1dc01deee899cf7e2ebe6a53bc20ce63a`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1812a931522cc8fbf015cd3b3b58a2eb0b9c1222bd70dfc121c9dffaee89195`  
		Last Modified: Fri, 27 Mar 2026 19:14:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897fc1e8c29bcb10cb964168dcfa37434c4464360410bea13412ee3e22aaaaa8`  
		Last Modified: Fri, 27 Mar 2026 19:14:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ba329e9df1b786afff14685bc91e71a3b66f9ea7295b4b5401362a5ca03713`  
		Last Modified: Fri, 27 Mar 2026 19:14:34 GMT  
		Size: 3.3 MB (3254672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14be52b14618bbe92b0ca675ae4a17792583a9dbea9434372587f46f55489e9`  
		Last Modified: Fri, 27 Mar 2026 19:14:36 GMT  
		Size: 72.2 MB (72205588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd2150c936202c232b6de6189c102ee3c09bf9a5bfd9800b835e6dd1081f9a2`  
		Last Modified: Fri, 27 Mar 2026 19:14:34 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:9fe8e5d6b5fdc3a83d8d142e837e87f626904882a606d977090aa54500fb744b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152b27f58519ad07f9c139219b1b6f5f47b16d7114f52dd2187f81ec73248dbc`

```dockerfile
```

-	Layers:
	-	`sha256:24007ac5b60684e22d364e624fdef86bc7ff6201230d3ee08b9be75c551a9242`  
		Last Modified: Fri, 27 Mar 2026 19:14:32 GMT  
		Size: 40.8 KB (40787 bytes)  
		MIME: application/vnd.in-toto+json
