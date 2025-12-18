## `redmine:alpine3.22`

```console
$ docker pull redmine@sha256:3284da4d9a25ff2178b2051ad5fc51a1d76536375acf5de02a771a679b9fc41b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `redmine:alpine3.22` - linux; amd64

```console
$ docker pull redmine@sha256:19045cd4374b342c13c21751a21f7478b6e302db346bf3489171005c2a74c519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190359202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee7e393ff0351962e6a3b276b13c1970fe00a8aa28f8741c27a27e293486c5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 20:06:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:08:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:08:53 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:08:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:08:53 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:08:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:08:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:08:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:08:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:08:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:08:53 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:12:04 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 17 Dec 2025 21:12:09 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 17 Dec 2025 21:12:11 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Dec 2025 21:12:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Dec 2025 21:12:11 GMT
ENV RAILS_ENV=production
# Wed, 17 Dec 2025 21:12:11 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Dec 2025 21:12:11 GMT
ENV HOME=/home/redmine
# Wed, 17 Dec 2025 21:12:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 17 Dec 2025 21:12:11 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 17 Dec 2025 21:12:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 17 Dec 2025 21:12:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 17 Dec 2025 21:12:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 17 Dec 2025 21:12:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 17 Dec 2025 21:12:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Dec 2025 21:12:41 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Dec 2025 21:12:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 21:12:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:12:41 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 17 Dec 2025 21:12:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7115cc2ce86375650231038e1151173fc3cfcbc1077ba2e8d8a5a162e62d92c`  
		Last Modified: Wed, 17 Dec 2025 20:09:08 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e3f4f891ced55198697cd10c4ba3afb312f6df9859686613f7b8c89d6a424`  
		Last Modified: Wed, 17 Dec 2025 20:09:12 GMT  
		Size: 39.3 MB (39275442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133a16c53999e27764b899a47440a728b47e4d52aff0ac21efe6796d422756a8`  
		Last Modified: Wed, 17 Dec 2025 20:09:08 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac64b424bbf6b577ba76449e9353a0a538a98766bdb1a32a7804b17cec8cf283`  
		Last Modified: Wed, 17 Dec 2025 21:13:03 GMT  
		Size: 915.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b957bff4fc0b7a559990ac82dadd70014217ea8f93080dae0216b295e8ae8a`  
		Last Modified: Wed, 17 Dec 2025 21:13:08 GMT  
		Size: 75.4 MB (75408082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789aec18d339407a97226af79e0fa6953d980149e337a175d0238640b531d278`  
		Last Modified: Wed, 17 Dec 2025 21:13:03 GMT  
		Size: 966.7 KB (966678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea732117267f99e191ca3834c37ac697d66ae3e9af57a133693b88aaf72289b2`  
		Last Modified: Wed, 17 Dec 2025 21:13:02 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e2a6b9fac1ce22f63b73256110bf5ebf9c88ae0243755cfe924c83df0c673a`  
		Last Modified: Wed, 17 Dec 2025 21:13:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f974e30504a79f176dcd0ce5432fce8cfa00c91f904c1866963c994bfbe9124`  
		Last Modified: Wed, 17 Dec 2025 21:13:03 GMT  
		Size: 4.1 MB (4140758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6430565149976096f64b54363efc4140e74773ed9811f874c648e69daa32e3a2`  
		Last Modified: Wed, 17 Dec 2025 21:13:10 GMT  
		Size: 66.8 MB (66761871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498988ba9406e882ce4200ce56968482d944999f9affa0ca571144ab1618c8ac`  
		Last Modified: Wed, 17 Dec 2025 21:13:03 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:b781e6f8e526bb15436ccda9e2963d557c0b080ea5fb13e2c58c76bdd2a6b125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae183c9c09fc09aa65073ccfa36d9202561a70efed3ca08abed974ce9f18d44`

```dockerfile
```

-	Layers:
	-	`sha256:d1fc64431d9828141f5bb0915a8ce2d1689dd4d88a2dc05c5d1e217c86d796ec`  
		Last Modified: Wed, 17 Dec 2025 23:51:17 GMT  
		Size: 36.7 KB (36748 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; arm variant v7

```console
$ docker pull redmine@sha256:aa64daef2f90848f05d4fb92389a3a2dd14c261f52533ce26d09a3a056b6cd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194401614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403fde9b0e0002a75cd203bb01623c931a2c7062731ff7e3377a9c70b996ab37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 20:07:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:09:47 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:09:47 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:09:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:09:47 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:09:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:09:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:09:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:09:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:09:47 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:13:39 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 17 Dec 2025 21:13:53 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 17 Dec 2025 21:13:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Dec 2025 21:13:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Dec 2025 21:13:57 GMT
ENV RAILS_ENV=production
# Wed, 17 Dec 2025 21:13:57 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Dec 2025 21:13:57 GMT
ENV HOME=/home/redmine
# Wed, 17 Dec 2025 21:13:57 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 17 Dec 2025 21:13:57 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 17 Dec 2025 21:13:57 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 17 Dec 2025 21:13:57 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 17 Dec 2025 21:13:57 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 17 Dec 2025 21:13:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 17 Dec 2025 21:15:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Dec 2025 21:15:21 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Dec 2025 21:15:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 21:15:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:15:21 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 17 Dec 2025 21:15:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf316c569d5e6640d33cdb160d1d9d43f3dda4c3d3ec6f9ae1574a241ab047cb`  
		Last Modified: Wed, 17 Dec 2025 20:10:04 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c9a4592f6d140412eb7de6a9bd99377c1452f0a2027cfc582160dab4e8ea53`  
		Last Modified: Wed, 17 Dec 2025 20:10:06 GMT  
		Size: 34.8 MB (34769256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251bf51ce5c9b36c6991c3a5b8873950f754e0cd2cebe904114facfca45021d`  
		Last Modified: Wed, 17 Dec 2025 20:10:02 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411ae06815ee4f9306150f1d6dbbb456e1bbc7b209fd30e270e37292943665ff`  
		Last Modified: Wed, 17 Dec 2025 21:15:42 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c20182576c2efb2f74536a6c3ea55df7077e0a5c49b40fc57c682c55ddd366`  
		Last Modified: Wed, 17 Dec 2025 21:15:49 GMT  
		Size: 69.0 MB (68989150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609787a3207966668f410de09725ca172a348536fef71fab8574ab671140150f`  
		Last Modified: Wed, 17 Dec 2025 21:15:41 GMT  
		Size: 934.7 KB (934673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c678782251681010ff823b440bd7aa62f328ddf79b5be7744f939430149ec20`  
		Last Modified: Wed, 17 Dec 2025 21:15:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113523c96c002c285e58370c81fa6362b00a176840a2e2f058f24419321aebe2`  
		Last Modified: Wed, 17 Dec 2025 21:15:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e759aa641360b886870b1d4daa92804f12c9c90ce7715340cc19799a8437ac`  
		Last Modified: Wed, 17 Dec 2025 21:15:41 GMT  
		Size: 4.1 MB (4140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aca407c39458da69284cf837a31cf4bac4176084c25b0ec4eb5b41cc5259b5`  
		Last Modified: Wed, 17 Dec 2025 21:15:50 GMT  
		Size: 82.3 MB (82342191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a2f85a03df7097bb319470425e679a1ee360a28b8c2a2302beaf58135196ef`  
		Last Modified: Wed, 17 Dec 2025 21:15:41 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:5b5caf9f1f580c6c0c9a1e64c3e790d8f472df414e8adacf40496f39b29b5b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac7c71fdf9307d48ad438c2f8e5944137723917fcc1b545145f7aa1b026e4fd`

```dockerfile
```

-	Layers:
	-	`sha256:5b88d8153f57fb0dc61e1481e3cd0bb98250e01519c5085cd7209e464673176b`  
		Last Modified: Wed, 17 Dec 2025 23:51:21 GMT  
		Size: 36.9 KB (36893 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:ef489738f5b4bb9494b28b3a5641f333fee3333f4f4db49a9130cac4d626ab12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190071217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60218ff40d756130b05fd9c4af9f9a48595e4da7baccd702e5f7044f166b2a50`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 20:07:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:09:54 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:09:54 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:09:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:09:54 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:09:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:09:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:09:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:09:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:09:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:09:54 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:13:04 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 17 Dec 2025 21:13:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 17 Dec 2025 21:13:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Dec 2025 21:13:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Dec 2025 21:13:13 GMT
ENV RAILS_ENV=production
# Wed, 17 Dec 2025 21:13:13 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Dec 2025 21:13:13 GMT
ENV HOME=/home/redmine
# Wed, 17 Dec 2025 21:13:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 17 Dec 2025 21:13:13 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 17 Dec 2025 21:13:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 17 Dec 2025 21:13:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 17 Dec 2025 21:13:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 17 Dec 2025 21:13:15 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 17 Dec 2025 21:13:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Dec 2025 21:13:45 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Dec 2025 21:13:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 21:13:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:13:45 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 17 Dec 2025 21:13:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ddf0f51a1f142bf8dea9d6125f86304658cd041b98fa064a62e46a4394110d`  
		Last Modified: Wed, 17 Dec 2025 20:10:08 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a95de64a39bc16258d004d406a2982268d1ff6c2d7e25e8d9a9429a41bda7e`  
		Last Modified: Wed, 17 Dec 2025 20:10:11 GMT  
		Size: 39.2 MB (39186731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057a0397de8d57a5f0ba88f78f2173423330c1463f45a6d53b08bba80c5ae45`  
		Last Modified: Wed, 17 Dec 2025 20:14:40 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5597d93b2abd837865e6152a942502ef04d5e32f1755bb547cef9247bc738356`  
		Last Modified: Wed, 17 Dec 2025 21:14:07 GMT  
		Size: 915.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de04d485c55b5d34f0a20f5b060009f063824f86acedc5885b08b5302382c695`  
		Last Modified: Wed, 17 Dec 2025 21:14:18 GMT  
		Size: 75.1 MB (75059967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3897e36647b77573ad8ac94139a77a6b2ce6d112cd65f86d6173d27b1b9452cd`  
		Last Modified: Wed, 17 Dec 2025 21:14:06 GMT  
		Size: 922.2 KB (922186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6947f4cc8fe1d370e7037e2b5214eea42532f76f7a03b5c426363176bc0fef1`  
		Last Modified: Wed, 17 Dec 2025 21:14:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f364403bfcd8ffb96ecf0b30101faceea6d32963a9866e8c0a423b299deb069`  
		Last Modified: Wed, 17 Dec 2025 21:14:06 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf34b2441d9ac0b2c858cd4232ff7c6c4ca3db3e771ed88bcc66e53c3ae425d`  
		Last Modified: Wed, 17 Dec 2025 21:14:06 GMT  
		Size: 4.1 MB (4140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd7480b42a0e01b941813ca6a06ce6e1cd0448046ad8ae199f8ff9525a30afe`  
		Last Modified: Wed, 17 Dec 2025 21:14:18 GMT  
		Size: 66.6 MB (66619472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198672b6f39175bea721c52c97e5e1912caaa6d9e91b06ee3e3e6f1e2cddf95f`  
		Last Modified: Wed, 17 Dec 2025 21:14:06 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:f7fd97173609e7b1db34f4f4e957e9e2cb425962daa212197badb3c45cd8df05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db3b71822ade204ef07095483cddfa126ccd99265b9f6283f7d584ed5d90b79`

```dockerfile
```

-	Layers:
	-	`sha256:dde784dc1c3b7d425ae3b55216b5378c04a064bd2858d88f208bb83c0f3aa465`  
		Last Modified: Wed, 17 Dec 2025 23:51:24 GMT  
		Size: 36.9 KB (36927 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; 386

```console
$ docker pull redmine@sha256:209298cab639e28f98fdd607af4f8f11d5f285a835a24411eb46eec8c97f2551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207867271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf1e6c4d514349612a755b1fe6c76067cbbb20ff253cc0c2648c564463fb4cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 20:06:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:08:30 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:08:30 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:08:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:08:30 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:08:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:08:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:08:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:08:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:08:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:08:30 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:12:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 17 Dec 2025 21:13:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 17 Dec 2025 21:13:15 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Dec 2025 21:13:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Dec 2025 21:13:15 GMT
ENV RAILS_ENV=production
# Wed, 17 Dec 2025 21:13:15 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Dec 2025 21:13:15 GMT
ENV HOME=/home/redmine
# Wed, 17 Dec 2025 21:13:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 17 Dec 2025 21:13:15 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 17 Dec 2025 21:13:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 17 Dec 2025 21:13:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 17 Dec 2025 21:13:15 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 17 Dec 2025 21:13:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 17 Dec 2025 21:15:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Dec 2025 21:15:34 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Dec 2025 21:15:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 21:15:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:15:34 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 17 Dec 2025 21:15:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec07caffba4afe4bb6f30ead8d6baa56845cab3a2fb0f95cb9c33c1d24a8a659`  
		Last Modified: Wed, 17 Dec 2025 20:08:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cd2c761e808c907de767bcf9aa434cf67db67996753a72cecbb28090c16d2e`  
		Last Modified: Wed, 17 Dec 2025 20:08:52 GMT  
		Size: 34.8 MB (34775876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee04004094c443c6a2b3df20ec9b614193848822f7f7f2f1ebd42c247e32114`  
		Last Modified: Wed, 17 Dec 2025 20:08:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7973493012e59d2683071140e97440fb64b1dbca48fef95649386cd684a8bf5`  
		Last Modified: Wed, 17 Dec 2025 21:16:15 GMT  
		Size: 915.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691ffb742ccb8f1da5ba3114bc850a0c44bab498d8f8aaa05ee8ef4a231abb6c`  
		Last Modified: Wed, 17 Dec 2025 21:16:11 GMT  
		Size: 76.2 MB (76186150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2987fb2b600e80051d8b8b78e4788bc327787da81618a80c96b3f01b683d9714`  
		Last Modified: Wed, 17 Dec 2025 21:16:05 GMT  
		Size: 939.2 KB (939218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fe4f6cc399069739c8672543bf7e7e3a73d6284e4b684cfb9db016354c9b6`  
		Last Modified: Wed, 17 Dec 2025 21:16:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea159023431b42f2a3a78a8299737949ab664de4a2f761c71dbfcbd48ac4c52f`  
		Last Modified: Wed, 17 Dec 2025 21:16:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c36ed51920e1fd0803e5d2e84ea88485eb225f8b1b9afd2e43f09dbe99e1ff`  
		Last Modified: Wed, 17 Dec 2025 21:16:07 GMT  
		Size: 4.1 MB (4140762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e635d385fd7592cfbf730d35a9292e8dc323f0a1753e7db52be9cd9fc8da94`  
		Last Modified: Wed, 17 Dec 2025 21:16:18 GMT  
		Size: 88.2 MB (88202416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef6d870c78f46d2c85d5b7337b3da5407dba3f82e3af4d7d8ce9e1fe17dbba7`  
		Last Modified: Wed, 17 Dec 2025 21:16:05 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:bb63ed37f957454beab7d386d3f7b0f4be741c09f34711035f84b8c02cb78e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21239e0975e6ee8810017e2a58921ad0d6ad5b5a61be14bf407f3591aafb73b6`

```dockerfile
```

-	Layers:
	-	`sha256:e5710db193c55df3025fc377245eabaeeb6d755b58897b26553ca477851165de`  
		Last Modified: Wed, 17 Dec 2025 23:51:28 GMT  
		Size: 36.7 KB (36706 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; ppc64le

```console
$ docker pull redmine@sha256:da3135895e0ad2ee00b447c790f3ce6e9cda12819b5119e0b9df710fa9c56df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226463013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237e451735f9dccb35e78a757646107c9ad68b71ff5c592f8fe13b3c927c7410`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 20:03:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:16:38 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:16:38 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:16:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:16:38 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:16:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:16:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:16:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:16:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:16:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:16:39 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:16:34 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 17 Dec 2025 21:16:59 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 17 Dec 2025 21:17:06 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Dec 2025 21:17:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Dec 2025 21:17:06 GMT
ENV RAILS_ENV=production
# Wed, 17 Dec 2025 21:17:07 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Dec 2025 21:17:07 GMT
ENV HOME=/home/redmine
# Wed, 17 Dec 2025 21:17:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 17 Dec 2025 21:17:08 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 17 Dec 2025 21:17:08 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 17 Dec 2025 21:17:08 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 17 Dec 2025 21:17:08 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 17 Dec 2025 21:17:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 17 Dec 2025 21:21:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Dec 2025 21:21:01 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Dec 2025 21:21:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 21:21:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:21:01 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 17 Dec 2025 21:21:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdf3e5b236174bf8a7f72eebdcbe39f5672bf2333fec5ff0bb140b22fcddbdb`  
		Last Modified: Tue, 09 Dec 2025 20:07:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be075c3072d1f4ba2b5608d6080f9b73a678bb789f4db5846d9a328b4d925d2`  
		Last Modified: Wed, 17 Dec 2025 20:17:09 GMT  
		Size: 36.4 MB (36429326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7684d3e45e9b9b45e286957dbdf9fd911fc68f5e1f2f3d2788114b1cecdad7e`  
		Last Modified: Wed, 17 Dec 2025 20:17:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b500563b78c9ab746ed536006332c976ba431fcc1acf75da570b6665fbd63130`  
		Last Modified: Wed, 17 Dec 2025 21:21:36 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eca1d6ad1e99b560b8969cbec4fca282d1fa1de26a5d68eaa46f999ecafa904`  
		Last Modified: Wed, 17 Dec 2025 21:21:52 GMT  
		Size: 77.5 MB (77514154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd0f2cb2bbcc13cb0804acefadc18a07ba9bdd50f9ba460ee4176dc9174e8ba`  
		Last Modified: Wed, 17 Dec 2025 21:21:36 GMT  
		Size: 927.7 KB (927714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7e3c200aa74b72a82de1da4ac0db8996437e6b70a1229b7d98c9113af4f615`  
		Last Modified: Wed, 17 Dec 2025 21:21:36 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938de92edfe7261a83063205e7c84717257a7bb1a51f4f42cc85ff7317f31ce`  
		Last Modified: Wed, 17 Dec 2025 21:21:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a307de9f6de2875e510d46be66e34a45089dd583cd97dd68d0a52483a9edd56`  
		Last Modified: Wed, 17 Dec 2025 21:21:37 GMT  
		Size: 4.1 MB (4140875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7b8656b24bc749349e5387863af0b9a08cbbac6279beefe285577ccdd73698`  
		Last Modified: Wed, 17 Dec 2025 21:21:45 GMT  
		Size: 103.7 MB (103714785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0109d648875d32572587fa8db2714321b64f2e82fd8e05643ecfaa4607bb8111`  
		Last Modified: Wed, 17 Dec 2025 21:21:36 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:1129101e3edc0866f0e328d741bba0d1b709bdc4b4d16d7507568a1cecb6586f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb34fec498ea71ccdb7b2bbf8358f58e4a89837ac4bcb9ef9648b12df57d7be`

```dockerfile
```

-	Layers:
	-	`sha256:255019ed4548ab83e2729ad6fc6cbfa449fc90e471dbc033522f686cc649ebe4`  
		Last Modified: Wed, 17 Dec 2025 23:51:31 GMT  
		Size: 36.8 KB (36803 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; riscv64

```console
$ docker pull redmine@sha256:980eb45090976235d40b3deed7fc5b75c90949c90fe846921e26c19f94992db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220598669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c678991b8d0d9f0b95159c2f304b52d1c655ccd654e1f0020586feb2fbc984`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 13 Dec 2025 01:39:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 13 Dec 2025 10:24:45 GMT
ENV LANG=C.UTF-8
# Sat, 13 Dec 2025 10:24:45 GMT
ENV RUBY_VERSION=3.4.7
# Sat, 13 Dec 2025 10:24:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Sat, 13 Dec 2025 10:24:45 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Sat, 13 Dec 2025 10:24:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 13 Dec 2025 10:24:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Dec 2025 10:24:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Dec 2025 10:24:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 10:24:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 13 Dec 2025 10:24:46 GMT
CMD ["irb"]
# Sun, 14 Dec 2025 19:53:49 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 14 Dec 2025 19:54:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 14 Dec 2025 19:54:43 GMT
ENV GOSU_VERSION=1.19
# Sun, 14 Dec 2025 19:54:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 14 Dec 2025 19:54:43 GMT
ENV RAILS_ENV=production
# Sun, 14 Dec 2025 19:54:43 GMT
WORKDIR /usr/src/redmine
# Sun, 14 Dec 2025 19:54:43 GMT
ENV HOME=/home/redmine
# Sun, 14 Dec 2025 19:54:43 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 14 Dec 2025 19:54:43 GMT
ENV REDMINE_VERSION=6.1.0
# Sun, 14 Dec 2025 19:54:43 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Sun, 14 Dec 2025 19:54:43 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Sun, 14 Dec 2025 19:54:43 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 14 Dec 2025 19:54:49 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 14 Dec 2025 21:11:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 14 Dec 2025 21:11:26 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 14 Dec 2025 21:11:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 14 Dec 2025 21:11:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 14 Dec 2025 21:11:27 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 14 Dec 2025 21:11:27 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26b0bd4ba0001e62e053563ad2589e2ee25243368f3dce76bed85b6313b4567`  
		Last Modified: Sat, 13 Dec 2025 03:34:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed194b5fc4d53bbfecff4347f3c8036db2b6e95cee9f1cbff0af68c4f4525cc`  
		Last Modified: Sat, 13 Dec 2025 10:26:07 GMT  
		Size: 34.9 MB (34947716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b68aabe0b66d9b6aba13cbff2bb1d7a276bd87a0214a0666ef9cd4e85f2aa`  
		Last Modified: Sat, 13 Dec 2025 10:26:05 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54adc7cad21707f8e042ae984bf6fb32221680135081a5a8af9400728baec30b`  
		Last Modified: Sun, 14 Dec 2025 21:14:24 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a50a58361fd15c648fd75e399be478b83a2c57355d084178e4eb50bf8a129a`  
		Last Modified: Sun, 14 Dec 2025 21:14:32 GMT  
		Size: 72.3 MB (72324727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41708367234f3b3c8bf6682da9c4ba21d0bd960c070366ef679124bfc20ec441`  
		Last Modified: Sun, 14 Dec 2025 21:14:24 GMT  
		Size: 915.2 KB (915169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc9eaf39fb6ef870cbf09b37d6ab39cdb98b7781a6abec012ba39e483db892b`  
		Last Modified: Sun, 14 Dec 2025 21:14:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861bd975af5682d1a4b2c4e4bbd9e16f05401bf775e1a41204210f18bca71bfd`  
		Last Modified: Sun, 14 Dec 2025 21:14:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a2e5350cd917e92777ae0583015b39ea3ba2402bc7f070094eb9a294dc6e5f`  
		Last Modified: Sun, 14 Dec 2025 21:14:24 GMT  
		Size: 4.1 MB (4140943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d00e103a80da7e465f24f9f2dafbb1c4ec72c5851b5115b09e3a4667a437396`  
		Last Modified: Sun, 14 Dec 2025 21:14:33 GMT  
		Size: 104.8 MB (104750958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5865f525c1a2ea55ed4a430d7feecf9b9d605c22def9c888a5aeb25741f49f`  
		Last Modified: Sun, 14 Dec 2025 21:14:24 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:f56c7d580b36d0980cc1f30d6dbc5a209b7230ed30b2d1f06b64e222d68069d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea84eee7fb93371d13ce221b709b735ef73d35691239a60b4d0d9e9bab512f4`

```dockerfile
```

-	Layers:
	-	`sha256:bb565518673ad06d722a03b43830f2245fcb2f26cf04b8f9d384c9987b90c694`  
		Last Modified: Sun, 14 Dec 2025 23:49:55 GMT  
		Size: 36.8 KB (36802 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; s390x

```console
$ docker pull redmine@sha256:d3ed6e41a670a1914db1b07282056b9b7dd08750308c82ebb207213481e79803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221941368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f424929d5f9f4c7ca70cbc563ac4cffb77a371ee8e8da1f6d9c138d2621cbf25`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 19:56:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:08:24 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:08:24 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:08:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:08:24 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:08:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:08:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:08:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:08:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:08:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:08:24 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:10:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 17 Dec 2025 21:10:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 17 Dec 2025 21:10:17 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Dec 2025 21:10:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Dec 2025 21:10:17 GMT
ENV RAILS_ENV=production
# Wed, 17 Dec 2025 21:10:17 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Dec 2025 21:10:17 GMT
ENV HOME=/home/redmine
# Wed, 17 Dec 2025 21:10:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 17 Dec 2025 21:10:17 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 17 Dec 2025 21:10:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 17 Dec 2025 21:10:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 17 Dec 2025 21:10:17 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 17 Dec 2025 21:10:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 17 Dec 2025 21:12:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Dec 2025 21:12:47 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Dec 2025 21:12:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 21:12:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:12:47 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 17 Dec 2025 21:12:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559a492a9261e799874f27f97a8210839dee9952835594c19282c304847eaf8b`  
		Last Modified: Tue, 09 Dec 2025 20:00:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12ccd0f097ea2957b693f6a9b7c79a8bca9591519603a470de8b89a98930be3`  
		Last Modified: Wed, 17 Dec 2025 20:08:48 GMT  
		Size: 36.2 MB (36219558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428d3812d8e4bc892905f9f71c0a20b0104bef13f749226c76b03f61a1952225`  
		Last Modified: Wed, 17 Dec 2025 20:08:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013674c156424a2db0072271865130ffdbcd002b9b2707733f2ba8587784af8f`  
		Last Modified: Wed, 17 Dec 2025 21:13:25 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfd82f2bd2eb20f2c4c84f77f868aa13b4e920f38eee42aa59f89b19d2d36d2`  
		Last Modified: Wed, 17 Dec 2025 21:13:31 GMT  
		Size: 74.4 MB (74418326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f926474b83bdce00b03e66342382235580838c5507aca13a8fbb8b445cdb2e2`  
		Last Modified: Wed, 17 Dec 2025 21:13:25 GMT  
		Size: 943.2 KB (943206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5234518087065daf94f5e9ac1149d41f7d92e1a6abc6882c2a5ae2b1838eafe`  
		Last Modified: Wed, 17 Dec 2025 21:13:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1db18e6776cc2a424a913b1d3696f20c4462c013286a5cba44d380b3446f54`  
		Last Modified: Wed, 17 Dec 2025 21:13:25 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4d58483e4e6ea69d40e1ea65b32a7d950491667aba2a6fd19d4d75652aed07`  
		Last Modified: Wed, 17 Dec 2025 21:13:27 GMT  
		Size: 4.1 MB (4140904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f486875a8cbab8d872dffad971bd15364a3f09a8d86cbfcd6698e2c31da8a654`  
		Last Modified: Wed, 17 Dec 2025 21:13:44 GMT  
		Size: 102.6 MB (102566216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d06b2bc8c159754081a05ddf591d8ee02ee81d93ab816fc9d90d847be3fdea1`  
		Last Modified: Wed, 17 Dec 2025 21:13:28 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:9c2c9b9d9f1d54372d34d583a23538841e3c0385937e53e26e1b9be24bc89a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7125c6ed0057d501351585c589dd25adebe7e77b7420105309e471908c1c9ce`

```dockerfile
```

-	Layers:
	-	`sha256:1f584a6024a1b4d52758cacd167082890322bce5a6f27007dc0930bd48201f35`  
		Last Modified: Wed, 17 Dec 2025 23:51:41 GMT  
		Size: 36.8 KB (36750 bytes)  
		MIME: application/vnd.in-toto+json
