## `redmine:5-alpine3.21`

```console
$ docker pull redmine@sha256:1de1e3834c37b003285f1dc56a396059c8d162995cfb886db122b35f73e12354
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

### `redmine:5-alpine3.21` - linux; amd64

```console
$ docker pull redmine@sha256:fedd82fdedcc67af0221d0525d4f311258fe9783e0e0b2c4dde5dafd21d20518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184941013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab474937682f71a1092d19903bc12d8d0684988993aa7b7d977243571d57d1c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:00:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:00:32 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_VERSION=5.1.9
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.9.tar.gz
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=cc0ddafa6fe6f5192236a27cec64e3466023a12c92c1da4abb680248639f678c
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:00:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:00:32 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:00:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82050ef87981644624a01fd9c2d0ea0ebe5f06ba19438fe3a4207de7ccea595d`  
		Last Modified: Thu, 08 May 2025 17:21:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b9c29801ccf9034db369521d155d2d39179759f5c08246fd21ccde55982d66`  
		Last Modified: Thu, 08 May 2025 17:21:49 GMT  
		Size: 33.8 MB (33805385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d7a9463bac14c0b2a151493cbdf6011a6b7edcd5b9a4560e4ce3bd6742b0b0`  
		Last Modified: Thu, 08 May 2025 17:21:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188093f33c717876833a11c4bae065c1f9d8e878eb2f23df5b0f5c752b1d8e72`  
		Last Modified: Mon, 07 Jul 2025 23:02:59 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e31c38a6907224c9af225608e15c19734e20203eba5ce1b4827493da4c672ee`  
		Last Modified: Mon, 07 Jul 2025 23:03:07 GMT  
		Size: 72.4 MB (72382882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0fde3f4a9411343cb2ac28b545c7e4e89744f8f09ea7c8540175efd4e145f9`  
		Last Modified: Mon, 07 Jul 2025 23:03:00 GMT  
		Size: 1.2 MB (1168641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf5bd7a8fd2beb288cc204911ad2c2cd4b741c4a0a9a1a839439bd2d517c166`  
		Last Modified: Mon, 07 Jul 2025 23:02:59 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e51a0075c49c9727520e5dcc30bf2237ac42a98b5a8ade40e54c03abef278a`  
		Last Modified: Mon, 07 Jul 2025 23:02:59 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7e97eb93244efbcd7e1472ddaec1b36e35ff8f2b9fcc038590e33615ed5dd3`  
		Last Modified: Mon, 07 Jul 2025 23:03:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3e0af2669ddbaed43b7715438b8e86bfecd0a15945b3b0e1c48a772de43706`  
		Last Modified: Mon, 07 Jul 2025 23:03:00 GMT  
		Size: 3.2 MB (3249827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2df65e73f2834624ec8ab9e08b3fcd5b76677f2ff79af78c0676fe66a38f23c`  
		Last Modified: Mon, 07 Jul 2025 23:03:07 GMT  
		Size: 70.7 MB (70688047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a075ccca9d6490c76919c04a40f5dc1896b90a8a4dfaa13996d7990dcb727b9d`  
		Last Modified: Mon, 07 Jul 2025 23:02:59 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:751e271d7698466cda935df45df8a52a719e9716b94940d7c48bc80b7c6c8906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edc3d913654ac2fa3e244df023d7a9b4cf714613483b22920657902b67a6c11`

```dockerfile
```

-	Layers:
	-	`sha256:9210f5cfc497e2ae7648adf1cf710ebc5375f8e966cf23723a098750cb58906c`  
		Last Modified: Tue, 08 Jul 2025 01:50:01 GMT  
		Size: 39.6 KB (39635 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; arm variant v6

```console
$ docker pull redmine@sha256:5d1fdf8c5835605b87d288297977268144801a5345ff8479200c307ab4b739fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177041061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79cef37dd0186c360937c90244211420cf1aad0614e283e36256b51b74ce860`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4026b00b6e21fbadf6a8a598214400acf92d3e7692e141b46a55ee0beb504ed5`  
		Last Modified: Sat, 15 Feb 2025 12:57:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f48be190b8f83385aab4d50d4d33605c506bacff5981452fe5c23bc2aa3dcf`  
		Last Modified: Fri, 09 May 2025 05:44:22 GMT  
		Size: 30.1 MB (30052775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1384bb22b44decbe06f15c09e9af483e19ec1c083df8d8a01f4b89e00e61f3`  
		Last Modified: Fri, 09 May 2025 05:44:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ee7242f1b9ffc89a95dd45d99cd7218c3e009876166065e910a6563e017f8`  
		Last Modified: Tue, 08 Jul 2025 02:18:07 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d797ccd2e94b9492b79cf16f8abce4138797d237bb470fcfd5ec513d3784a299`  
		Last Modified: Wed, 26 Mar 2025 17:10:51 GMT  
		Size: 68.7 MB (68670315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88de0af39a1e142256bb110abfa3c7e006ca842120d4b70120d32d8b7eb1ca19`  
		Last Modified: Tue, 08 Jul 2025 02:18:10 GMT  
		Size: 1.1 MB (1134866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b266185973ed69909cfcedf1bbf7a0579b4dd56f28095b349c40a7eb9e83c7`  
		Last Modified: Tue, 08 Jul 2025 02:18:15 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2da9541cad7d178d4a1aec0ddcf36a7cb798781b7f4b0e102caea890f81c971`  
		Last Modified: Wed, 26 Mar 2025 17:10:49 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc2f676a098b2ae5257c37b5ae28d6772ab981ae619fc955a1c610997f1d6fe`  
		Last Modified: Wed, 26 Mar 2025 17:10:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6b89c78163bf7574c16b419f1c79851a440374cd42585695a2531801ee0d33`  
		Last Modified: Mon, 21 Apr 2025 23:01:52 GMT  
		Size: 3.2 MB (3248022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ef170c746f98b526965b272ed3f2ace3be1c02cdb02430b1843204b2b648fa`  
		Last Modified: Mon, 21 Apr 2025 23:01:54 GMT  
		Size: 70.6 MB (70566374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfb8ccfe229bfb8315c894c8e1ecc8d209ace79ce8b513dd47c73ece43d0b86`  
		Last Modified: Mon, 21 Apr 2025 23:01:51 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:572a3e0f26416dee52697489349001dff29c9384e77ee900505865e34b2ffba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace26a75339c1269ded6987a2c297bea12f0ed7ec98442baac1f6653a3bbec4d`

```dockerfile
```

-	Layers:
	-	`sha256:2306ce06d1d1c235722b8eb18f9f78e346bb3affa6f4ac11361b8b533362faf7`  
		Last Modified: Tue, 08 Jul 2025 01:50:05 GMT  
		Size: 40.7 KB (40729 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0697470f02c8d3100eee4d2f0507b9ae0a2b557acd2295563941524957b932f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172125558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2017a7efdc384613817535a7cb10d24e360a578d75fd9c23f34eb04ce2da4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c428f51edf4e52635d4d3ad03cbb076c9509daee6cc3212c8ed31afd484d9e76`  
		Last Modified: Thu, 08 May 2025 21:23:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952ccac258493a39d87af59c84310469180e3a6b6b933e3da389f96964ffbc19`  
		Last Modified: Fri, 09 May 2025 05:44:20 GMT  
		Size: 29.9 MB (29913398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018d63b2d2246f38de37d58de2e323c518c9738cc9ac5c68bc7747322bfbafd1`  
		Last Modified: Fri, 09 May 2025 05:44:18 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04a0287fdabf9be810bcb98354e9e7fd3310c63b3c1bb1a2e85f948dd92d15e`  
		Last Modified: Tue, 22 Apr 2025 00:12:17 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efb142a43aff7af0b62e6d9890d0cfe383fbb534febd82becf52611d0401933`  
		Last Modified: Tue, 22 Apr 2025 00:12:19 GMT  
		Size: 65.9 MB (65903959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e891b205457c33e7e21da41aeb731ee0acd754d17f13a45adc8eadc549be8c34`  
		Last Modified: Tue, 22 Apr 2025 00:12:17 GMT  
		Size: 1.1 MB (1134872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd877456c6e4f05aa99b6a493a24869a6fbbc67f4cdc3d5ed94279463a9a330`  
		Last Modified: Tue, 22 Apr 2025 00:12:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f794bfa98074a3096ed595a0536523ff167f855e07debea37e8ff6f3bfd9d8b`  
		Last Modified: Tue, 22 Apr 2025 00:12:18 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff977fd95aea1883af137cf9207871705d291ea017e631653f129b0787fb4585`  
		Last Modified: Tue, 22 Apr 2025 00:12:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b643b8a21d5481aab72045110815372c8c682519516b4a20e40470807bdc059`  
		Last Modified: Tue, 22 Apr 2025 00:12:19 GMT  
		Size: 3.2 MB (3248026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6071ae491b9f7ecd2eac6b85cd7b5c58984f4522c1146f41e77c922a7c71067`  
		Last Modified: Tue, 22 Apr 2025 00:12:21 GMT  
		Size: 68.8 MB (68823204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e38632363ed918a583440560cbc0cbf6cb27c84d6e9846bf33ba24ca8b16aad`  
		Last Modified: Tue, 22 Apr 2025 00:12:19 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:0a3ee5b52ba12d14a81ab2a137c4a91f7346278330418246b09c18f20af9c626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c139df140c615055b2cb7c13996a848ddc3828de74ba6c1341cf0848dee47e`

```dockerfile
```

-	Layers:
	-	`sha256:7184b05a473fb496478a73d97615ce1fe73c8117c67ab1dc6b49602ead736fda`  
		Last Modified: Tue, 08 Jul 2025 01:50:09 GMT  
		Size: 40.7 KB (40729 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:1dca54bf803c4be4413a848f0d2c82dfba5ef3949cc2dd8c3b015ecb5d48e395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184378015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9e37232e3b571300c210349e3d65e4eb7bb44cd1515f51e191531c38e3e0d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9c621ad8c1aa244652bb567a1d455b956459afd342ac2e53400dacfdb4c3a5`  
		Last Modified: Thu, 08 May 2025 18:01:11 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e434d036f1f0896224b6443939378a4fe40897716d2b56cf6b8a6a27788ae965`  
		Last Modified: Thu, 08 May 2025 19:43:57 GMT  
		Size: 33.8 MB (33759782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00b65b7944e0a8b9c0683f72ffc415c6fbf80fceff241da1376f6a807728b50`  
		Last Modified: Thu, 08 May 2025 19:43:55 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d4d61385f85fe9f2f4306f42a147f11f259f45ee4f1296071a8755dd0ab234`  
		Last Modified: Mon, 19 May 2025 11:29:06 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d9de9bb650e8ae770cab68ce1b9f96723a3f5cdea350dc611efa5bc5de8e73`  
		Last Modified: Mon, 19 May 2025 11:29:14 GMT  
		Size: 71.7 MB (71728105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b12973000f648a86f969716e11fac4fc874cb95bd26182cf3e160ea7ab8d3e9`  
		Last Modified: Mon, 19 May 2025 11:29:06 GMT  
		Size: 1.1 MB (1096568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbee72477d0f555dc74b8283a8a4b731dae3259fd7376efff6eff97c17eb2ce`  
		Last Modified: Mon, 19 May 2025 11:29:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a861763a1155e573e3188976e75418743af9bf5f4bc5854cfbd791c28f035358`  
		Last Modified: Mon, 19 May 2025 11:29:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931662dacca46d0fcb668e67ad4d5222036436df655acf5c893cc7c8d27978df`  
		Last Modified: Mon, 19 May 2025 11:29:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733136f032f4adbdb1ef451dc4077310ec60a26f6363a29e0bfbd1aa810d5df2`  
		Last Modified: Mon, 19 May 2025 11:29:07 GMT  
		Size: 3.2 MB (3247999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de511b7d7f22f5b67c00cf206217d28424e2fe97ca100d1b4c7f9ce1f88a17b8`  
		Last Modified: Mon, 19 May 2025 11:29:14 GMT  
		Size: 70.5 MB (70548547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1b3364b59f72bca8ed1a4b68550e5c63750561a4b3331f11192fb332eaedb5`  
		Last Modified: Mon, 19 May 2025 11:29:06 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:d2ef49db0b2abc43b94978d6702fa06e160a75add411b85caf16131b1668057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee10260f2172a7c7632e676a7a4695f55ef03ee12ca63f9aa5f2b23923824b4`

```dockerfile
```

-	Layers:
	-	`sha256:c68120a883a3cd4ff316fa9edd56f6af8f646e156739931656707d309229695d`  
		Last Modified: Tue, 08 Jul 2025 01:50:12 GMT  
		Size: 40.8 KB (40777 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; 386

```console
$ docker pull redmine@sha256:47d2b5f67fd491b5cd7084a68943a3464328c6222cf15c8e9443f67921276a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181609105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648acef53844146f7267677d85fe01b65a21e31df6f4b2875e757f69d391410e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:00:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:00:32 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_VERSION=5.1.9
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.9.tar.gz
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=cc0ddafa6fe6f5192236a27cec64e3466023a12c92c1da4abb680248639f678c
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:00:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:00:32 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:00:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e05bf57fe60ac5590b522b1d66df3bbd94700e0ebffb57e97572a8e0c7584c`  
		Last Modified: Fri, 09 May 2025 05:44:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ce678cd54151b4f73d7ac5304d122bf31225c7b3905b1f0a63412bbb94b455`  
		Last Modified: Fri, 09 May 2025 05:44:20 GMT  
		Size: 29.9 MB (29916383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e7faaa44064e6751923cfa8c8519472b9c27630d57481d74d82dc9ecf9d2ec`  
		Last Modified: Fri, 09 May 2025 05:44:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d254f46519cffe55f010feb9c111d30b04161e27b8d491dcb178a6f9408a0fe`  
		Last Modified: Mon, 07 Jul 2025 23:03:11 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4902d5ab661493716bf44ed008b98d261bc5863b178f471218447e44a86999a5`  
		Last Modified: Mon, 07 Jul 2025 23:03:24 GMT  
		Size: 73.1 MB (73057019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27732fa3aa46341ea41c74f9a4e09c429ddfab2a9df0a849976be21868737036`  
		Last Modified: Mon, 07 Jul 2025 23:03:12 GMT  
		Size: 1.1 MB (1143858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4528488e0ecc551fac4831183100c4568fe25b34cd3d5dd8ca649c0abd59d2`  
		Last Modified: Mon, 07 Jul 2025 23:03:11 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07828d6d43f33354e94e1d0e0f4142c058becf72a6626ad56dece81c481500fe`  
		Last Modified: Mon, 07 Jul 2025 23:03:11 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7e97eb93244efbcd7e1472ddaec1b36e35ff8f2b9fcc038590e33615ed5dd3`  
		Last Modified: Mon, 07 Jul 2025 23:03:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9282aa13b26ccbdc9d055fda8689399c3b8e8e1236c6cf91235949344cdc05`  
		Last Modified: Mon, 07 Jul 2025 23:03:13 GMT  
		Size: 3.2 MB (3249828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a0a0e0ca8482feb2c1cb561dd7f3349f4b953cbb196515c38519addfe0a822`  
		Last Modified: Mon, 07 Jul 2025 23:03:26 GMT  
		Size: 70.8 MB (70774414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf357b32afa8dd9dce2f5715d7d163a4383911587632566e09736f1758123845`  
		Last Modified: Mon, 07 Jul 2025 23:01:26 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:7c2508b220a7ff5b3d0d67ccda79752e742afc8d1cb4066b92a07200317c51ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063e7ef27cb3c3dc90fcc784e82b6cb29b97b508cfe5cc9870065d4d5e6b838f`

```dockerfile
```

-	Layers:
	-	`sha256:b45615f6ebe902f04e7f3bff92cf724f8ebc7158dffa1527cf2632c696670142`  
		Last Modified: Tue, 08 Jul 2025 01:50:16 GMT  
		Size: 39.6 KB (39596 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; ppc64le

```console
$ docker pull redmine@sha256:3eff1a602f41819039b5e882ae4e6156d373242298220c5d69f1311b2ddcbb47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185887871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c9ee1c6737feb2d444abc4b2e44506acd95120532bb1e86d9933f64479e372`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:00:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:00:32 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_VERSION=5.1.9
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.9.tar.gz
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=cc0ddafa6fe6f5192236a27cec64e3466023a12c92c1da4abb680248639f678c
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:00:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:00:32 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:00:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64403cfcff3618b1b2794e115b532a696917e51f3853d14aa8d5de99a1094f8`  
		Last Modified: Fri, 09 May 2025 01:08:19 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8034b582ce33d0efea676a0a2fb007ce83729bbcddb733790ff3e85d671f0a6`  
		Last Modified: Fri, 09 May 2025 05:44:20 GMT  
		Size: 31.4 MB (31389785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095c1d153e711b39a7d23cbf345902012be3db102566ac58f93c55475f4dfa33`  
		Last Modified: Fri, 09 May 2025 05:44:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f27c3a484ff9c98691f491fa40c5a26a6682ea34fb7814b11b13531346a6d8`  
		Last Modified: Tue, 08 Jul 2025 00:54:44 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50889aaab1b6723b2b94b18884ea13ff9aa84cb9292243920d77ced7dfb93f3`  
		Last Modified: Tue, 08 Jul 2025 00:54:50 GMT  
		Size: 74.1 MB (74096563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daad77b0a4149ac6604dd8118bda00d4efb1629ca94ff0c18ed41eda763df9e`  
		Last Modified: Tue, 08 Jul 2025 00:54:46 GMT  
		Size: 1.1 MB (1087723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ff69ff95fc1b5cd2fbdce88419535d4bd6e608e8a08c1e97f7436e3deb33bb`  
		Last Modified: Tue, 08 Jul 2025 00:54:45 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1c5b98f80e33affe8bc5c720bdd1bcb158398d0e57d24d76ec1e35e3920e0`  
		Last Modified: Tue, 08 Jul 2025 00:54:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5f0bca2561804a90fba5532310890d1f67344497dc6799a9c54d9c0c298f3`  
		Last Modified: Tue, 08 Jul 2025 00:54:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dd5d1d4e5acbaeee49bc5258d19bd1b3f618cfc2ee2a84a94c4a3abf9abf97`  
		Last Modified: Tue, 08 Jul 2025 00:54:45 GMT  
		Size: 3.2 MB (3249903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c95778f1d622056e70d814cae0df49e54e86185cd3d32344f92c735c4b8df76`  
		Last Modified: Tue, 08 Jul 2025 00:54:48 GMT  
		Size: 72.5 MB (72485568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc61560cafce68944d77dd8256ed661efe5d33805f829ace677567b5cbcfd0`  
		Last Modified: Tue, 08 Jul 2025 00:54:45 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:2ac0a54ec328b97842e5a62b9a8b473afa9bf529cbf977fb3d2b05fd176934e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 KB (39685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0745f6cef16f8ea31dc6ee60cf2f92710a12773c777f5a1b3236e4d96f5e6f9c`

```dockerfile
```

-	Layers:
	-	`sha256:efc03fc762f082d1b3189b891060a328b63cbf487856109f6514ca7d76e8e78e`  
		Last Modified: Tue, 08 Jul 2025 01:50:19 GMT  
		Size: 39.7 KB (39685 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; riscv64

```console
$ docker pull redmine@sha256:42930436980e3f87d8ffc52e386aa6b7854d6286c94d45d41691e21a6ea07dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182277127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74f5d7a5ce05f2e6729a87de8155a06b45103089f002dc8b22a364ed6ab2d44`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54551e4382c55dde49be426f193ab43d68f0dc67bbd9d53e416b8b3ec8e530b4`  
		Last Modified: Mon, 17 Feb 2025 07:19:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f24fc982414ac4e1e43af7ca4c2fb10bbcac4891954f60da84f6a75af874f03`  
		Last Modified: Sun, 18 May 2025 13:50:37 GMT  
		Size: 29.8 MB (29798095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a196fa083a31c1786c5d10231721e769fd975a4ce38bbe2dbab5af1b44f6488b`  
		Last Modified: Sun, 18 May 2025 13:50:35 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81449399899c1e63130f0439455b3d71b2d8479ae120cd90b1c448c0e81fb3b`  
		Last Modified: Tue, 22 Apr 2025 04:03:25 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4343742355ff0dc0f12cb2d6f2c7d6347ca447d382b0890062a3b2646ae5cead`  
		Last Modified: Tue, 22 Apr 2025 04:03:36 GMT  
		Size: 70.8 MB (70848430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4131f496dfbf2e92efd676ae6d1ac8962ecbf92ebeaa570a2345a294abe48daf`  
		Last Modified: Tue, 22 Apr 2025 04:03:26 GMT  
		Size: 1.1 MB (1136891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a48a170283105cf5bd8d7d7259c0772ed95f4f812b024ab74639d73fd6bfcb`  
		Last Modified: Tue, 22 Apr 2025 04:03:25 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fb663fc3b556572070866e4956c6348a09916be5a4b109cf63cb3d51d824c3`  
		Last Modified: Tue, 22 Apr 2025 04:03:27 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24db85a2b56972e07c500d9c77366e51f63f5695610b735322af8ab8e60d1b3b`  
		Last Modified: Tue, 22 Apr 2025 04:03:27 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7931f9602a13d44e259b7fe6d45f6b276c56746a96ffcfc79592a9724808a9e`  
		Last Modified: Tue, 22 Apr 2025 04:03:28 GMT  
		Size: 3.2 MB (3248089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad2413dfe2cc441c8835cc5cb37affda5e1d64514f1ee520ca31b8cbbc6c9e9`  
		Last Modified: Tue, 22 Apr 2025 04:03:39 GMT  
		Size: 73.9 MB (73890204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03247f95e013b9b7dc4c2bdaf7b27cce3ef54dbd6781e08639b67da2dc7f903e`  
		Last Modified: Tue, 22 Apr 2025 04:03:28 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:1b17776d423602d2530549bbbbf1a9ed64b55c89a10b699aafc0449288fc3743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00a3fc0f30669795a1084043b5d9e527b534c454ec49b2081d224b80eaf6316`

```dockerfile
```

-	Layers:
	-	`sha256:8cd4778967c8fa06d5a2d8c63eb2c89eec6f668e294ae1d97ac79c0af6644060`  
		Last Modified: Wed, 04 Jun 2025 01:50:24 GMT  
		Size: 40.6 KB (40627 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; s390x

```console
$ docker pull redmine@sha256:acfecd6e8daa4dd3131e4e20c66cc94db036752984063977a42acc6d549fe165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183563576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68969693c7cc08be8b06bb424e0fd32f073c47f310daaeef1bd25dd88a83d993`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV LANG=C.UTF-8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_VERSION=3.2.8
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Wed, 26 Mar 2025 11:33:53 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Mar 2025 11:33:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 11:33:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 26 Mar 2025 11:33:53 GMT
CMD ["irb"]
# Sun, 20 Apr 2025 08:26:13 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV GOSU_VERSION=1.17
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_ENV=production
# Sun, 20 Apr 2025 08:26:13 GMT
WORKDIR /usr/src/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
ENV HOME=/home/redmine
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_VERSION=5.1.8
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Sun, 20 Apr 2025 08:26:13 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Sun, 20 Apr 2025 08:26:13 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 20 Apr 2025 08:26:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 20 Apr 2025 08:26:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 20 Apr 2025 08:26:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 20 Apr 2025 08:26:13 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 20 Apr 2025 08:26:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b693562415b7f437cd80ccbaf0711f61a5adb8f0e25ac8276f1544c3a6cbd295`  
		Last Modified: Fri, 09 May 2025 01:08:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1036e29c9006f215f22acd5b63ecaa6cf027e0cb1c22049431279e70e4cf4e`  
		Last Modified: Fri, 09 May 2025 05:44:21 GMT  
		Size: 31.2 MB (31233289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0866e40f4777cde729561ad0024197e2ab69df1cbd2979b9c52031247e91aa7`  
		Last Modified: Fri, 09 May 2025 05:44:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54738bc93f003502ab4a05284956531802f8995324273f5a31335e2d1f9eb37e`  
		Last Modified: Fri, 09 May 2025 12:58:07 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab175f9a3877a1557aca6e87236a42f5669a75005b3c4ae9b25d15da623b433`  
		Last Modified: Mon, 21 Apr 2025 23:36:46 GMT  
		Size: 72.8 MB (72769927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a240e0f695a32ceebb3c331bd9500a20efa273e97a6650a7757206517525aeac`  
		Last Modified: Mon, 21 Apr 2025 23:36:44 GMT  
		Size: 1.1 MB (1131707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350fd0f3b11b74520024f5a0449331101bf48df0bc9cc770acb18ca49babc4bb`  
		Last Modified: Fri, 09 May 2025 12:58:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aa18be3fe2f6b9d84e38330992528a36959306d09f564be727b1ce0da89a0e`  
		Last Modified: Fri, 09 May 2025 12:58:07 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d1788e992036a68db8daab44dd24664d9c3fbc40e2f2e49596f76fdd262402`  
		Last Modified: Fri, 09 May 2025 12:58:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0f8753d551c7330ea70b8d0e92de995d8d29b7a286bf8dfb7035f2ca95ca32`  
		Last Modified: Mon, 21 Apr 2025 23:36:46 GMT  
		Size: 3.2 MB (3247992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ecc0ce61a161ea5e41498e777ae13cc0a121e9318e1f4363f3fbdb46be26b`  
		Last Modified: Mon, 21 Apr 2025 23:36:48 GMT  
		Size: 71.7 MB (71709108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072e1cd2bc83ec98f04440aeb055465d0d7479226495ebfe2b9859051d288832`  
		Last Modified: Fri, 09 May 2025 12:58:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:b9f26b4dc7140d2e930e80bac21fad4f52382c767d2bb5b0ed3522aeb747e1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0190df0b5b2237f4035451968d64920fd1e03bd1e45253fc8fc84b61c2dd3cd5`

```dockerfile
```

-	Layers:
	-	`sha256:b98b403907b0e7000d7da168713db62216d93cfa20ec09ef0073c38a90f2cdc6`  
		Last Modified: Tue, 08 Jul 2025 01:50:26 GMT  
		Size: 40.6 KB (40559 bytes)  
		MIME: application/vnd.in-toto+json
