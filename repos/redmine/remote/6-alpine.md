## `redmine:6-alpine`

```console
$ docker pull redmine@sha256:0b22d92be2bf68af1607df0d5948fdfab72f54c86aa9f12a5b3a6b9be9f93fce
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

### `redmine:6-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:82c98c332c0dc2b1cb08506ccc10909ad96d36997a67b01ce273f86ff2b4871e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196275807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b0cfe1ba06229e97c5307a7131a4d26c305ab71d6266a3cf0e3a8bf012824f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Sun, 21 Sep 2025 14:39:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:39:20 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_VERSION=6.0.7
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:39:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:39:20 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:39:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384b7de5c8f2fb3d8c37d62c25fa66614128499fdef0eae1f9ce06fc7bf85af2`  
		Last Modified: Thu, 24 Jul 2025 18:29:47 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d2cc9f9b4b0dcf7965bcdfd11f0a0d10cb7109cd005052729953b2b4fe12c`  
		Last Modified: Thu, 24 Jul 2025 18:29:55 GMT  
		Size: 35.6 MB (35639389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccc537e8a51e033b821956a72dca3eecbe12f50e8a15843d1423cb39522b30a`  
		Last Modified: Thu, 24 Jul 2025 18:29:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f33f61ad2b6efac84764a12b9d54c1c72a09e26ef33a15986c079ad657f3a4`  
		Last Modified: Mon, 22 Sep 2025 23:49:06 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13f46c0ec1b33e6852c351994303172e9be885fa9d290d096d5e57e1952e1b6`  
		Last Modified: Mon, 22 Sep 2025 23:49:19 GMT  
		Size: 75.4 MB (75377838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5ab1ddb6fcfe767c1740f121c6956bf51709ee535a4edc844a1dd583b9a862`  
		Last Modified: Mon, 22 Sep 2025 23:49:06 GMT  
		Size: 965.9 KB (965863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c9860e797620010b523ba3fca48b74e90bbf2ada5251be0d0e61d57fe88991`  
		Last Modified: Mon, 22 Sep 2025 23:49:06 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12dd2467df781af1e6453dbeb3c04c853a9b4696c67fe9ac71d36060ed3b632`  
		Last Modified: Mon, 22 Sep 2025 23:49:06 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d519863c3c4443787b9556df34aeffbfacf25bd619b404e633636dde8da23c20`  
		Last Modified: Mon, 22 Sep 2025 23:49:07 GMT  
		Size: 4.1 MB (4069898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b216bbae073f7f14a4b9632286fb06776ff6e0af2373e17aa45ea8e2e88865a`  
		Last Modified: Mon, 22 Sep 2025 23:49:19 GMT  
		Size: 76.4 MB (76419282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cdf5c18d58cca49ce4f74f5bd00f7750dad6f82db7fb4e17583aafec0b26f3`  
		Last Modified: Mon, 22 Sep 2025 23:49:07 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:16ab5ab65ba69542ed0cdfd8c97d73480c845b11a9a220b84d32f370db3bd021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebf14e53acc6b5b0e7e5f11a68d5150014535e5712bdd5063cb19fa6678950d`

```dockerfile
```

-	Layers:
	-	`sha256:a762a6cca4bba40627bce537d5cb0590666d41f6e6967e1cde62de44d5883460`  
		Last Modified: Tue, 23 Sep 2025 01:52:25 GMT  
		Size: 38.0 KB (38009 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:c745d89ab996e33f1dbbb4c593f4b6ca0af969a7df459a482c4e1633b35a3ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188007096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180b13a9c864ae4c053cf024bb367b90c1617c0a890b85826518d9c894b5f197`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Tue, 23 Sep 2025 19:31:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_ENV=production
# Tue, 23 Sep 2025 19:31:28 GMT
WORKDIR /usr/src/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
ENV HOME=/home/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_VERSION=6.0.7
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 Sep 2025 19:31:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 23 Sep 2025 19:31:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749f40903fc8c363b20271f0d659c019b7541c985c0fff98929bd8f47ad95d7`  
		Last Modified: Wed, 16 Jul 2025 03:10:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d1d4e03a7fbecd69c3a28cf026859ddd2ac815af3d86ceb0e550ba1c72366e`  
		Last Modified: Thu, 24 Jul 2025 18:29:14 GMT  
		Size: 32.1 MB (32100277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7128ae21f785e1b4597a019e0af372c3f8295d8c4637decedc296f3dee17ab09`  
		Last Modified: Thu, 24 Jul 2025 18:29:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa258513a168c3015bd3959639b82dfebb5baecee9f5f6dfae967621653465c7`  
		Last Modified: Tue, 23 Sep 2025 22:08:04 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0708a200d7b51ba7d36c5bf1189b2156ab5217f8c220de6d4822c96945a4206f`  
		Last Modified: Tue, 23 Sep 2025 22:08:10 GMT  
		Size: 72.2 MB (72158505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab7357c9c317c20d3e16feca3987fe1a9dfd60d641049bb7dc081d055e82000`  
		Last Modified: Tue, 23 Sep 2025 22:08:05 GMT  
		Size: 934.6 KB (934560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbd12c4b14004a5de37ce206a6c8e4242d0c8708fa009c5e70ec27344bfd37f`  
		Last Modified: Tue, 23 Sep 2025 22:08:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477ebcc9df71e18b19f67bab709a318885d47f1b3ce358d8071b216e4321f779`  
		Last Modified: Tue, 23 Sep 2025 22:08:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3d03b9026bfc0b210a03e8940548b8ce370d101367c8eff9e0832f54bc932a`  
		Last Modified: Tue, 23 Sep 2025 22:08:05 GMT  
		Size: 4.1 MB (4069887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ce139063ce517dfd5fbe8cc066163604fc87d10e0753453a9c9bbd70911025`  
		Last Modified: Tue, 23 Sep 2025 22:08:11 GMT  
		Size: 75.2 MB (75239110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e89a43a0aafe9de85e87fd5b176b504551a3fb8bd60352a3aa944b03f72fb`  
		Last Modified: Tue, 23 Sep 2025 22:08:05 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:fcd158ea13ed5eac0aaec3768826bbe46a6674bfdf992897b52759fa76c4a342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d72cb6602f286bafe0a2def0f2f88a7f2a9b921b8ec9d307e0e581a4d5f070`

```dockerfile
```

-	Layers:
	-	`sha256:e35e33d9eba665a858c5dbe17a57ce39a765569bd55e50336815d1afc22432fc`  
		Last Modified: Tue, 23 Sep 2025 22:50:51 GMT  
		Size: 38.2 KB (38186 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:ad6aa05d77d0d0d49d6653f7d52a9caaaa328ac31bec687bf90e37cf43d0b2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183248628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d6a73327d485bb69f10a55b4e0861d22d76a10d7ecbfae9ff9f7705656e97d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Sun, 21 Sep 2025 14:39:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:39:20 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_VERSION=6.0.7
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:39:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:39:20 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:39:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b77cd865d0c67b298abaf8807a4136a70f54c59294ed70401ffdb2b65368440`  
		Last Modified: Wed, 16 Jul 2025 03:17:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b481856eb3c874e37881028cbaaf3a479dc287401717803c9da0f17821e9ffbc`  
		Last Modified: Thu, 24 Jul 2025 21:53:31 GMT  
		Size: 32.0 MB (31962302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bb1dd3d36ebe4fd18546b9cb64247d00ed316bcbf544f675adcde41f8f62b7`  
		Last Modified: Thu, 24 Jul 2025 19:00:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c8e0ed54fca7148278f4effa2de26631d7d56ebdbcf589767ad2558bf6b848`  
		Last Modified: Mon, 22 Sep 2025 22:20:05 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26e60dba9353386617a205e854233048219e228b7bae2bf6733a505b0ef594d`  
		Last Modified: Mon, 22 Sep 2025 22:20:09 GMT  
		Size: 68.9 MB (68946899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddfa982dee39f483bac1916424c00a19a5f1e464db9b7f312a5e7af51e5d15e`  
		Last Modified: Mon, 22 Sep 2025 22:20:05 GMT  
		Size: 933.8 KB (933785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad610f04050b9db0252bf756352effae1eb858039ab09dcf64764c7f2179d7`  
		Last Modified: Mon, 22 Sep 2025 22:20:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096fa53436ea95f283ecb4a98cbfaf10c9fbb91f67566c937fb9ad4e87262d0a`  
		Last Modified: Mon, 22 Sep 2025 22:20:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fcad29c79f1ad47a11f4f317a31d15a510a0f65af32f63fd2ac348537eed12`  
		Last Modified: Mon, 22 Sep 2025 22:20:06 GMT  
		Size: 4.1 MB (4069892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c574978dbd2172ae3119206ba14380c3842eaadcb293b91853e9518d0e2d6e4a`  
		Last Modified: Mon, 22 Sep 2025 22:20:12 GMT  
		Size: 74.1 MB (74112861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd85bdaef55b1ffb2d14ade88a928423ba50409a8f33f1aa31feebe254b6d76c`  
		Last Modified: Mon, 22 Sep 2025 22:20:05 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:a71c0465505d3719b50d7db0861af964d4bfbd182e5cd49cb8c680f5408838fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef154bc4cc4b6d48c291f03f0704d0cbd73e8955a2229069d8db26349e0837d`

```dockerfile
```

-	Layers:
	-	`sha256:7020006d855b8e34c52f9fce2814cea93f218c7f886eb37b614102f7e1777d11`  
		Last Modified: Tue, 23 Sep 2025 01:52:31 GMT  
		Size: 38.2 KB (38187 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:54a95d89dcecbdff2b5c0f9683604300c0ae6e577495cd52ba8924350becbe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196426125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36d4c81984e333fae02bdf31e8695d44f9cbd1beff212d37cbf2cdf7bcd9098`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Tue, 23 Sep 2025 19:31:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_ENV=production
# Tue, 23 Sep 2025 19:31:28 GMT
WORKDIR /usr/src/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
ENV HOME=/home/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_VERSION=6.0.7
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 Sep 2025 19:31:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 23 Sep 2025 19:31:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c09257109ac898fca88b26ba8b5083a10c26c1561d2fdfa48f428f3c19c121`  
		Last Modified: Thu, 24 Jul 2025 19:12:09 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f101a1cb65b95a0ef2947118cfcb4f5b4f57d43a52fdbdec65dfc5ac77c5ac`  
		Last Modified: Thu, 24 Jul 2025 19:12:12 GMT  
		Size: 35.6 MB (35566308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13799c5ed6b81b70be277ee62a00784098d8d512d76b7c554fd881010e1f54d2`  
		Last Modified: Thu, 24 Jul 2025 19:12:09 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e941f26f3f3e067b88175a93cc3d7a21964b952e2ff985a4fdbb87c98f68c6`  
		Last Modified: Tue, 23 Sep 2025 21:32:10 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03990b3bf7307b975ffb577967b2ba63824777bd6c51ee6c7e263eb2703a8022`  
		Last Modified: Tue, 23 Sep 2025 21:32:19 GMT  
		Size: 75.0 MB (75020317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af28653dbc43e84ed1a44f7c5176b12b942a1e40fe8d1c3f18211a34e2ba1f4`  
		Last Modified: Tue, 23 Sep 2025 21:32:10 GMT  
		Size: 922.1 KB (922131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ca78dae093855c64dd2f3474b53dd41445b32bd5688cf146fc0c5e153c1832`  
		Last Modified: Tue, 23 Sep 2025 21:32:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b179936544ba2e5d650532f694c7f4452cb12167592a499012bb32e53f55b1bb`  
		Last Modified: Tue, 23 Sep 2025 21:32:10 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3618c28a977741b4e867a6ca9c657d653cf34166cb51731dbac25ca5553cfe0b`  
		Last Modified: Tue, 23 Sep 2025 21:32:11 GMT  
		Size: 4.1 MB (4069912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab427e1a7786c2fc9dd9326e981a9a5ab106feba2bc3310ba506e2387974459`  
		Last Modified: Tue, 23 Sep 2025 21:32:17 GMT  
		Size: 76.7 MB (76712854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1027ddc05c33ebeb7b5efc6914fca5c52e38a9acd1a7cebf3757e7a31b37eadb`  
		Last Modified: Tue, 23 Sep 2025 21:32:11 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:8ec458c8d61933717168f489e6280eea01a9244a844d132b716897933d4e53e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153a735ee52311a756015b10ac1e8fbd02c78942597831c5d398b5b31aec1370`

```dockerfile
```

-	Layers:
	-	`sha256:7b1f918ce8a4ae4680a483ecb3b705a7bad890f6ccbfe0e92260103203246a16`  
		Last Modified: Tue, 23 Sep 2025 22:50:56 GMT  
		Size: 38.2 KB (38236 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; 386

```console
$ docker pull redmine@sha256:5cb0a727fb9efe96bcaf165cd33148de1a8d584c34d47f63c59955247cfce517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193032379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80959db6d6a9bb2472a8abedde4745e2a2b26cea77113f612b05831b083974b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Tue, 23 Sep 2025 19:31:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_ENV=production
# Tue, 23 Sep 2025 19:31:28 GMT
WORKDIR /usr/src/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
ENV HOME=/home/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_VERSION=6.0.7
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 Sep 2025 19:31:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 23 Sep 2025 19:31:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12b7eb52fa449c9b0aba432b977e6b0695fd9ec6ced94b5ae2d0917d747934e`  
		Last Modified: Thu, 24 Jul 2025 18:29:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221c1aaa8074b3e6c17171630b3cd5d659ad539494c2e15a3a24766d7159e80c`  
		Last Modified: Thu, 24 Jul 2025 18:29:49 GMT  
		Size: 32.0 MB (31978271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eca6b1e23b2530f3d6e9be64a8b96278ba90e83cf48cba3ef556a16ffc22aa`  
		Last Modified: Thu, 24 Jul 2025 18:29:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7150ea0f0c7946fe345630c0e366aae5627eaa907980814d8ed4a649dd4790cb`  
		Last Modified: Tue, 23 Sep 2025 21:54:58 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f4d414348356ea398523c6ab1ba1a1e1a2be0b5d44262a6310a13bb40715af`  
		Last Modified: Tue, 23 Sep 2025 22:51:25 GMT  
		Size: 76.1 MB (76129841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e594df47240ac202b7a4c45bac0eb289d654aa260e33dc3f62bfb95c19b504`  
		Last Modified: Tue, 23 Sep 2025 21:55:02 GMT  
		Size: 939.1 KB (939051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257210261890ba9460bb4b1730dd4d1e2b08dc061e4622140017027c04af533`  
		Last Modified: Tue, 23 Sep 2025 21:55:08 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee7aad810f191e2b2b951c7f5379c701205965a2e1e786c665f1804c5f0772e`  
		Last Modified: Tue, 23 Sep 2025 21:55:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124b20e761aed8f2bcfb21868a6aa09a77be77fc9c24b6eecfe1e2a69e9d6b66`  
		Last Modified: Tue, 23 Sep 2025 22:51:12 GMT  
		Size: 4.1 MB (4069757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dba3fe6118c681455cdee55e119f823794e045396adcab0d21de7301d5a222d`  
		Last Modified: Tue, 23 Sep 2025 22:51:27 GMT  
		Size: 76.3 MB (76296598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4ce9735a4be63547ef9c00352b9b9a5e311174d3c50b7f58ae8a91e88e31fd`  
		Last Modified: Tue, 23 Sep 2025 21:55:15 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:b7c9ad4d538d5dc31bc5acd109cfeb9a234d88aef2695c98eb584b8b4785efbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45e299be9f0496d01e343042024b31aebb633cad27af0d36986a57670e120fc`

```dockerfile
```

-	Layers:
	-	`sha256:4cabb91a06ced4b6f9a260d2fed737097ee24fa692820f2a162185ee7939c858`  
		Last Modified: Tue, 23 Sep 2025 22:50:59 GMT  
		Size: 37.9 KB (37948 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:e6f96fbe59be78b61372110a5aef30718928d631c7ac6706312fc93f1a15ec3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197719387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fe45614531bcb20be088bee89612540e648cb8a219ad53d21970b0460597b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Sun, 21 Sep 2025 14:39:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:39:20 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_VERSION=6.0.7
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:39:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:39:20 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:39:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897bcad2380e05e6ccb43d1c1224d66ccbf31e39c5f494a35ffd42393b648798`  
		Last Modified: Wed, 16 Jul 2025 00:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52155cbf6e208386f6f5ab022c61b2787741d2cda534bbbfaa6fcfb7193058d4`  
		Last Modified: Thu, 24 Jul 2025 21:54:13 GMT  
		Size: 33.5 MB (33483243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33a1359538c744e6ee0e1e9f1e5e83e4f173b979f34ee371c080a1627bea54`  
		Last Modified: Thu, 24 Jul 2025 19:01:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc37618f9aabacb0f46e4d955ade4110cc5dbe4147643a732627a4371213558`  
		Last Modified: Mon, 22 Sep 2025 23:55:52 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6b05f85bb34237db274e34f19000eca7cfc7f928340005486aa0595b3bd491`  
		Last Modified: Mon, 22 Sep 2025 23:55:58 GMT  
		Size: 77.5 MB (77463445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2550bd7d23b6110522dccd5385a2f6fd8515077af5d3e8b0e0afaf01e4107365`  
		Last Modified: Mon, 22 Sep 2025 23:55:52 GMT  
		Size: 926.8 KB (926793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b491a65781d7e99c85d0c6360e3d0e14659320d19ae2cf0eddae2ae69d9531b`  
		Last Modified: Mon, 22 Sep 2025 23:55:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1035fc6f5ecb79b4111dba5c3603ab3cabec677c7c6ed605895852e0b9a47eb3`  
		Last Modified: Mon, 22 Sep 2025 23:55:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea25ed5179e7627f19044b5b9998202712e8e26a6f6a1d0cdd405c51c77b9ce6`  
		Last Modified: Mon, 22 Sep 2025 23:55:52 GMT  
		Size: 4.1 MB (4069869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a658f561f6b28ad4dbe2d9e03a684cad78300f6fb17e193267c6566ab0899e6d`  
		Last Modified: Mon, 22 Sep 2025 23:55:59 GMT  
		Size: 78.0 MB (78045073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cd6369a63332ee8bedf39ebd12b7b76165a38f3a2b8c78cbfcfabdad93d00f`  
		Last Modified: Mon, 22 Sep 2025 23:55:52 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:596affeff3fce6365fda7eed070d973843ad8355f480f7d0d341e86e1f554dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a3a70d913683779d6f9af3b76e169af94b6dba1617d3c3f1ecc44a56b4aa14`

```dockerfile
```

-	Layers:
	-	`sha256:8ce0b0649c363b70e7361c372514445940b6cf89d3952375c5d05567ad711f89`  
		Last Modified: Tue, 23 Sep 2025 01:52:40 GMT  
		Size: 38.1 KB (38088 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:ea8be7be6a1a3004486c3ff400f9b0ec005900aacbfeafc145da1e7cbd2b6c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191980816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2b507217c13107d7b396db89c8c53e0da228058c6d3f0678ee7acc1d0782f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Sun, 21 Sep 2025 14:39:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:39:20 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_VERSION=6.0.7
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:39:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:39:20 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:39:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3905288231d9db3a0fab057825d486ad746db59697d750f674f00bfeee979f9e`  
		Last Modified: Fri, 18 Jul 2025 01:30:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8a218f941e8f339d4b366b40dd1beb052449325260e342be2a8eac783b50`  
		Last Modified: Thu, 24 Jul 2025 19:52:23 GMT  
		Size: 31.8 MB (31771158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70ca7f3fc9114d11cadb7a27959f03e1f0327a2c4f7ae2d4bf8f622f7669f9f`  
		Last Modified: Thu, 24 Jul 2025 19:52:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7bf8178196c5666501cce1ca98a2e58bf388fd450db239cb47c3a5f4963149`  
		Last Modified: Tue, 23 Sep 2025 02:26:56 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3490a77886c3666116ba293b5a80989dd52dbca8493f70cbfea74d073e1caa9f`  
		Last Modified: Tue, 23 Sep 2025 02:27:12 GMT  
		Size: 72.3 MB (72283343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146424d1a879546da4ad0acdef62b5a66a77f89aa1399911cd5e6690b21d541`  
		Last Modified: Tue, 23 Sep 2025 02:26:57 GMT  
		Size: 913.9 KB (913925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399f2fb76e5ca3a1e20d6fe83b7d57fb0d9744d1c7197062b5d62d9a184f6f86`  
		Last Modified: Tue, 23 Sep 2025 02:26:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ba3f253d3863c98bb6a31f4333bd7443a698c7846d2576978a00b93625f1fd`  
		Last Modified: Tue, 23 Sep 2025 02:26:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26105c3033a32f77ed3adb0a74428adcc0927c7db4acd5a8f68d9ed391386fce`  
		Last Modified: Tue, 23 Sep 2025 02:26:55 GMT  
		Size: 4.1 MB (4069934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e2a68faa98b0e6d55dc0d8075c6d64f1dcef5ab1d1583f027486a0403dcff`  
		Last Modified: Tue, 23 Sep 2025 02:27:00 GMT  
		Size: 79.4 MB (79425803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5369f338654dcf4979c0d22601b560e74236fb5bb9203141bf79bdfe7d50edb2`  
		Last Modified: Tue, 23 Sep 2025 02:26:54 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:6002f0b5f219ae9678804f5f9c0bd90180c4bf7c6310261b411790517b519547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eeb449951c6a91adfec1464a883b8dec589e43af73d371f9fa0a0b896d0b1bd`

```dockerfile
```

-	Layers:
	-	`sha256:3a63a387bdd58e17b9a61041957adecf4e5b5628bba521627b7aa689a0234cd4`  
		Last Modified: Tue, 23 Sep 2025 04:49:51 GMT  
		Size: 38.1 KB (38088 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:9413339f8b7c6c5bf54c6e64f49f203898aaa014d8cdaabe433a5f1dcf044824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193665520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40f66e0b17c4d605c187484527119de2996fe710c6ec18530abf5150a4a7b2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Sun, 21 Sep 2025 14:39:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:39:20 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_VERSION=6.0.7
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:39:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:39:20 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:39:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b165588f00306099ed574634bb65ed4b9211498ade906a1602cb03e077aa2e4`  
		Last Modified: Wed, 16 Jul 2025 04:41:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be42f89d9caa3bd043bf99687a891c112e45683b83a72b13f1bd1aa688072413`  
		Last Modified: Thu, 24 Jul 2025 19:51:51 GMT  
		Size: 33.3 MB (33270320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4861d5d86889f08573cbf3a1565450c7be782596e326ea404fc5e6bed9bdfa12`  
		Last Modified: Thu, 24 Jul 2025 18:45:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219175f30af94925b0e5f124659eaddf354a2e9780b6285cb6c65eea547cf476`  
		Last Modified: Mon, 22 Sep 2025 22:39:54 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5668bfd5f2b1d5754ba1f9cf88b5e8590574ed280f4bfb96d571d629e68fce43`  
		Last Modified: Mon, 22 Sep 2025 22:40:01 GMT  
		Size: 74.4 MB (74365339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e726a4f48112a53ae2155c7264f9749650f4ddeca7d173007520ba657065f40d`  
		Last Modified: Mon, 22 Sep 2025 22:39:54 GMT  
		Size: 942.5 KB (942524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a24e882e65f5de39b6b8a51e9c34b8acc6f35035dac87241fc8842ae2b3ab57`  
		Last Modified: Mon, 22 Sep 2025 22:39:54 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81bb3de1cf3bfa51101ebbd4e7f5b9755854f98eaf19cf289374e56d55d3e90`  
		Last Modified: Mon, 22 Sep 2025 22:39:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4ed093f5fef72acf8cc695b9285015557db146538ae354f7c00681642a0344`  
		Last Modified: Mon, 22 Sep 2025 22:39:54 GMT  
		Size: 4.1 MB (4069870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f555fe7053c4a186a1f2d7bdf10f707a1c5548d5dd549297305079c8db937993`  
		Last Modified: Mon, 22 Sep 2025 22:40:02 GMT  
		Size: 77.4 MB (77368644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2265fc1e484f08c505a2ae8c71f5be785386e3f7aae8e20eb46da766294c3f56`  
		Last Modified: Mon, 22 Sep 2025 22:39:54 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:37947f05e6d195d80b00d7cfe3aaefd00cb745c238700e03dc408c013f327b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd04c79a225f1d5e37ea32a92606bd9b9a1a096f6a25125a3b6e32e7bef97d1b`

```dockerfile
```

-	Layers:
	-	`sha256:86bc6d7d2630595ea38d32dcbf7f75f823779dd484ed73e1a48fcc44c250c87b`  
		Last Modified: Tue, 23 Sep 2025 01:52:46 GMT  
		Size: 38.0 KB (38010 bytes)  
		MIME: application/vnd.in-toto+json
