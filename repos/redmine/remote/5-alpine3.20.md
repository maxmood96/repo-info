## `redmine:5-alpine3.20`

```console
$ docker pull redmine@sha256:5fff7b721a46b4bc619aa0221d98a59e0ccfb53f58d6f2bb824a3026a8940a48
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

### `redmine:5-alpine3.20` - linux; amd64

```console
$ docker pull redmine@sha256:079d9cc017e37359ea39490280d63b45881660271e440810852306922d80ec9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181949363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed577ee482a611de4a541aad0e43572e9650c6c0e2b718cde08ebda99a141aba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ffb0df9e67a13fbefd16873f6ed1e4d21c0fc13b33a36c6b821adffc903685`  
		Last Modified: Thu, 08 May 2025 17:05:18 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7999427950b9a0b6c9eab0b79e8568d42251b1bc6a207deb7ed4c3d5b2c1a0e`  
		Last Modified: Thu, 08 May 2025 17:05:23 GMT  
		Size: 33.5 MB (33512659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449674d5ae355335fc8be189228d0015af72b9c199f09cc250d98e00af77792c`  
		Last Modified: Thu, 08 May 2025 17:05:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524fb96adf5fd77da6a9140f8696ff2c5e5dd1d65b84b6df946e2e9014ed6e5`  
		Last Modified: Mon, 21 Apr 2025 22:36:26 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0fc9efa09718da78cde5dce2caaa32cec9c5f919f91b4f0ea49df31b53d5dd`  
		Last Modified: Mon, 21 Apr 2025 22:36:27 GMT  
		Size: 70.1 MB (70077120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3e6065167cc1fa7bc183d9f5dfbda66e47740aa08d0eccfbc422450c19a605`  
		Last Modified: Mon, 21 Apr 2025 22:36:26 GMT  
		Size: 1.2 MB (1166521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e765646ac7688db2c105fdec8a86092a41f070d0cd1544acb244572ff8220689`  
		Last Modified: Mon, 21 Apr 2025 22:36:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226f68b180381caf98e0c0d407f40ae0fab7fe1bca893383a67ba59b22104091`  
		Last Modified: Mon, 21 Apr 2025 22:36:27 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453d271b15b1705e876b41aa0f5373d199e9141fcba643f4a6494c3ea107a7e4`  
		Last Modified: Mon, 21 Apr 2025 22:36:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870835d7965d8b829d59a051000bfa0398e0d95a16d95157d6a5a3b0b288a80e`  
		Last Modified: Mon, 21 Apr 2025 22:36:27 GMT  
		Size: 3.2 MB (3248011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a7abca7931d987e30f11543aacc1ae911b965de9b941fff91a9dfe1ef03883`  
		Last Modified: Mon, 21 Apr 2025 22:36:29 GMT  
		Size: 70.3 MB (70314156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9947375008a6527b82e31b08e9207815013715c027338551fc09a9f21e72f7a7`  
		Last Modified: Mon, 21 Apr 2025 22:36:28 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:d4aefa541fc943cd7c472a788177adbf9193f51a66246216c35798d3baa5202e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721565fdeaf6ab4451a172e90aa9568c58cc9c6d846327b7570ff0fc86911fbe`

```dockerfile
```

-	Layers:
	-	`sha256:4ebb50c2cf803d7724a8cb08c76f6d624b0d6a6e2c16668dc55625d1841afabb`  
		Last Modified: Mon, 21 Apr 2025 22:36:26 GMT  
		Size: 39.6 KB (39635 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:f783795b1764c508cc2270166f08dd8adf97fc0c0e8d650c67430664ba4e027c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174869982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521db68242f938754fd095b3edfed8194918e1a9260cf49863d14cfe2c96bc60`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c33e30311f7bfd2e574783afd81b2b022925223ace47a3475b924f32b157bc`  
		Last Modified: Sat, 15 Feb 2025 12:58:07 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b350a40c236f02bf7989a41a42775950cb805ab2f8aea76c95ca74a37f7cec7d`  
		Last Modified: Wed, 26 Mar 2025 16:32:32 GMT  
		Size: 29.9 MB (29858818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfe9bdad3f4c0b817403e27eb3dfd8606db9a12f4367c125c79182ec03c051f`  
		Last Modified: Wed, 26 Mar 2025 16:32:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fe8afe2824cbd2638fa6f7c5102e9a543f47dfd4aea4f8ed69a44cf4f81e6f`  
		Last Modified: Wed, 26 Mar 2025 17:14:19 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4168d58c0c402c9e32c1447b396a8f74feff0ec1b844a5a34e11f07bc6ef1a52`  
		Last Modified: Wed, 26 Mar 2025 17:14:22 GMT  
		Size: 66.8 MB (66837677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f5a98a2a1eb8d4a31c7ad8e0277220f433889dba8988764bd206ff258bd58c`  
		Last Modified: Wed, 26 Mar 2025 17:14:20 GMT  
		Size: 1.1 MB (1133546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45c045288a9df3d7d49e8a0d54ced7e65c2775a19ef48fe02c7852e64cc6a2d`  
		Last Modified: Wed, 26 Mar 2025 17:14:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260f548f4127f45dca30d188edcc80184a1608c082e4d8884d7a92ba138dc7cd`  
		Last Modified: Wed, 26 Mar 2025 17:14:20 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70ebd198491a97624b44b848d0c24ac4b1ec83a7151357bfdcc072ca459d5a3`  
		Last Modified: Wed, 26 Mar 2025 17:14:21 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d1e33f003a7ebc7ed033f3e1f9defaeeac50e947728715c825ba5938930361`  
		Last Modified: Mon, 21 Apr 2025 23:04:55 GMT  
		Size: 3.2 MB (3248023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf45690b3ae329a2c29eba12ebdf567dd08b6f34218c4acfabedf2f98d68d96`  
		Last Modified: Mon, 21 Apr 2025 23:04:57 GMT  
		Size: 70.4 MB (70415394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4716a9fb4d53637af088acd6b4307ec9d55988ad021e791b21ddeb80332694bf`  
		Last Modified: Mon, 21 Apr 2025 23:04:55 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:227db64f40b087ec370165085e213470d671807a14b4f37e7f70614d787a79db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6292177664bceef9d4711edc4d5749f79fe2f6f1ccf74caa991b23d3b3d3dcde`

```dockerfile
```

-	Layers:
	-	`sha256:2aa877df5da7ecd032f06ec605ad59007f1c9bc71ce29462312eed14be89ed6b`  
		Last Modified: Mon, 21 Apr 2025 23:04:54 GMT  
		Size: 39.8 KB (39781 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:07ec16391e1f8828b1f43589274aa987bb82055720ef691e1bd84e268f52ef32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170046612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7121cfbac016d9151d6467daae458595190533af9b147376241452770913ed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2a1abd79c8408aeb5068f398ee58dd6d205ac18aea943b7042904720577fee`  
		Last Modified: Wed, 26 Mar 2025 16:43:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06785d910c705eafec499a8c861e619127d53d29f716d74b32661f989f54d77`  
		Last Modified: Wed, 26 Mar 2025 16:43:59 GMT  
		Size: 29.7 MB (29695296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d291d31f5ab55b1bd2cecbc8f5269d8ffde3f99425171ca2b3829f6ec7d3a325`  
		Last Modified: Wed, 26 Mar 2025 16:43:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecf2aecc7cb00c2347d345602666906497d95edcee89d3e3ba177bff68f498c`  
		Last Modified: Tue, 22 Apr 2025 00:15:14 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e98f7290910f1868525cea392f92170e2b755be46caf14d70f58c7b2f532040`  
		Last Modified: Tue, 22 Apr 2025 00:15:16 GMT  
		Size: 64.2 MB (64196308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f66dbd9e68dad540c40b74c4991f59d3e6ce70efd7af243feab099ced7d7b6`  
		Last Modified: Tue, 22 Apr 2025 00:15:14 GMT  
		Size: 1.1 MB (1133500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d906261bfa3a0b96a36702f6cc2976b44b420c40d0cddf3d4af0e292af3fc86a`  
		Last Modified: Tue, 22 Apr 2025 00:15:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d27ce95d06406f67acc462b18e6091a365548fe2bd4599b124f4090d5c2a392`  
		Last Modified: Tue, 22 Apr 2025 00:15:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0453e81795275b0a26e3d67576671756c95de9f211d9734684aa51e43891c69`  
		Last Modified: Tue, 22 Apr 2025 00:15:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f04b271e101a63e113d27567b91b09aac11ef4d9a77e6c749a6b4597ef72662`  
		Last Modified: Tue, 22 Apr 2025 00:15:15 GMT  
		Size: 3.2 MB (3248019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2675972fd00f89485460c503d84974b6d200527653e9485a26da31ca8d56280`  
		Last Modified: Tue, 22 Apr 2025 00:15:18 GMT  
		Size: 68.7 MB (68673529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4a998e5b2f2a674fd50b9566b13f8c94171e96557b25092e358880ad71cc9b`  
		Last Modified: Tue, 22 Apr 2025 00:15:16 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:7724d93cccaf68785adace63f15d2aa2231dee592add810713955a74b13024d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e5c64fe3638ec160d666881be3a6014977a68c66dcebc5efd217c7a4b0cbc6`

```dockerfile
```

-	Layers:
	-	`sha256:1e21cde08cd64e32af2e067d83f9285f1b3a9c55227cb7b4e44f018c6161f70f`  
		Last Modified: Tue, 22 Apr 2025 00:15:13 GMT  
		Size: 39.8 KB (39781 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:4f9bc12419c769fd55c35a0859273d6eb502db01be2eaba55453912ef004d286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182946534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfed17e17211c5fe916b3cbded8fbb2de58f54cb553f554212cd16ce80bb4c69`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba2c2dd90d8650ddbf5aba6d465177a4f93b2d732e0b9fb5742f8c1129423c0`  
		Last Modified: Wed, 26 Mar 2025 16:40:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecabfc130086803c444a4e6d976974d473a6378d8381b34d0f72686c302ee4d`  
		Last Modified: Wed, 26 Mar 2025 16:40:35 GMT  
		Size: 33.5 MB (33512045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c86a3b81eb5fbfff77708cd0b209084cd8ac26e5f15afa13ace6f61ab1cdc3d`  
		Last Modified: Wed, 26 Mar 2025 16:40:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd57b7e1ed17232534aa9e245e4c4805f07db99f2efeaba541b32be0b32550`  
		Last Modified: Mon, 21 Apr 2025 23:55:55 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5877d23adc8ab05963621276145d65143dd3ce2cd60d6a70942b292a695ba`  
		Last Modified: Mon, 21 Apr 2025 23:55:57 GMT  
		Size: 70.6 MB (70558565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6579150732aa13dab0d62e190377699e1980ac9df249902377672e7b08b0788d`  
		Last Modified: Mon, 21 Apr 2025 23:55:55 GMT  
		Size: 1.1 MB (1093152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095e8145811d732a8ce2b4b75e73ba7799d3a5bcf6a798571c17a1d881bc4034`  
		Last Modified: Mon, 21 Apr 2025 23:55:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040533e79d50d59ab999f6ada6c6e7865e5a326085e80c4786a3abac610abb8c`  
		Last Modified: Mon, 21 Apr 2025 23:55:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ac826df9240b23aff6459a3b3eaf8846cab1bb8c63d8598a27338568df5ea`  
		Last Modified: Mon, 21 Apr 2025 23:55:56 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639df8059bb8b3a60df4ce1757ea9bd54866b53de1f7b8c391fe56ab6afe085e`  
		Last Modified: Mon, 21 Apr 2025 23:55:57 GMT  
		Size: 3.2 MB (3247983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee18bfb0902dbb79252e2f14002078226f3eae3722169740f76b16c08489af98`  
		Last Modified: Mon, 21 Apr 2025 23:55:59 GMT  
		Size: 70.4 MB (70439631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328d996cb750786f012f4b979ba9f91f4960c727254486b9ce0947cab4823e38`  
		Last Modified: Mon, 21 Apr 2025 23:55:57 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:6808584de4051f804db9992dddb0a9505d57b946fc4ef19753b0cc37c269b733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffddc910f94001b13b92c8f51b550fb3eb5c4d389f297cf4c55fafa1c451e85`

```dockerfile
```

-	Layers:
	-	`sha256:80f3032e1d0a171b75423500477de3b108cf0fa1c8021b4473c35c193028a460`  
		Last Modified: Mon, 21 Apr 2025 23:55:55 GMT  
		Size: 39.8 KB (39817 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:2c96e5c2edc329afaf2799f47d37957f001c0abe9402a518d3ad5f8d4e51bf92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178851566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb0ebed3b8b7a1db94352b5f27c4b1fe82cec6edb19b08a6b21050bbbf89bc5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5002de7ccf4a83110755351c4bd4398aeca0f9c208339e6ff98a9b134a945f`  
		Last Modified: Wed, 26 Mar 2025 16:28:37 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba82825f875c8d320fe8fa1a7e3ddec11a2b3bcdb08f2533c894a2a2c365d76`  
		Last Modified: Wed, 26 Mar 2025 16:28:39 GMT  
		Size: 29.7 MB (29723128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b5cf1cdd0ca7b730d9bc2207ec4c57128ce68da9c05ebbd60805ba972e22b3`  
		Last Modified: Wed, 26 Mar 2025 16:28:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72da55cf53f42c1fc898cab34f686638b4f738a90481dc0e861a41ed667228ef`  
		Last Modified: Mon, 21 Apr 2025 22:36:43 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f683e52e1bf385e6dadb31a413ac9d29ada1744cde4d5832824e36516687bfce`  
		Last Modified: Mon, 21 Apr 2025 22:36:45 GMT  
		Size: 70.8 MB (70831970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dc685fd49c01dc0f1da4594cf81be329de59cfdd44df8254e75b8ab733c807`  
		Last Modified: Mon, 21 Apr 2025 22:36:43 GMT  
		Size: 1.1 MB (1141462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eb121abb23988fbe55f74a8869e6ea30a3bc98c66871a5e7393a4a03b151f0`  
		Last Modified: Mon, 21 Apr 2025 22:36:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfe563a17789a615f178f61b8c539847a857a72c85cebfab025f09c6fe9b306`  
		Last Modified: Mon, 21 Apr 2025 22:36:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49df1c07a821fbfd5fc6a5e3c9589c413f0aadd824c03eb1e517c9f9c98ce05f`  
		Last Modified: Mon, 21 Apr 2025 22:36:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27830541353f3cfc90dcd33a41c1ece2a720ddd9d4c940e86bfc205356209f4`  
		Last Modified: Mon, 21 Apr 2025 22:36:44 GMT  
		Size: 3.2 MB (3248023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58a481a91acb22f36884d966b66fe5c28a2239526e2f473ba71c464a5d365cf`  
		Last Modified: Mon, 21 Apr 2025 22:36:47 GMT  
		Size: 70.4 MB (70431319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9947375008a6527b82e31b08e9207815013715c027338551fc09a9f21e72f7a7`  
		Last Modified: Mon, 21 Apr 2025 22:36:28 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:ed7c51a6580348fa590ec13d91a6b4b2bae8c1ccc8f59cb892900a2699701eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efe74533ada7ca9d0ba741e56f8208ed7421eab1fe16aa1ea95d67aa4c8133e`

```dockerfile
```

-	Layers:
	-	`sha256:921b18e2ce3c5ee6b50a2b7de1dac53073056e3c701f7c25a218da08530477b6`  
		Last Modified: Mon, 21 Apr 2025 22:36:42 GMT  
		Size: 39.6 KB (39596 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:c3593461e1bc5990405ba6d6f3e6bee831804cb68d46bc02bbe44ca98a64295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183001362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed30d23073aeb7f5d8ce92a6f522662fea36c3e47922ce2f3a8aded8aee5c61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee75c986061a4fb3856d5d3395d81aac1db32a542e9fcb7245b0b0be06ebb1`  
		Last Modified: Wed, 26 Mar 2025 16:40:47 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc117377c2bc98243c23e915e0376e7a0b10419001b00e5f2ccf8157b2e9be`  
		Last Modified: Wed, 26 Mar 2025 16:40:49 GMT  
		Size: 31.2 MB (31151998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43017f66116b14f9d2eec493b72c048227984401d2ac5dbe445999ec412514`  
		Last Modified: Wed, 26 Mar 2025 16:40:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70dbad57fdb05be69cf6534c93957451b0d2218972769a65d1759af164c28e`  
		Last Modified: Tue, 22 Apr 2025 00:27:35 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e49079a50606bad33e3bd25058b78e662e4ef8ddcb18706cf2346ae50a95598`  
		Last Modified: Tue, 22 Apr 2025 00:27:38 GMT  
		Size: 71.8 MB (71783675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f69b47e80ee18f601e3d3869bd3da498988df9f7d5a8d2519abd564e03688`  
		Last Modified: Tue, 22 Apr 2025 00:27:35 GMT  
		Size: 1.1 MB (1083801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baf3550051fbfbafa8e7cef080a6872352e85b69e6ef43b5a2773e60a1895d2`  
		Last Modified: Tue, 22 Apr 2025 00:27:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ad26cbb444dab34be7b94b053823314718572726a9312070382234c3030a6`  
		Last Modified: Tue, 22 Apr 2025 00:27:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1535e771b4aa3c892d2f7a8d1ae3d79463efa3c1ca3020685d6d700b81c50c`  
		Last Modified: Tue, 22 Apr 2025 00:27:36 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6622d7fcf6fffd038784f37bddccbeff535cda2dc1e8f23fa07f10ad89c8053b`  
		Last Modified: Tue, 22 Apr 2025 00:27:37 GMT  
		Size: 3.2 MB (3248030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed5536f18911ddedd916b663492c3babf8034814aaa8617c63f8ce389593c5`  
		Last Modified: Tue, 22 Apr 2025 00:27:40 GMT  
		Size: 72.2 MB (72154188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec749c69b6d97ca0523cabbdbf6663e20c14f80ef03d9c0ced49d4fb626b6d1`  
		Last Modified: Tue, 22 Apr 2025 00:27:37 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:3aa38f5c610ff2f399bdd44dd549e182321c47368dbb67bf0fd593108ef85547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 KB (39685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202057d62d0293aaec64c1971d12733837e354c329654411a98d197ad0cd3b2f`

```dockerfile
```

-	Layers:
	-	`sha256:6df126ccde6efaebc3b7cd548024977b780c45e958e26189ada4bb2225d23bce`  
		Last Modified: Tue, 22 Apr 2025 00:27:35 GMT  
		Size: 39.7 KB (39685 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:11691509304fd1a439348caa4e0f5d82db65140ae953bfff0df3cdd62e57290c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181769766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce60a074c00d844bb69dffe4907b32082de9f2acdb3a6451a1a1e07981ab41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 19:30:36 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cd13f0347dd4833f5941662d6b8aac773d7dd4aa9f99b546f2070234b3130e`  
		Last Modified: Tue, 18 Feb 2025 20:50:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8630cba80784c9a357fa5a71b8a24f44594d4359d8338d9e435355c6dacc88`  
		Last Modified: Wed, 26 Mar 2025 18:25:18 GMT  
		Size: 29.7 MB (29664932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5981ac7f6a549a4bee49c0daeec70c356e52990b3cef93cebe83c2f7f175b377`  
		Last Modified: Wed, 26 Mar 2025 18:25:13 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3893ca46329639091c8c7653fcd6519dd1e4327363758b735d4357ef62f4a`  
		Last Modified: Tue, 22 Apr 2025 05:01:09 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03439f1f02e773f129ba5705932022e0007767b055cb4064887e2bcc004ea21d`  
		Last Modified: Tue, 22 Apr 2025 05:01:20 GMT  
		Size: 70.5 MB (70465906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176e498e1c302fb201f32e74d7cacbdd080b18e45fc3195988d11ea022087a37`  
		Last Modified: Tue, 22 Apr 2025 05:01:10 GMT  
		Size: 1.1 MB (1134842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e76f890116e25102e1773aadd8a9c5b1068bfd4b14e3911649d3c9c8fee70c7`  
		Last Modified: Tue, 22 Apr 2025 05:01:09 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e862f1fc539ef166c0d9235a5e559216431d77bb88652df5192487f5e8601fe`  
		Last Modified: Tue, 22 Apr 2025 05:01:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f90c8c3d31f5711c4ccc34ad19329ba7ae1d64f5b98cf33c157ccb7738dce9`  
		Last Modified: Tue, 22 Apr 2025 05:01:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b601d590b444bd4a3fa1b856e65a02aed00e3c4facbca8d50cb2ce4fd88f`  
		Last Modified: Tue, 22 Apr 2025 05:01:12 GMT  
		Size: 3.2 MB (3248018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed7501853e90f6b9aec15555bf90a5703ee9264daaee48bfd72c5d219c626d8`  
		Last Modified: Tue, 22 Apr 2025 05:01:22 GMT  
		Size: 73.9 MB (73878842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254622ddc78793a4bdd16964bd0a2db2e6304d7fe6ec7f15cb99b3cc61b94f5`  
		Last Modified: Tue, 22 Apr 2025 05:01:12 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:6951cff7773b8487989f193b385a86352f3b10cd9cabbd2e66c63f1cdfcf61d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 KB (39685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6652669d1e59f3838e3a92219d5a3dab577c8a6f428325d27606b8f0fe8331`

```dockerfile
```

-	Layers:
	-	`sha256:6f0f78cc593a376a831a7fa7331d0f9004ee2a6e4200d740bf884fd4ee61c46f`  
		Last Modified: Tue, 22 Apr 2025 05:01:09 GMT  
		Size: 39.7 KB (39685 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:bc5eb29ac5b7342a4183fe9f68db15b13b93c3dafff373d6068979263bd2a3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182351183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d912486079c49d2fb004767760629497df2af5ca7e144bfe43eae38e904347fa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358c19d19e5fcc3b0eb1434fc34a507d44c2b194edc42c61b7baa654ac57a49`  
		Last Modified: Wed, 26 Mar 2025 16:37:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a107beabedd427f5f907a7166e9e99cf71411b3e92913f09aa8227c5f605c405`  
		Last Modified: Wed, 26 Mar 2025 16:37:11 GMT  
		Size: 31.0 MB (31020875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71213bfb0aba644c83cd919c5c2867257a57825961fc4475e766ec59582d29`  
		Last Modified: Wed, 26 Mar 2025 16:37:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a73931167b74713ccc8897e6412533ebbb6033b889de3afedfdde23ca69e4d`  
		Last Modified: Mon, 21 Apr 2025 23:39:30 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7051eaf455990b2b007882ecb0d7b61979b50198825e75fa18f5e708ba992be0`  
		Last Modified: Mon, 21 Apr 2025 23:39:31 GMT  
		Size: 71.9 MB (71941069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02353c1aa2cc1e801479fbf6222eb1fcb8277418082b367f9f9c19e2d7b37009`  
		Last Modified: Mon, 21 Apr 2025 23:39:30 GMT  
		Size: 1.1 MB (1131155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e562ad00b9c413fd1442262e141a45fd5a35b4cecccb150c412c62c04eee6cc6`  
		Last Modified: Mon, 21 Apr 2025 23:39:30 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6129adb8f52f10bf083a5144a5cc5ba4889e309b53067c9d19a44e365e005532`  
		Last Modified: Mon, 21 Apr 2025 23:39:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6cdc67f591b45e6fdd37ffbf71344027f156ee8ca869002fa31ff80f79d44f`  
		Last Modified: Mon, 21 Apr 2025 23:39:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e17d18450c4635906d32e803bfe972d7b1182cf587a709faad5e065086ef0a`  
		Last Modified: Mon, 21 Apr 2025 23:39:31 GMT  
		Size: 3.2 MB (3247888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8ba48e5526c70b0aea9d0ed66f1771fe7fb43d9f10e21243f46ed73882bd22`  
		Last Modified: Mon, 21 Apr 2025 23:39:33 GMT  
		Size: 71.5 MB (71542078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e487f61f66d118f2337f684cc3bd812999831e76fb11c8269906e99d4e5b52`  
		Last Modified: Mon, 21 Apr 2025 23:39:31 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:1fca48e1c2b4a7428aa67084f92af282aef3b5b9129e11b2bcfa371fea77f847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8f102a6e1dbf3c6b888656571b758e6982bb44d63311699c8fa93c5e7d38f`

```dockerfile
```

-	Layers:
	-	`sha256:b0ad9a7a684c5c0d57105e28f568a6954b0af4d5ef8084433bebe19b8b268980`  
		Last Modified: Mon, 21 Apr 2025 23:39:29 GMT  
		Size: 39.6 KB (39635 bytes)  
		MIME: application/vnd.in-toto+json
