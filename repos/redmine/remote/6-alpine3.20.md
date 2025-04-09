## `redmine:6-alpine3.20`

```console
$ docker pull redmine@sha256:e91dc840b3a6aa0e240e614b0ceb1e0eec846f256c8274e30ff2e9ad945e2413
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

### `redmine:6-alpine3.20` - linux; amd64

```console
$ docker pull redmine@sha256:b355bec71cda5b01bbe85f053f0b7ca7bfc07e19070377563b9d325950e71c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187664474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435571081632690a00dc0593f9a4f78765be6b4bc89d9c1a7febca0af1192907`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93df4c87d55138abcd35ecb102e717fd1d71ebaa856a800f87a6d87bc88fc14e`  
		Last Modified: Wed, 09 Apr 2025 18:34:03 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c60d8067458c82e1aafbafbbdea65f6bf0ec3b9667e3fe2cfa827190267ff3`  
		Last Modified: Wed, 09 Apr 2025 18:34:05 GMT  
		Size: 35.3 MB (35320052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d55e8a1b766e3a115001b32877b36158231343274851c2fb485b876cd63b7e`  
		Last Modified: Wed, 09 Apr 2025 18:34:03 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3f59079ed10020565717e1b7ff648cb81886f126e1484147804d2eac66c845`  
		Last Modified: Wed, 09 Apr 2025 19:07:03 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde93d808985774e070f4f42e661f75246ecea49d50298a72af6d7a7cbf00ba3`  
		Last Modified: Wed, 09 Apr 2025 19:07:05 GMT  
		Size: 70.4 MB (70385800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b085cbfff678315a86875aae4f901167ee9c2b838623acd9ab90110e0e80dd0`  
		Last Modified: Wed, 09 Apr 2025 19:07:03 GMT  
		Size: 1.2 MB (1166496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5a59d1a1b11db29eb57d1aab84ec62d79d180cb3ad16d3731ccaee2eab4078`  
		Last Modified: Wed, 09 Apr 2025 19:07:03 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e3ae62ca8a886026e116eb59da602499106802a968677165fb6a1634407f83`  
		Last Modified: Wed, 09 Apr 2025 19:07:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dc91504ed248f6deeba8220a4d2279903813d95870f0e949b8b4f5141606ff`  
		Last Modified: Wed, 09 Apr 2025 19:07:04 GMT  
		Size: 4.1 MB (4057599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3659d6f855c446a7a41cb3d1abfcaeedd3383896a25e5f5f2acd3621d1afaba5`  
		Last Modified: Wed, 09 Apr 2025 19:07:06 GMT  
		Size: 73.1 MB (73103812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6210b5394108519efd29e4e2b56087b9ef5679461b51c9618987be4a888164`  
		Last Modified: Wed, 09 Apr 2025 19:07:05 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:e8db35822db37ada607b30eee22d0f71cbb3e6a1c9ae07a0bd02f55a0b2e7170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac4b43153e7f162f367e454a7db67a6a3134d37b016cb6924d49352e21a3ed9`

```dockerfile
```

-	Layers:
	-	`sha256:0c7d738cc90867ceb4635957a8fb257a0d9c672d323bab7210e73daef966dadd`  
		Last Modified: Wed, 09 Apr 2025 19:07:03 GMT  
		Size: 36.8 KB (36792 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:0c946c9bdcfd2eab438958a69381c32ad9d5ac8d48446c15597905cc945a7a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179898626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a2465381bdab13e365915634376478568c7fc3703469d6a2cdb0d3b586db23`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c33e30311f7bfd2e574783afd81b2b022925223ace47a3475b924f32b157bc`  
		Last Modified: Sat, 15 Feb 2025 10:14:54 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe3c273884bd065c78b707e19d33e27dabd6a459e73b3496a64111c41f95a2d`  
		Last Modified: Wed, 09 Apr 2025 18:47:40 GMT  
		Size: 31.8 MB (31821286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dff2b8dd7869f7dfd28bd9c1f4d7068b46887ad455e8c29b0579a6cbf3ae56`  
		Last Modified: Wed, 09 Apr 2025 18:47:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d6cea316ccb2ff05402817288517225b6f3cb672c58a0b137500f3ce9899e2`  
		Last Modified: Wed, 09 Apr 2025 19:13:12 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407e6ea8f36604e77a17c399aceb1fbd94604b53dc635aeacc8b7d8c80e6e55d`  
		Last Modified: Wed, 09 Apr 2025 19:13:15 GMT  
		Size: 67.1 MB (67126787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a62173f1a65dac89f26b509be30278b7a2cc4f5807da8b2e83c5648ed4950`  
		Last Modified: Wed, 09 Apr 2025 19:13:13 GMT  
		Size: 1.1 MB (1133529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc44a371b7dbe0d5fe6a35123df2f9225941e378706a5571ac8f47b3abfe4af3`  
		Last Modified: Wed, 09 Apr 2025 19:13:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f10be57363d343ac58d7c9ea190c38329574f9928a2e0a076018037b6e8eafc`  
		Last Modified: Wed, 09 Apr 2025 19:13:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bb83e852351642cc000816919179d69bcc4a94c7d6b9aa696cb866c325cc6c`  
		Last Modified: Wed, 09 Apr 2025 19:13:14 GMT  
		Size: 4.1 MB (4057602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713f39fcda3f968e98de2229cba4cfb2018840cfcd0ce90dc4b6470ec7cee572`  
		Last Modified: Wed, 09 Apr 2025 19:13:16 GMT  
		Size: 72.4 MB (72383074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407305337104adfa7d8933d3d23ff38454a4d17cb32da7e58ca25bcc46c578a7`  
		Last Modified: Wed, 09 Apr 2025 19:13:14 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:e49b552cf0294c3b7e1f707512c728774c487303ae74e8cbcce6fe9389cf3a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c74656426629d192967b0ffa8187ba6e8e78908385b0afd81a7de8cd130cbde`

```dockerfile
```

-	Layers:
	-	`sha256:7f4387c3027fed7bf561fbdfbe9eb862d69f1c5f5c1aac71763663219325457a`  
		Last Modified: Wed, 09 Apr 2025 19:13:12 GMT  
		Size: 36.9 KB (36933 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:7f50f3c2c569d0f65739ae1d15200ff842f93683dbce8340bccb4b23f2bbd88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176089879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bede290a8215ba49d080b0f0e0f65f55b3444609d93ae643f25a96e9385a3339`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799e57590c350f854e3f043f25424960a35650d3b131e18c9cb90402ce911024`  
		Last Modified: Sat, 15 Feb 2025 13:28:36 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c3db92d3cb7bd38e0475467920f10bbf740d5b9cfb7c7b7f473965a1c80ed`  
		Last Modified: Sat, 15 Feb 2025 13:44:04 GMT  
		Size: 31.6 MB (31599489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711d62a2368b81c36686d988db2275e9a2767fc31111e524363fca340850fb0`  
		Last Modified: Sat, 15 Feb 2025 13:44:03 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9782f8e36c999c08c5eda8b882a5c11488e1ceab4589a7fc41c4a6d73e1f50b`  
		Last Modified: Tue, 11 Mar 2025 16:55:31 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d88a94f857dbc85e5026febaa1456798fe90afd467f70388c8ad86979306d68`  
		Last Modified: Tue, 11 Mar 2025 16:55:33 GMT  
		Size: 64.5 MB (64471989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4e9cd27053291fa543606c23d15d7a7261e3624527eb4ad978cfc63526ce7a`  
		Last Modified: Tue, 11 Mar 2025 16:55:31 GMT  
		Size: 1.1 MB (1133517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552ff309f14cf8c0870fed9b1c36d77d4d921c9f50ea8bf49afc3fae10e0665b`  
		Last Modified: Tue, 11 Mar 2025 16:55:31 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14a9ba9b0ac52c8322eece9d4a54cc09291d02afb8f9cc06feeca0374e343be`  
		Last Modified: Tue, 11 Mar 2025 16:55:32 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b72100075dd742e93a869c7abd3fafce7779e72f6c3a2ab6376df8c4c721f0d`  
		Last Modified: Tue, 11 Mar 2025 16:55:32 GMT  
		Size: 4.1 MB (4057576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd4ca6ac183d19d0f0b7671f0d0162b5dc7e07f42e8a8786f858db97f44bae7`  
		Last Modified: Tue, 11 Mar 2025 16:55:35 GMT  
		Size: 71.7 MB (71727524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128dca4ea238db8211f21384170135e879091b13b67c86e0591a6b2710134475`  
		Last Modified: Tue, 11 Mar 2025 16:55:33 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:772a7da60babf2b584e22ea72568ed9c91f8dda712814e8d699e45e2312c7a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6eea0f125b773f3ba4931a14b2dfa6ee18d097055e18d40cafaaa8d65b6104c`

```dockerfile
```

-	Layers:
	-	`sha256:6e8786da75f6d4eecbed4977ffcf9b12c28984b310ec3fca213d5ae81014bbb9`  
		Last Modified: Tue, 11 Mar 2025 16:55:30 GMT  
		Size: 36.9 KB (36933 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:90276a2b71a3058b1da7ee540de74dbb82c7be6bc200e6c52c4dfaea8dc645c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188904714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d0c5dbab939a74482d54732ec3b83c1acb1d91bb8ecd6cab379aaf44115d9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66821f213e2071472f4c29c4b6c7310a5d934f9d4ecf3ddaa6487a2ed00afc3`  
		Last Modified: Sat, 15 Feb 2025 09:11:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f0ac8517929d07bf85291c2a6aa8d8964afb6955b48ba76bdcd381e2b9f83e`  
		Last Modified: Sat, 15 Feb 2025 09:26:33 GMT  
		Size: 35.3 MB (35269320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0716f77f137277988b479bf9011de2a7458892db6217a33d730ac64ade59ce61`  
		Last Modified: Sat, 15 Feb 2025 09:26:31 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827e56b3d3a5d3ceb4bb8c3427b5a51c3e1cba3ed0ee8bd003b3f8701092a290`  
		Last Modified: Tue, 11 Mar 2025 16:53:37 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc0a75f993af19920ed3f24474962b5970afb3875ffa8af1f68713625ca353`  
		Last Modified: Tue, 11 Mar 2025 16:53:39 GMT  
		Size: 70.9 MB (70881989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5cd219e290e5df120595e2651d6b18ea0c0173f7bac31a05e57d0da05a97a3`  
		Last Modified: Tue, 11 Mar 2025 16:53:37 GMT  
		Size: 1.1 MB (1093163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fce1b166220b01cab69a063476310f9367c77389a25dcb969c327c1bd7b57`  
		Last Modified: Tue, 11 Mar 2025 16:53:37 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e143dd2a846564ab38b6b361a7895d7f77bd00e66b7be28faf1da1f1ffac694a`  
		Last Modified: Tue, 11 Mar 2025 16:53:38 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97760d8440d7a241a64b75e41e711204405831f168f4d818dd05c5f442b17375`  
		Last Modified: Tue, 11 Mar 2025 16:53:38 GMT  
		Size: 4.1 MB (4057587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8474d70cf1c0522ac1e22d3776382482e77237b170227b8f40fae110691496f3`  
		Last Modified: Tue, 11 Mar 2025 16:53:41 GMT  
		Size: 73.5 MB (73507674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7aee2c7411846def92ca853161079f8410d2695dae4f6238015a1e14b5e3ada`  
		Last Modified: Tue, 11 Mar 2025 16:53:38 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:d99918bcb03492543919265a820f43d8b4399b856c61a10a62e0b884a7bbf7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34919b3306188d5fd20d5229e7fd830dc8a19d72f1c65139239c3c9190803354`

```dockerfile
```

-	Layers:
	-	`sha256:af1613aaee3d818f9ce7f67080e9939ac66a141fa56a71101fe95660f75af274`  
		Last Modified: Tue, 11 Mar 2025 16:53:37 GMT  
		Size: 37.0 KB (36971 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:b644e03cc2565b16403c3adf152834845927951f553ccb855cdcfa6b124a60c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184693756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14b40868110f31e7c2eefd38ce8a83ed7b9c11fc8669bc0a772c9ce16edce18`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e19e99331736f1aecd67f9853ea1ba5bb1a7e2552549048a7bf0270c1fb3f24`  
		Last Modified: Wed, 09 Apr 2025 18:33:30 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98476c4f037559912bb79c9473bf46f095fd1e7a9a9369238bc767f852f90b86`  
		Last Modified: Wed, 09 Apr 2025 18:33:31 GMT  
		Size: 31.7 MB (31687387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1195e1d13875318044d1f1e168b270ec56f3f093ba34b0e2acffa5e8cc94b7`  
		Last Modified: Wed, 09 Apr 2025 18:33:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535d9d3231bcdb23534b009815b153ad9416ac5753c01ff2079e7c5bbfa4e3c4`  
		Last Modified: Wed, 09 Apr 2025 19:07:10 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851e0cde26ae5a5dbeff41f52756fdd5e42876f1fbc933db4f16e6cd2b2f836f`  
		Last Modified: Wed, 09 Apr 2025 19:07:12 GMT  
		Size: 71.1 MB (71130039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557c16d54cfb67e517ce088105c4620653744fbb15a4d4e47d220a9a97e1fd3c`  
		Last Modified: Wed, 09 Apr 2025 19:07:10 GMT  
		Size: 1.1 MB (1141441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3c345a1db0cd22bb6f784e1c1b8343c80acdde76ee4ab360f8c3714592c6b1`  
		Last Modified: Wed, 09 Apr 2025 19:07:10 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44479f40a5abbb43023df2b1756c3d97ebeaa67c65de189ff43912020474eae4`  
		Last Modified: Wed, 09 Apr 2025 19:07:10 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d3905251a31d7d2cfa80dde78e477b573f7337e6406ce9270127c2097e8b7a`  
		Last Modified: Wed, 09 Apr 2025 19:07:11 GMT  
		Size: 4.1 MB (4057650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62362069669c1d899636ac3d23d00f647a8f3109b5c45f8ff885bd517a04eade`  
		Last Modified: Wed, 09 Apr 2025 19:07:13 GMT  
		Size: 73.2 MB (73201753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6210b5394108519efd29e4e2b56087b9ef5679461b51c9618987be4a888164`  
		Last Modified: Wed, 09 Apr 2025 19:07:05 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:b9ff413cf466b2daff7a07d48d98d95a2f094b83d76682b3c15bf6ff2843bffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82eb379394c8b6f16b1ce3359be32ceecf58841541710678f227cd167c8dc831`

```dockerfile
```

-	Layers:
	-	`sha256:715f6e26306e324df86f007ed5bee3039a4eff7c2e3a29ee83a1a2a6ee03ecd1`  
		Last Modified: Wed, 09 Apr 2025 19:07:10 GMT  
		Size: 36.8 KB (36750 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:3b42b9e3ad902c9c4b9a6849f30cb92819f8c636fd09d5408378d69786cd2dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188935568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96527eeef1a6b24cb7e92968236a6476be4c518b21dc9cfebc5570ab882a5d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a693b867e7bda881243cadc00b9fd3fb1dfa2463906770a27d86b54b103c064`  
		Last Modified: Wed, 09 Apr 2025 20:08:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc2f8ce33bdbe12759bd62c21259aab02392ba2b7653784b1101859e583d83c`  
		Last Modified: Wed, 09 Apr 2025 20:08:26 GMT  
		Size: 33.2 MB (33177344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb221d184f9bf9ad0b85501ba63879e8654da90dc71ac7ce1cbdf989b4b37e`  
		Last Modified: Wed, 09 Apr 2025 20:08:25 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a741214896f5b62fbdc039d6f46874d1aeeb8dd2ccba43ab5f73bff230302ed1`  
		Last Modified: Wed, 09 Apr 2025 21:15:09 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75996aa612ecec7cc650bc5f4f0d10da83719609e0abe1a24a9243621637e915`  
		Last Modified: Wed, 09 Apr 2025 21:15:12 GMT  
		Size: 72.1 MB (72118435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca71864cc12fd363ed1c3f8d0068c63b8279cf3a4eab7827dbc95c8052fe59b`  
		Last Modified: Wed, 09 Apr 2025 21:15:09 GMT  
		Size: 1.1 MB (1083770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e75b60ce7ca231ef85bf906d8137abd4a651f6404dc993ca2bd6409dd1a3e6b`  
		Last Modified: Wed, 09 Apr 2025 21:15:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1018200ef064964dfcabdb39fc43173881f52867802f630420f138c1cf2e4551`  
		Last Modified: Wed, 09 Apr 2025 21:15:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311f96cece5ca0413a0da43d124cc3b0a6f0da6a020431702446e0ccbb2c5f9e`  
		Last Modified: Wed, 09 Apr 2025 21:15:11 GMT  
		Size: 4.1 MB (4057675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1831dfb045761fb6882937086188644bcceea236c759d6fa5126c534f8a6b519`  
		Last Modified: Wed, 09 Apr 2025 21:15:13 GMT  
		Size: 74.9 MB (74918843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23fa6ae84a8e424281ed294789c00cd38a7b3b79d0726bdc60658c13313f0e2`  
		Last Modified: Wed, 09 Apr 2025 21:15:11 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:9b0b0365bef9f2b24d78ce3c5f520c724ea3ff1f49784a3dceddeb377eaae2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654c0a074279ea00f0e69500ae985ab9fee497a52df58298ccdde5888d622bb8`

```dockerfile
```

-	Layers:
	-	`sha256:fb2051032bdfdeaeb68015e29138fc8fdce5269ed90cab1bcc9ea4a93963d6b7`  
		Last Modified: Wed, 09 Apr 2025 21:15:09 GMT  
		Size: 36.8 KB (36845 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:3223f85be0f749119099580c8917bf3fed3436a95000162e00231b0c9eef7dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b927ea2ae0b8d36200eb76466864f407e41d390c5d6797809f4e20579266ed79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cd13f0347dd4833f5941662d6b8aac773d7dd4aa9f99b546f2070234b3130e`  
		Last Modified: Mon, 17 Feb 2025 04:46:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec867a08f4e71902fc1e2ba70569514c00bce5ae4c253b861e54bf23a692b1f4`  
		Last Modified: Mon, 17 Feb 2025 07:47:06 GMT  
		Size: 31.6 MB (31557006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4f725f8ff080246a72d77dff5985faad3aaf6dd00eda0c19e6b46a8c36c49`  
		Last Modified: Mon, 17 Feb 2025 07:47:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a797d21eb630cff9240964065d494d62f57bf7d4d118886f136b0ff9cd48872`  
		Last Modified: Tue, 11 Mar 2025 18:48:14 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f92a6d5a4e7ca119d530cab266bc944ab4bd07bd0bc446d377e4a832c6fc05d`  
		Last Modified: Tue, 11 Mar 2025 18:48:25 GMT  
		Size: 70.8 MB (70774874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef64b66f60d683b16eb516035a38713500e2fa51bea99e9df3ef317749012a1`  
		Last Modified: Tue, 11 Mar 2025 18:48:15 GMT  
		Size: 1.1 MB (1134864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d843b4ec5594e7f199f7a1537b467c541491af9613bfde9cb3fb9ff491d651f9`  
		Last Modified: Tue, 11 Mar 2025 18:48:14 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2738bd70ff9cc0cad7ce3475a71d90048c7856866edb02df8c73ae7a2499bf90`  
		Last Modified: Tue, 11 Mar 2025 18:48:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8d81b1b9a9ebf5496e9e202961c36ff8ef094174cd3bfa2f092269ffd43dc2`  
		Last Modified: Tue, 11 Mar 2025 18:48:16 GMT  
		Size: 4.1 MB (4057636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c272828911bcd9e4df7ac66c5ff7c6b77823b164dd83933adea29bf1d27d4`  
		Last Modified: Tue, 11 Mar 2025 18:48:27 GMT  
		Size: 76.8 MB (76794862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee555556d7a45895f93d1d1e4b3abf5b5078e712c59226eda11fe49834540759`  
		Last Modified: Tue, 11 Mar 2025 18:48:17 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:15fefec18e8cbab558d2eacb0332ec4c30ee2b115592afe0b524b051ba09e2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ca0584c4fc1f0906cde15e97b50068d0cb54d1e9d1dcb5eca1a51740bcd738`

```dockerfile
```

-	Layers:
	-	`sha256:928f11f35c74978dfe869af8c1bdfe35e66fd78d2784bbb5c45e080190e7a303`  
		Last Modified: Tue, 11 Mar 2025 18:48:14 GMT  
		Size: 36.8 KB (36846 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:b8b347ef70e5de397ad50f6eda90465fa2b899a98c256f6ce4369e0d61dbcdd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188274175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb429763c888806fdc4b3ce2e65011c8cc6c3c3e59ad487b32ffb4fbb8785bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cdde91b1efa7806e68cc1ea41fabb266e9146a0d033cbfa2b0cb94cbabd8bd`  
		Last Modified: Wed, 09 Apr 2025 19:57:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a4faaf0bb8963b4ebfd125ac2723641d5b8c6577b1e4bfe5cf9252a8746730`  
		Last Modified: Wed, 09 Apr 2025 19:57:27 GMT  
		Size: 33.0 MB (33027239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f085ae41ea0bed0cb7af56b4851f62a5f0ab86edceac81279348813217817434`  
		Last Modified: Wed, 09 Apr 2025 19:57:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ae3b3a9cbcafba4f257f4fb175c2fd7e095cee6e0b84154cca9080c8034b2`  
		Last Modified: Wed, 09 Apr 2025 20:28:34 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d464d2464533cda83b983f1a4fe876b43a49b0781ade689faa163691f69afbb6`  
		Last Modified: Wed, 09 Apr 2025 20:28:36 GMT  
		Size: 72.3 MB (72278761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5d27c3611011de6b94e25e5c677866693a38cd7b00c04b0e1db19a575956ec`  
		Last Modified: Wed, 09 Apr 2025 20:28:35 GMT  
		Size: 1.1 MB (1131140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b09b8907c81dc8b1564eec3a5a38636876d65cbc1c8c57643dc446a6c25eaeb`  
		Last Modified: Wed, 09 Apr 2025 20:28:34 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab97eeb60affde902ffaf0377ce65e0814e167d93019cc85073c020a3baa6c9`  
		Last Modified: Wed, 09 Apr 2025 20:28:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc120761c218de276c789e67739d7b518d227d0727a4acf94f7e4021d81cfde`  
		Last Modified: Wed, 09 Apr 2025 20:28:35 GMT  
		Size: 4.1 MB (4057632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ea2a241900ec0f5161291fe42a1bd029c0bdb6cdc5e6b94c3481bade3fa76`  
		Last Modified: Wed, 09 Apr 2025 20:28:37 GMT  
		Size: 74.3 MB (74311461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541fa4702ed4765dbe69b21bdfabf04041c88e142bc7223e477b1ca14b057c64`  
		Last Modified: Wed, 09 Apr 2025 20:28:36 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:b873899651ca3a4ff6ad4457a91a3a0923620d2f6eaf79b78a39dba66609295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4261cfebc05d8caaa75ecfaad6cea82ce718696437af6a41f37acd2d3d65d1`

```dockerfile
```

-	Layers:
	-	`sha256:298767045d6f9d312635e40cb9a964583947c50bc9d053ea3689710fd5928d6a`  
		Last Modified: Wed, 09 Apr 2025 20:28:34 GMT  
		Size: 36.8 KB (36792 bytes)  
		MIME: application/vnd.in-toto+json
