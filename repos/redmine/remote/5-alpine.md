## `redmine:5-alpine`

```console
$ docker pull redmine@sha256:fc7365f540dcbca9de0d51426a07a82e2c7daf5c3be10398f2d90bd1e5a1b987
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
$ docker pull redmine@sha256:5826e0a7efd803f8dfe73aa3a1207afcff768242c594047612804d5d57e2de47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184494400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c6865fe75c6d6c646ead404da5b12dbd99084789167d2b11410351b53b8bac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
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
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=5.1.6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff48a71ea5ac888734d3028b6e17262e09a64a380d483a85c3ce5c880e1f3d9`  
		Last Modified: Sat, 15 Feb 2025 03:09:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cf5834a633a3cd36029631cbcb70f4ab9ae61979b9ee02ec4430cd61d9eca0`  
		Last Modified: Sat, 15 Feb 2025 03:09:50 GMT  
		Size: 33.8 MB (33802348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76efcf95ae0e2cd90e761972bb7508e38c43db9640d9a00e72cc8b20b29d801`  
		Last Modified: Sat, 15 Feb 2025 03:09:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053c70b8699f96116854f6efb8542409b65fa7e2c45fa999534a691c03e698df`  
		Last Modified: Sat, 15 Feb 2025 05:49:56 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f27a5e66514445fec8862171827ed95a877764de585f8bf38dc8ca15f16d64e`  
		Last Modified: Sat, 15 Feb 2025 05:50:02 GMT  
		Size: 72.0 MB (72031898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8390acda96851a689631778ec8174dbc9535bad48b17b0ff88eabb8aaae80f`  
		Last Modified: Sat, 15 Feb 2025 05:49:57 GMT  
		Size: 1.2 MB (1168364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fd17390f6b7e0366a40911161f07d9bffd9232702f41f6f7e6f49f6579023d`  
		Last Modified: Sat, 15 Feb 2025 05:49:56 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784933936e2bf592117ff13ee6d525c398329431a7d09408a5230c405fa0af3a`  
		Last Modified: Sat, 15 Feb 2025 05:49:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c742b1a2396b0c975d292ddeb87a843db4720871716a8aec41c10b80c1977ca`  
		Last Modified: Sat, 15 Feb 2025 05:49:57 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1742c12347000d51c94325466e2823eb37bbd923318ce671815bc5876433ae61`  
		Last Modified: Sat, 15 Feb 2025 05:49:57 GMT  
		Size: 3.2 MB (3244049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fa723b969e0f638a857fea4d0cc4bd0342225f9555d4eefd31bfa041d69a9f`  
		Last Modified: Sat, 15 Feb 2025 05:49:59 GMT  
		Size: 70.6 MB (70601515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36278bb7f58ac9a9d59acda72a1b39bf326f43b14b4d8d823b375748be694edf`  
		Last Modified: Sat, 15 Feb 2025 04:09:01 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:8ea47bde9bf187845001299756ff0c70064f7bda8d2de2e2e80ec7d1510d581e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b048424ac8ae28e9a497884c11925fbd4e75819cec214e1061b08c7020da59eb`

```dockerfile
```

-	Layers:
	-	`sha256:5467be4a49dc14be3620d73cfc03b2ca16a17be618efc8641e12923457b2cae0`  
		Last Modified: Sat, 15 Feb 2025 05:49:39 GMT  
		Size: 40.6 KB (40558 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:be99d34b52629b65e6b95bcf9a550c1f07a69677e55f93040845d238bd6511fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176272999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f228f108fa650abd71d58f46547cffa234d1cbbf2e9ce9dcea64a28334f5f527`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
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
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=5.1.6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10557ebb6bb2572adf43075a3e0ad01cddaa051ed1d29bae84c264720aa25c9`  
		Last Modified: Tue, 14 Jan 2025 20:37:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccea69114d6a590f07b7d46c5fbc447de2686d361a16a85ddce66bcbd3870e9`  
		Last Modified: Tue, 04 Feb 2025 23:21:31 GMT  
		Size: 30.0 MB (30044086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff0992036dc96f5747866e0b88aa74cbd22f240bee5e8f94ee2527d000ce8f3`  
		Last Modified: Wed, 05 Feb 2025 05:42:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3063c3f323dec56875a7b5cdc5e5e2ee50a7e1c5257102864000df089edddf7`  
		Last Modified: Tue, 04 Feb 2025 21:13:15 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e55ffdc5c4e74f194034c7e194d198cea99a0e4d93a6f2e701b5e995923b33e`  
		Last Modified: Tue, 04 Feb 2025 21:13:17 GMT  
		Size: 68.6 MB (68616595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f149e304455239d46dbc50f0c0726021af4d01d9819cfe28692c461b5beb538b`  
		Last Modified: Tue, 04 Feb 2025 21:13:15 GMT  
		Size: 1.1 MB (1134891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7660227d712293af6c6eac78b86617f6a6479e507d611d9b96453ef1674b821b`  
		Last Modified: Tue, 04 Feb 2025 21:13:15 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68822b9e80a5fdb8a3ed2b403a04f213a183cce9e69870df60f55722b77b5b6d`  
		Last Modified: Tue, 04 Feb 2025 21:13:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e66d9a60f724c7edf9fa4ae9cdb606408b2df0d21a02fe2b4fc2d08cb3f4f8`  
		Last Modified: Tue, 04 Feb 2025 21:13:16 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c042a8e87485199f138429f3412f780dc6ced85e4461cc2070f5de261d03c9f`  
		Last Modified: Tue, 04 Feb 2025 21:13:16 GMT  
		Size: 3.2 MB (3244079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae61396166f9f5a3b265fcaa1d7c7feb7915a742e469b4fdf9e2662bc755fa1`  
		Last Modified: Tue, 04 Feb 2025 21:13:19 GMT  
		Size: 69.9 MB (69865480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8975158d5cd246db1e4dea1a842301da1ba9e4470aa658b3985c1361da0fe9fb`  
		Last Modified: Tue, 04 Feb 2025 21:13:17 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:a67819791691113b9c0805c27664d1b23b9f495bf35687f1148f7c05a5784210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7386d0e46224f59da98916c06687db7e013f1d83527757c1c7138fac45b951`

```dockerfile
```

-	Layers:
	-	`sha256:c7b3ede5fbf7a796ec6559bea7fe1490ea843ff5e88e35ab6efb910c65c5f00d`  
		Last Modified: Fri, 14 Feb 2025 23:49:25 GMT  
		Size: 40.7 KB (40729 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:33baa6630046e0c8f142a5440a072ed92f2ccbac3321a08b4b3864e1c24ee5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172118905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea11052dc30094ff9ef2085f4e7e9f01006c84887717b91645587a485ead696`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
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
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=5.1.6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380ab3ef7501f65bfd3ad014abb3f53ea3c8615b29785844d93b4f3e5c68eeb9`  
		Last Modified: Tue, 14 Jan 2025 20:37:37 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbebe0c8fd6defee3ae7bf9a320cbf03b5f2d9cdfefc7cae4fe540e0ba89f4f`  
		Last Modified: Wed, 05 Feb 2025 05:41:53 GMT  
		Size: 29.9 MB (29895330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d42a98494172a4897623fff0b57360ca9b26c2347003a0560f9ba819eeef16`  
		Last Modified: Wed, 05 Feb 2025 05:41:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de726e486220871c88716fe7304f8e34c9c104cc7e9aef8226687312014e677`  
		Last Modified: Wed, 05 Feb 2025 11:41:37 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943f6309ac19af5264335655513b782824fa80a8d0b1fbab39f7b955ef69bec6`  
		Last Modified: Wed, 05 Feb 2025 11:41:39 GMT  
		Size: 65.8 MB (65825251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b57fd408f5a56e10cc5fe8b4b5423d2398a8fcd06cfe9fad5f7fbd7a55f2ad9`  
		Last Modified: Wed, 05 Feb 2025 11:41:37 GMT  
		Size: 1.1 MB (1134869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cd0539064474b689fbe4f5210c8bc42ab8fbd04de2b393606687dea7ab19bc`  
		Last Modified: Wed, 05 Feb 2025 11:41:37 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70d696ac562bfd98eb0cbb3641355ed8269c0719235eb1f0ccbb5a8766bfef`  
		Last Modified: Wed, 05 Feb 2025 11:41:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b9fc4b93b0d71046da82f1535b011652d9210037706456c4f1c59dca73df20`  
		Last Modified: Wed, 05 Feb 2025 11:41:38 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698a7354ce799e4b7a78116542357ce203d6cb7bdc5984f610e36a256495e317`  
		Last Modified: Wed, 05 Feb 2025 11:41:38 GMT  
		Size: 3.2 MB (3244129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f855b6411308b0441cae10d4b3a786c85c91ad15f6c0fb3388578165775c57d`  
		Last Modified: Wed, 05 Feb 2025 11:41:41 GMT  
		Size: 68.9 MB (68918222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f07e8796307844de99a23abee103188ec492d6885bd5247097f955652600b4`  
		Last Modified: Wed, 05 Feb 2025 11:41:39 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:54a056641045ed86b3644ddcce0a141c91a8512c005848269fe9669a0ffa8416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64d364ddf75c76aaa5df80327552425ac2ad3c2c394a172b0bb71f4293d3498`

```dockerfile
```

-	Layers:
	-	`sha256:23f74067a111d24544fcdcc18ebadfa3b8b1320f62b892c1da80ac6a019ceb57`  
		Last Modified: Fri, 14 Feb 2025 23:49:26 GMT  
		Size: 40.7 KB (40729 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:15fcfcece5daadcb0f0d65a343cf081fcc42d4ba1845f9272bdfc27f19debcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184346999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665d1cc8fbcc160852fb7e6cdfc16ab82af76b287afb74a575c95eab70e90dcb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
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
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=5.1.6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8703f74360b1a6cb917d00d2a341f6907f9d3d7b931b3e81a2925142beddb94d`  
		Last Modified: Wed, 05 Feb 2025 08:42:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c88d84ac874cfef45ae2d3b5066d8237b094afc9d19535b5202c7118281810`  
		Last Modified: Wed, 05 Feb 2025 08:03:39 GMT  
		Size: 33.7 MB (33738824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b89d602cfaf42ac9a08200c29fce3023b837185ba8c673d12234efc5bce66f2`  
		Last Modified: Wed, 05 Feb 2025 07:57:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5512fb8ff909b5a050423fadb7c581ab035891613596818e98b3e3474e0122`  
		Last Modified: Wed, 05 Feb 2025 21:15:54 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f001e528c78e5e9fb6d2a2131a66baa81da6aaa8b3b17d4e8320f9db354c5bf`  
		Last Modified: Wed, 05 Feb 2025 21:15:59 GMT  
		Size: 71.7 MB (71659255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e28deee069d5640d2ee3e4f2bf83e208ccaacaca046405e576bbcca082c74`  
		Last Modified: Wed, 05 Feb 2025 21:15:56 GMT  
		Size: 1.1 MB (1096418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0706cdbffc6b37e6d2136b984f59ba3f0ac85e09c2a2e747764782617c1552a4`  
		Last Modified: Wed, 05 Feb 2025 21:15:56 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d13d78f19603f2b62adf244933b9a7ea385bb5f78db4eab9ef2f04ad9c4c8f`  
		Last Modified: Wed, 05 Feb 2025 21:15:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816f1da7cf6f8edfc2cec843dad21ee8677530bea0f8375ed20b901afc5f4947`  
		Last Modified: Wed, 05 Feb 2025 21:15:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd0a6a51ff38b58f20014b366cce9ea660d99d1799d9369931c164b0b130574`  
		Last Modified: Wed, 05 Feb 2025 21:16:01 GMT  
		Size: 3.2 MB (3244101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677cce1c6785b9065f871aa238232d5d3e6716c0fbe81bb663a20623386d51b3`  
		Last Modified: Wed, 05 Feb 2025 21:16:06 GMT  
		Size: 70.6 MB (70612051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adca1678f37d39c7d1cac757a7e665b617db1bc13d32d328fba6485c0e8f16c6`  
		Last Modified: Wed, 05 Feb 2025 21:16:02 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:26f025490374abaf95cc09bd34c61dc8e3e3110699e84ca47164fec2b4c534e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348afcac48a8ea3c2e69400c7265d2ee70af371f5f48daf6bffc9cc1c1d51c58`

```dockerfile
```

-	Layers:
	-	`sha256:52c093000e40a116f63edb3a698fddb2b96e7fc6c383229f0fa181417582aa20`  
		Last Modified: Fri, 14 Feb 2025 23:49:27 GMT  
		Size: 40.8 KB (40777 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; 386

```console
$ docker pull redmine@sha256:689c8c9a1f342cac345bae74380f147dde97364cbbe71d2aa49cee7b023710b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181203883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237106d361c00a9693720c318c787098c6eae04f17b512dbcdbb1392fe04899c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
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
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=5.1.6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58870fd35831dba1efa04c00067a36308153c346bfb4e37baddcf5b557ea59df`  
		Last Modified: Sat, 15 Feb 2025 03:09:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09adefd046c5e78c904d163ecb9d4b6195b17728454a0e1a2d97eb801e428cd`  
		Last Modified: Sat, 15 Feb 2025 03:09:47 GMT  
		Size: 29.9 MB (29911188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76efcf95ae0e2cd90e761972bb7508e38c43db9640d9a00e72cc8b20b29d801`  
		Last Modified: Sat, 15 Feb 2025 03:09:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a44ef8bbb7551f9eb46eb42aeffce44b6c9d6a323f0a6177cca432c3beb70a`  
		Last Modified: Sat, 15 Feb 2025 05:49:56 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8e3706ba721840e51f708873985e43c3b39b1b8b7440718d76d1908981b028`  
		Last Modified: Sat, 15 Feb 2025 05:49:59 GMT  
		Size: 72.7 MB (72719328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6978355ca3ffd9b8636ca1a4d7c5ba23dc5092bb6e8c12d60c30dd3e583968eb`  
		Last Modified: Sat, 15 Feb 2025 05:49:56 GMT  
		Size: 1.1 MB (1143595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60230e2d846ba92ffe35395ddbbe5e89470a38a452841138b1858aa08ffe355c`  
		Last Modified: Sat, 15 Feb 2025 05:49:56 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af26ddf28884faa7cf5ddf0571969b262d51c501e1a9e19f700e9b510a64f86f`  
		Last Modified: Sat, 15 Feb 2025 05:49:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fec247b6cdeeca8f465f4c6051a4662947e2d673dfd5c74975999fd4b5670df`  
		Last Modified: Sat, 15 Feb 2025 05:49:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653c8adb1e9a699b1086929ca3491dce7d14bc8cb0c66eef647a3c26d7f20235`  
		Last Modified: Sat, 15 Feb 2025 05:49:57 GMT  
		Size: 3.2 MB (3244098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c8ded1a56861980ed2419ab7c096a32e4fb88a8127551cefbb9207fb76ade6`  
		Last Modified: Sat, 15 Feb 2025 05:50:03 GMT  
		Size: 70.7 MB (70718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36278bb7f58ac9a9d59acda72a1b39bf326f43b14b4d8d823b375748be694edf`  
		Last Modified: Sat, 15 Feb 2025 04:09:01 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:ad529f17d9c101828be63d5883f532338e10f7e27f0e9126c71114a57e8507bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 KB (40504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26959cf347475691cb06a4566f0c6bb9abcc397f7a7e8f177df05ad2fb003431`

```dockerfile
```

-	Layers:
	-	`sha256:6e90f132df2ca9e1613ae01841460e3adf60cfdba5023e9ed740a62b09db0b25`  
		Last Modified: Sat, 15 Feb 2025 05:49:44 GMT  
		Size: 40.5 KB (40504 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:532d0e4ac28b0d9989b4fdc09a7b481b24016f17f5ed6209609ff096ed2ca5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185445102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3dce92934e2d47f178fc70b6a57b0deaaa6c1aef1f40560f1181b93b1018c7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
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
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=5.1.6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fa082cf274421d4c78de9388c1d638ea51a72957cb0c9671c02d801d001eeb`  
		Last Modified: Tue, 14 Jan 2025 23:50:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c997244e9ca707fd716b6e30bbd6b57d9dec0488f8a904b2e29ad6b28e484`  
		Last Modified: Wed, 05 Feb 2025 05:41:59 GMT  
		Size: 31.4 MB (31377180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755be58ce8a86ec74428e764d3058fc7d233e4a9abecc2c2f2ba95e1a27372bc`  
		Last Modified: Thu, 06 Feb 2025 05:42:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a316b58eb70eb03615f53c2257cde5ae35603df17e0137d322390a804d5405c`  
		Last Modified: Wed, 05 Feb 2025 11:12:26 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3ebaabc06e598cec07a087ad60f803f68cebdbdcabcfbd570389c0c48fe850`  
		Last Modified: Wed, 05 Feb 2025 11:12:28 GMT  
		Size: 73.7 MB (73674228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdd3078027a9215bc30eee5a2fe7ddd97eacee7b2d5e1f6e241ffeda5aa8c58`  
		Last Modified: Wed, 05 Feb 2025 11:12:26 GMT  
		Size: 1.1 MB (1086997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfff4cd9d8971a45e4b6192ae53d5d2e7f74c008d128bf942cd5138491c3fa8`  
		Last Modified: Wed, 05 Feb 2025 11:12:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01932b563ce33532adb1c82f55bd57f9bad032db7ac0eaad57f6efbcb59ddc8d`  
		Last Modified: Wed, 05 Feb 2025 11:12:27 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cb005786b23fae1bd3de82635daa59d9af8bc552d0db649c4528aa1f23255c`  
		Last Modified: Wed, 05 Feb 2025 11:12:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e56a5a22c4afaeb68db3dfecf2b30da30494163340349d61166f067c68a8695`  
		Last Modified: Wed, 05 Feb 2025 11:12:28 GMT  
		Size: 3.2 MB (3244098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1219ff4f1cc7bd23f78529a474d458d75b3aaf3d05bf5d627fa821d4c035f4`  
		Last Modified: Wed, 05 Feb 2025 11:12:31 GMT  
		Size: 72.5 MB (72485007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd70ad98f811784d6d79d9aac8fb1fb4d2b858bc1eee9ad402ebf20841476ea`  
		Last Modified: Wed, 05 Feb 2025 11:12:28 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:1f6f2fd43cb4eb2c7b59c91f5137f1c174b3dc65fa356465cc45c360c0de33ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8857769c27f0f25dccbce5f093f49ac79766bde178934a5fd96c1741ccc67831`

```dockerfile
```

-	Layers:
	-	`sha256:019d5ebb345443ae1f1f89e852af71fc56a84aca019061f4951494bc6059aa85`  
		Last Modified: Fri, 14 Feb 2025 23:49:30 GMT  
		Size: 40.6 KB (40627 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:03916518422ad79420c2efb05e34f1be60299c5790a043c77621708f082345bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182297996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846dac155f7414bce2cad15953b2c0fa6c1889ec7b22c3f6ee1cec2d02531a4f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
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
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=5.1.6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f58c5f1e872ea5fb6d2093f25dc7e3e4e42116a78691c8d841fa04894fccb8`  
		Last Modified: Tue, 14 Jan 2025 20:50:15 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d3723aa6ba788e57cfc3bde16e2862d7f56e03d2a27b3b37190c75808e6330`  
		Last Modified: Wed, 05 Feb 2025 06:07:58 GMT  
		Size: 29.8 MB (29789200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7904f3c44bd281ca3d58abf1846a3b56502c132dc1c5038d20f9cfec5dc07c3`  
		Last Modified: Wed, 05 Feb 2025 10:10:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1209a58a439770b3a4119a0e970ecf91b253c6629aed9295432b834d60768b97`  
		Last Modified: Wed, 05 Feb 2025 08:50:46 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0aceff9e7a02ae2a0a3c1552aefeeca64680a94a9a00376c3e7d68a0aad6c1`  
		Last Modified: Wed, 05 Feb 2025 08:50:56 GMT  
		Size: 70.8 MB (70761780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5a9a650928db7f51748c96cbec0a1652364e7164e1ded60d93a15ffa9e4e1f`  
		Last Modified: Wed, 05 Feb 2025 08:50:46 GMT  
		Size: 1.1 MB (1136721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2f2a8593c93530ec051e05c7dd6f447e9df8c375a60de54ac2d8b53aca9771`  
		Last Modified: Wed, 05 Feb 2025 08:50:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bcd02e00cee6c3425fdbeb10f0d68429c2dde5e80fa0dcd2749457846c1b1b`  
		Last Modified: Wed, 05 Feb 2025 08:50:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccd98d4318c0f5d87e63880389b5b885e9b047a443493495cf2780e72509f73`  
		Last Modified: Wed, 05 Feb 2025 08:50:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82967b07e51f23c212284776b7fbcdf15db2c03f15db6ba0d89ca68bcc8e35e`  
		Last Modified: Wed, 05 Feb 2025 08:50:48 GMT  
		Size: 3.2 MB (3244104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b60b709ff098a96aa905de0708839bd796baf1fe3cb4e14be0d563cdd67696`  
		Last Modified: Wed, 05 Feb 2025 08:50:58 GMT  
		Size: 74.0 MB (74011942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65b52b499e9dcee51a5ab58dba2407e36cb1274995ba494a27b40cd2b4f3ace`  
		Last Modified: Wed, 05 Feb 2025 08:50:48 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:581dce8610c3b2fa6ad430af3335e08bbfaea5a9b4eec79f68679a9980b6b884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b259cc6325ec264ce5240aca35852e31fd24d72f78c4cb0712bc3ee27a21e10`

```dockerfile
```

-	Layers:
	-	`sha256:08ef5ddaea35eb5ef9aa72544b555045c891e627b891b51e3f44076d8a0491bf`  
		Last Modified: Fri, 14 Feb 2025 23:49:31 GMT  
		Size: 40.6 KB (40627 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:a2415bbc064bca7ed672c2d9155ebf0093a3acb7ef496172d4611637e67c1b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183542093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e706dedee7108bb736f17ed954edc3dee45db55a38cf616f325541ff45901b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.2.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=fc159b0d4a8ce412948fb69e61493839a0b3e1d5c919180f27036f1c948cfbe2
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 31 Jan 2025 19:49:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
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
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=5.1.6
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715918f0e770587d15212ec4d7b5b9eeb1c07e9bf7a302047dd6fe58fe3efb9`  
		Last Modified: Wed, 15 Jan 2025 05:41:15 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31467d9aa24f80ab999c6b64c04b5ffe53d39c5ede8283bb00a2bcd6613795d3`  
		Last Modified: Thu, 06 Feb 2025 05:42:23 GMT  
		Size: 31.2 MB (31230750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cae8c14a5df9e046baabf29a594c646a6e6852431f3658d57f38aafa766095`  
		Last Modified: Thu, 06 Feb 2025 05:42:22 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e5f5347b8b8c58f7962e80abc71b94cfdb4871ee8f820e1aa739546e3c93a1`  
		Last Modified: Wed, 05 Feb 2025 09:43:53 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f350f5aad007ad6eeb0d2063041d7a68192e2b1d9c09204d03450d014cf62b1`  
		Last Modified: Wed, 05 Feb 2025 09:43:55 GMT  
		Size: 72.7 MB (72687063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9011e18a647e1c22063d0445894d0187fdd406c27673a256438ffe8fb2c5b520`  
		Last Modified: Wed, 05 Feb 2025 09:43:53 GMT  
		Size: 1.1 MB (1131710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8b6341de65bf95863f0308e2debf009e501a4aa73bfc50dbdbcf19f8370be2`  
		Last Modified: Wed, 05 Feb 2025 09:43:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8341cf04ca573363a761cdaf60bc84b191fe3d5b473648395b9fe40b575901`  
		Last Modified: Wed, 05 Feb 2025 09:43:54 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4790d441bfd7727f526faf274832b2af0edf0d7934727d5d6bba9ba1b53b6f`  
		Last Modified: Wed, 05 Feb 2025 09:43:54 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84230023b7b7acf806de355b44c8f2151ec6612abf6947ab6af809d6c0a276e4`  
		Last Modified: Wed, 05 Feb 2025 09:43:55 GMT  
		Size: 3.2 MB (3244082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55b551d525addccba11eec3c89af81d6c27fb6aa64c9bc849ded865f9b944e8`  
		Last Modified: Wed, 05 Feb 2025 09:43:56 GMT  
		Size: 71.8 MB (71777631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5478c47eb3a51f81094bc3da47c3825392e8aa34e191f299cf581f464046996`  
		Last Modified: Wed, 05 Feb 2025 09:43:55 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:8096e4b640489afb36b9c92f9efeae27bcdb241b35362e6434b56bc079bf8dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b72a004fd50c83b57271fdffa7cdc2177ed13e688b62a6e8e3f44e8f2375eb1`

```dockerfile
```

-	Layers:
	-	`sha256:1e5acd156c03ee472d6fc6645cedef6a136f336be96ff7902119e9d6d02a5cc6`  
		Last Modified: Fri, 14 Feb 2025 23:49:32 GMT  
		Size: 40.6 KB (40557 bytes)  
		MIME: application/vnd.in-toto+json
