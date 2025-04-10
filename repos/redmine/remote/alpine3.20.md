## `redmine:alpine3.20`

```console
$ docker pull redmine@sha256:ad570961b3da49d5106ffc3dac3aeef1b278d9d1855c7302afde801f55693606
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

### `redmine:alpine3.20` - unknown; unknown

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

### `redmine:alpine3.20` - linux; arm variant v6

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

### `redmine:alpine3.20` - unknown; unknown

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

### `redmine:alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:2f288fd7896ef83f7d97ed238cf284d2336514c9c97e87cadfd9249838edfb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175778139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de833d73c70d570af6435198cb5c880619ea20812dbe7a023578d2299cf28138`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
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
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2a1abd79c8408aeb5068f398ee58dd6d205ac18aea943b7042904720577fee`  
		Last Modified: Wed, 26 Mar 2025 16:43:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30b8de27eb7e66960d6af925117888ac1bfeed5da4ff72827020ccad6e2d3ef`  
		Last Modified: Wed, 09 Apr 2025 21:31:00 GMT  
		Size: 31.6 MB (31640255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580b1cdfb5ed8e5942c47f8db5ebb2401a3c6214b06c07a243cf869f1501c44f`  
		Last Modified: Wed, 09 Apr 2025 21:30:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91f25e1e23f19e5ca67da3b57cdf17c9fe8977279b13a1722da1f27950accbb`  
		Last Modified: Wed, 09 Apr 2025 22:19:04 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b936dd6eb4e3f69be2f15b1060f91d62c4f6dab1b577710fd7d51bc91808c9d6`  
		Last Modified: Wed, 09 Apr 2025 22:19:06 GMT  
		Size: 64.5 MB (64465818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2b6070347197a5b2039c1acc376ceccd6708619093c71d77fe1a9d97a5f7f9`  
		Last Modified: Wed, 09 Apr 2025 22:19:04 GMT  
		Size: 1.1 MB (1133497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c714b30e2b5129f0b5fa8ecd139d36ad67796b36107fad59c873516d6e683804`  
		Last Modified: Wed, 09 Apr 2025 22:19:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151c1e3d2b5abdb18d1ddefd2e43a040a3d97a9f33b6184855118ca7d3bf1920`  
		Last Modified: Wed, 09 Apr 2025 22:19:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8a04c7962d766a86068ecbcb7dc23929b3fe169f3980c819f80949d22da018`  
		Last Modified: Wed, 09 Apr 2025 22:19:06 GMT  
		Size: 4.1 MB (4057645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9097a2ad24bb458f84d1eac45c3cd5283d8460c489a5479c31e4b2acc556888b`  
		Last Modified: Wed, 09 Apr 2025 22:19:08 GMT  
		Size: 71.4 MB (71381138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f75281e7e9c7791db2b612d25388e30b641c2d938df69acf56c1ba04872ad2`  
		Last Modified: Wed, 09 Apr 2025 22:19:06 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:ca97e7291e452dc779918852aba28454c918d6add21b7d6814405cf44ce57083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d522af659629e66f5ada293846a13300a742cecf42afb457909496c4f88b8f25`

```dockerfile
```

-	Layers:
	-	`sha256:54388a7ada4804342045d6ce44ce45976f44df3c3557313b85c6a26e2efef33e`  
		Last Modified: Wed, 09 Apr 2025 22:19:04 GMT  
		Size: 36.9 KB (36933 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:2ee61d3e9fed217e8037fb9a94831f79db1643c49abcb95757120f49eaadb769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188584991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c395440dbc6771665a53f9f836784fd7e339184a64bf1e3349e6b7f9dfd662e8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4db2f7a438d93cb33371d46a00392a977600785050079237e8d46f0b1e16a7`  
		Last Modified: Wed, 09 Apr 2025 23:41:53 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128cc7d4517edddfe3663e8e4f96fa344a29204094f5c6e562e808022c7d8dba`  
		Last Modified: Wed, 09 Apr 2025 23:41:54 GMT  
		Size: 35.3 MB (35278975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1084c2f6e3e83e93ef59f478a202f9b0339cf2645ae1172eb7baf6ad0128a246`  
		Last Modified: Wed, 09 Apr 2025 23:41:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452c859f301062bba5d5fe2eed297668859d4c73034a5c33ab4eba051c7b849c`  
		Last Modified: Thu, 10 Apr 2025 01:59:08 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edee375a3ff64e4a76ffdb0aec96c866dd72cc5f58bc749cca2afc9ea351f25`  
		Last Modified: Thu, 10 Apr 2025 01:59:11 GMT  
		Size: 70.9 MB (70879618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c0fb45aac216e71c80f80e06cb79a52a98f0095e8cd6ceef241b19c2307ae9`  
		Last Modified: Thu, 10 Apr 2025 01:59:09 GMT  
		Size: 1.1 MB (1093133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba9cb81db75ec4f256ab4eeb52cdb258a1428891d08b1460d49764af9eedd73`  
		Last Modified: Thu, 10 Apr 2025 01:59:09 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6015ca99686c21c1c2f2a0aeed0f122ce373512b34c8fe5844d000b207bbaebc`  
		Last Modified: Thu, 10 Apr 2025 01:59:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466915e4893947bd1d154894410bde0b8e797f0c9ef18533a32af82181b6e5a7`  
		Last Modified: Thu, 10 Apr 2025 01:59:10 GMT  
		Size: 4.1 MB (4057624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d0bce2445883a3fefa67f9b9d313a2b57aeb5a3be85b8c5ccb9b9089b609b4`  
		Last Modified: Thu, 10 Apr 2025 01:59:12 GMT  
		Size: 73.2 MB (73180656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5e16fedc77bcffbd0f78696581c59f1362798cae47625b429f9d1d20186032`  
		Last Modified: Thu, 10 Apr 2025 01:59:10 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:ed9f0b752e70c7453689c2e048c63ce6b7a7800e65698224b7b8e363d426ae7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b47bea3e287be727c1c1b1646d96ab415f606892ffd750f772d6f80490db43c`

```dockerfile
```

-	Layers:
	-	`sha256:416dbb6b08629f2fe0d42bac094ef6c915bbcabf96cc016bedf265b15f1dc2c8`  
		Last Modified: Thu, 10 Apr 2025 01:59:08 GMT  
		Size: 37.0 KB (36971 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; 386

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

### `redmine:alpine3.20` - unknown; unknown

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

### `redmine:alpine3.20` - linux; ppc64le

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

### `redmine:alpine3.20` - unknown; unknown

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

### `redmine:alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:d8191e3fe2423b836d66f19d4c6c44f068a2e41eefc2e1ac0d05761e570b5b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187398923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0923692fb96bc03627e9372701a0fd567503d5286afc9983feffd7b4ab0ad78f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
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
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cd13f0347dd4833f5941662d6b8aac773d7dd4aa9f99b546f2070234b3130e`  
		Last Modified: Mon, 17 Feb 2025 04:46:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeef1254d589a0d8debaaa3530bb011fe4d7b1efa47991d89b2080c8dfcd72f`  
		Last Modified: Thu, 10 Apr 2025 02:57:29 GMT  
		Size: 31.6 MB (31594412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8859b17feaa5629b28efc98ba29b173c66d96ee9fbd8fe851bbb941890336d`  
		Last Modified: Thu, 10 Apr 2025 02:57:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1478ac45645eaa6cb7ddc82af128a996f2a7de2619515b866afd0cb228544e`  
		Last Modified: Thu, 10 Apr 2025 05:53:40 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79493c071a32fc8f555bfe8fcf31c44cdf1492d2dda74808727f9b6809ebfaf6`  
		Last Modified: Thu, 10 Apr 2025 05:53:50 GMT  
		Size: 70.8 MB (70774489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c435c2210b9f8b0adf563bf89e414241088c2f21e39768f4a9fd9e5789d5ec6`  
		Last Modified: Thu, 10 Apr 2025 05:53:40 GMT  
		Size: 1.1 MB (1134854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bd785c14a2bb07b841d1aa32e5baa843bbbd149667c60df19d7885de3676c5`  
		Last Modified: Thu, 10 Apr 2025 05:53:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11d4050779e69eb135a489912ef6061bee145477be289241788e8ed3652c1f2`  
		Last Modified: Thu, 10 Apr 2025 05:53:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d46554b6c677e00001f9fd6b391798bab8ff18338988e59bb428c342e787be7`  
		Last Modified: Thu, 10 Apr 2025 05:53:42 GMT  
		Size: 4.1 MB (4057662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d612dc3e43d3bcbca4b67d5a3b1b1797cd41dec30e1965ac4efd0c5b7bb712`  
		Last Modified: Thu, 10 Apr 2025 05:53:52 GMT  
		Size: 76.5 MB (76460452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcb85bf4a57085f92bea8249b3c3471882b1af332f3e8231817d0279ab97c9c`  
		Last Modified: Thu, 10 Apr 2025 05:53:42 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:c7481656a0e9d16c312b377fb2699f16df662f81dc78c16efa38f93c04c250e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297134b4122b4f51aebef6f8eb21bda7089d6843646d3bd05bb0faa77c66f4f4`

```dockerfile
```

-	Layers:
	-	`sha256:cde45d140b321957c75187b0e7b28326b52ed27e7817fb227b78e91a2301f786`  
		Last Modified: Thu, 10 Apr 2025 05:53:40 GMT  
		Size: 36.8 KB (36845 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; s390x

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

### `redmine:alpine3.20` - unknown; unknown

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
