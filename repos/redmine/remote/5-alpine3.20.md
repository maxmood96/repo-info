## `redmine:5-alpine3.20`

```console
$ docker pull redmine@sha256:b72d929783deedff97bcd30123b26c7a2818db473d648a0f5ca63db245f7fcae
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
$ docker pull redmine@sha256:a412544338e94070b1138d2b9c3f4004ae20243190516a4461b1fdf43ae58ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186930286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9293898bd0fdc3d56a0b8f1330061e43d89ccb2d04068ceccae0ecaea5e4cf45`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
CMD ["irb"]
# Wed, 29 Jan 2025 09:26:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_ENV=production
# Wed, 29 Jan 2025 09:26:20 GMT
WORKDIR /usr/src/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
ENV HOME=/home/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_VERSION=5.1.6
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 Jan 2025 09:26:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Jan 2025 09:26:20 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 Jan 2025 09:26:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a890c4bbb4b44a2f3a58eb50e69f7e9d794f57d82a68467ae8b17be6327d9`  
		Last Modified: Wed, 15 Jan 2025 18:07:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76439907d51993d1920b09bfa6a2faba286d4b0cfd9797317070d3bf34671ef7`  
		Last Modified: Wed, 15 Jan 2025 18:07:21 GMT  
		Size: 39.5 MB (39495108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fbc15a476e84da1ccc7a9a80610b8852484e805f055e1dc9721059c91e15bb`  
		Last Modified: Wed, 15 Jan 2025 18:07:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c386f8aa9c88efecf633322a6585d955c70fc22c7eeadb0d7701a4ffdd702b`  
		Last Modified: Wed, 29 Jan 2025 23:28:50 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d14df99d0ab895dc644e39ebe9f094a407b0f2e2451b1bce91565b36c154e`  
		Last Modified: Wed, 29 Jan 2025 23:28:51 GMT  
		Size: 68.9 MB (68850996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23335bb0f8541d2d6c3250b758a9192e26c2dfa01f40893b3e595ca6c10ab59`  
		Last Modified: Wed, 29 Jan 2025 23:28:50 GMT  
		Size: 1.2 MB (1195499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d515f0a127c3c1d4ed015be870f6c0ef8fee5e4a10b924ef90a88e0777cbc311`  
		Last Modified: Wed, 29 Jan 2025 23:28:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4a36d682ebe66348dfd866cfce3adc4a3edfadb15ff1efaf3badb320039b9f`  
		Last Modified: Wed, 29 Jan 2025 23:28:51 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82aa3b54ace2b69b8252232ce11a9f949975f9dce7391b5cd02a10dbe042816`  
		Last Modified: Wed, 29 Jan 2025 23:28:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c62c90c19db65615a4b0bc792a7aabe2b7668f3a6e62e4fe17dff90d012838`  
		Last Modified: Wed, 29 Jan 2025 23:28:51 GMT  
		Size: 3.2 MB (3243730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fb57dd317284cac038ffab8a6e15b4dda0b7954932ecbf8385c832951f43c9`  
		Last Modified: Wed, 29 Jan 2025 23:28:53 GMT  
		Size: 70.5 MB (70514702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723dacb00f3023a09840f9054435d9f8dbaf8af8e4bd739203051259ffb22a1b`  
		Last Modified: Wed, 29 Jan 2025 23:28:52 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:cf6ff5ccf16569ede42a7ec84ad5a41eb65b8ae81f75d948316eaeb653352ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 KB (39435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1eaa4c5f268795b8892bfcf0d3f80b312cea4060b349787a77655b7ad3a1f3`

```dockerfile
```

-	Layers:
	-	`sha256:59f8b58c4e2a9331c4955d4944216cb5463f65eabb0a106bf2592ad846fd150d`  
		Last Modified: Wed, 29 Jan 2025 23:28:50 GMT  
		Size: 39.4 KB (39435 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:48b835597e0a6c845c2fe8579ec0d03e10de72a81da348a3eb6861138029f503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179102034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47937e82123e12f0886e52dde50618530b2227b68535e168109aed6f3d438676`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
CMD ["irb"]
# Wed, 29 Jan 2025 09:26:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_ENV=production
# Wed, 29 Jan 2025 09:26:20 GMT
WORKDIR /usr/src/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
ENV HOME=/home/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_VERSION=5.1.6
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 Jan 2025 09:26:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Jan 2025 09:26:20 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 Jan 2025 09:26:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646063a45551a61d3aff631507ce28db6d552b256afec6162f53389af67e600a`  
		Last Modified: Tue, 14 Jan 2025 01:42:24 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b1424ae6ea4e7a5973cbae3f1be8dc1f2992a40be1429c9b1b63f4c0a1d73b`  
		Last Modified: Wed, 15 Jan 2025 18:16:12 GMT  
		Size: 35.8 MB (35777812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ed9ffdc7d7e38a7ef75bcd29a753161ae9df112685b1b4036df4141a04314e`  
		Last Modified: Wed, 15 Jan 2025 18:16:10 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6b2da79a82b8937570a507607e3b434f6777364359b438b863d843313eaedb`  
		Last Modified: Thu, 23 Jan 2025 01:56:37 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe788f966d05f3fb39dbcdf97a523cb39039a70deb459fc60806464fe63b884`  
		Last Modified: Thu, 23 Jan 2025 01:56:40 GMT  
		Size: 65.7 MB (65677755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4380c732734448b8c648e51b51374f01c51779ab34e4de791c30e45565dcfe7f`  
		Last Modified: Thu, 23 Jan 2025 01:56:38 GMT  
		Size: 1.2 MB (1162232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9af285d55b52191f0bc9f7a4907500fadb301db3e43d4de8b11a0597c774d6`  
		Last Modified: Thu, 23 Jan 2025 01:56:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc8807381fd90ba76bc884e2031c219b734947710b243ced83e3c9b310f7d52`  
		Last Modified: Thu, 23 Jan 2025 01:56:38 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b62133e057f27d3df4ec2a013ba65677e000cdd88dcc49ecbe6e976ba6a7c5`  
		Last Modified: Thu, 23 Jan 2025 01:56:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f537e6a710516d73ad2e6bd629db4cce9ab76f048218b7a1d402de55eed1a`  
		Last Modified: Wed, 29 Jan 2025 23:41:51 GMT  
		Size: 3.2 MB (3243779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974a39910e3cbc1ff0ddffe3f3b6783bc4ca0bbe2b7fddde23a3fd5b8021f6bb`  
		Last Modified: Wed, 29 Jan 2025 23:41:53 GMT  
		Size: 69.9 MB (69864992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd94ef82665839ce16a7a7a3cbb890a835c2fa4095cf8509ff4df00246023b`  
		Last Modified: Wed, 29 Jan 2025 23:41:51 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:59d565266a1098eaafd3b8fc56d29d06819ccfc5f156fa4b714396f9f7cf5d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8251c797608ef935ab6e3a344c51f1af2e48b985a54d6fb3390997213ee62e`

```dockerfile
```

-	Layers:
	-	`sha256:5b3615e111376a59ec99056d54330f300894f3c8a91a26b241763ad67529dade`  
		Last Modified: Wed, 29 Jan 2025 23:41:50 GMT  
		Size: 39.6 KB (39581 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:cf452d4861e17f0ae5b94cd7c4b913e5a5d6f23ccccba2f71cee056afb095756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174930166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4961aa61845169f59b39e34b8e6a78c2a318a22fb2dd2a36cb2863bb98e6db5f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
CMD ["irb"]
# Wed, 29 Jan 2025 09:26:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_ENV=production
# Wed, 29 Jan 2025 09:26:20 GMT
WORKDIR /usr/src/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
ENV HOME=/home/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_VERSION=5.1.6
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 Jan 2025 09:26:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Jan 2025 09:26:20 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 Jan 2025 09:26:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04cd14ba7406c54223a25e09ff76f4ed50955d6c12ebda81a014cf1bcb3461`  
		Last Modified: Tue, 14 Jan 2025 01:47:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28142150a9091e5abb90be0ea35abe5c67141773230a023c2e3bf52d37b6f33`  
		Last Modified: Wed, 15 Jan 2025 20:14:25 GMT  
		Size: 35.5 MB (35480749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7535114493b9ab28db885d699ccc3f600a2af485323a25f2c929eb66b38ae7e8`  
		Last Modified: Wed, 15 Jan 2025 20:14:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3c72cc38bee871076fb7e2d5447f60f3b1efa9f60931b6596dc8f8aa9ebfd5`  
		Last Modified: Wed, 29 Jan 2025 23:50:44 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1262fe7e09cf57b109f865f777e9498b4573d841f9ccc1da346de1b65e756e61`  
		Last Modified: Wed, 29 Jan 2025 23:50:47 GMT  
		Size: 63.1 MB (63083525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb345f1713ee92baf69ac4b354fd2a6898f2e6fb0c22ce794465e52e8aba940`  
		Last Modified: Wed, 29 Jan 2025 23:50:45 GMT  
		Size: 1.2 MB (1162211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8524284ca15b2cdea25cfd5753f29955393e539ab9d84be4a4ee09fdd20febf8`  
		Last Modified: Wed, 29 Jan 2025 23:50:45 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54953a7f6efd2aad94840e499c72ef0b3f52765ab3fe3da374c69c7cc90668eb`  
		Last Modified: Wed, 29 Jan 2025 23:50:45 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1141d720e5e8f61b52cd446856a34c15d4613b12746307fb61ae5c692bf0048`  
		Last Modified: Wed, 29 Jan 2025 23:50:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8748a61d4dcff5ab59d4c5519c02c8c5e9f872e969b0e757e63b7952333a6fe6`  
		Last Modified: Wed, 29 Jan 2025 23:50:46 GMT  
		Size: 3.2 MB (3243780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e8951cf8dda1e05d530b4f4dbc4e2ff7f24b20b309972adf846216d1b7f97b`  
		Last Modified: Wed, 29 Jan 2025 23:50:49 GMT  
		Size: 68.9 MB (68860404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134c74d84abf9d66285ead4b2be77baa32690546a8392792fe3a525dfc4dc0ef`  
		Last Modified: Wed, 29 Jan 2025 23:50:47 GMT  
		Size: 2.3 KB (2300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:81f03e9f6fb6b875901736883cef2562888ea1fa7a7cfaf15f9d34d350b561d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e4250e47a51cb5a9acef6a67efcdefb98139aa3783d72663f21f672b5baba8`

```dockerfile
```

-	Layers:
	-	`sha256:bd4186789389312624b7da83f595f307b942467025a024610b454e9be65d8d19`  
		Last Modified: Wed, 29 Jan 2025 23:50:44 GMT  
		Size: 39.6 KB (39581 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:57027d9a1c188badf384cb522f2b94eef61493ddb0300e3c02d111af377ab81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187948016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523c6dcd2f16eb40c0d8d703bc2ee51fe1d83e6734599279679949e569608050`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
CMD ["irb"]
# Wed, 29 Jan 2025 09:26:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_ENV=production
# Wed, 29 Jan 2025 09:26:20 GMT
WORKDIR /usr/src/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
ENV HOME=/home/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_VERSION=5.1.6
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 Jan 2025 09:26:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Jan 2025 09:26:20 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 Jan 2025 09:26:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b061e389e1cfaa1b6c20109d4c4f25f3fbc6449802a6b02e00043572ab4bceb`  
		Last Modified: Tue, 14 Jan 2025 01:45:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3971029d70d3d8ff7f62b3d043755fb0fdfaf8e841851e4c30f26b0c702b4aec`  
		Last Modified: Wed, 15 Jan 2025 19:42:08 GMT  
		Size: 39.6 MB (39553796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2433d2bccb1ec00b67e02e566fdcca84868eea09bb6bbd1d3bab8f4b9b969850`  
		Last Modified: Wed, 15 Jan 2025 19:42:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9eb6142b61e35f503955920b57cee0bafe873e96362eccb1a13bc2de6230f8`  
		Last Modified: Wed, 29 Jan 2025 23:48:25 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e53ae248663db912fff3f80bd901df7b1a8ac648c3c9907c8750de8f113e9d`  
		Last Modified: Wed, 29 Jan 2025 23:48:28 GMT  
		Size: 69.3 MB (69336295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b54610db50b4cdafa8821371d431a81771413e8db4dc849359131c3450805f7`  
		Last Modified: Wed, 29 Jan 2025 23:48:26 GMT  
		Size: 1.1 MB (1121235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017fe9eddc92737927aeb85e7d39a0f0000c210561566679e9735f9c45621826`  
		Last Modified: Wed, 29 Jan 2025 23:48:26 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd58ee0f574d2f69126f7e2ce7104e2c8c4308af779824dd0e6676fd5a15498a`  
		Last Modified: Wed, 29 Jan 2025 23:48:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46911b2ba492577cad171b64c3d31d03bff8d5795b666c3b2d76c282eb65de1`  
		Last Modified: Wed, 29 Jan 2025 23:48:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8156eaeec16f78cabfdf979a13c6405521487344f648c6ac8ae20b40b1a5c212`  
		Last Modified: Wed, 29 Jan 2025 23:48:27 GMT  
		Size: 3.2 MB (3243785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85b35cef5c7039e24eea1a27a0c875cf911a8a025ab833c215720ccec89e8d2`  
		Last Modified: Wed, 29 Jan 2025 23:48:30 GMT  
		Size: 70.6 MB (70598146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecc4a51e8f04cc9b21beea922afdc894cf0fedbf6355f9f2dbd8223e8e6bb3b`  
		Last Modified: Wed, 29 Jan 2025 23:48:28 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:276db127cfe97503c13f36743eda152b31bb743d8fec70e38ead42fda48fda89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82682abe5e3181ef08945a3a83cc0bebff53fb1ca98e4972978320197ea77cb`

```dockerfile
```

-	Layers:
	-	`sha256:c93f31004829f3480c3248678bbe6bf57945e2597c56fc905b0619eaba1b74c9`  
		Last Modified: Wed, 29 Jan 2025 23:48:25 GMT  
		Size: 39.6 KB (39617 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:e91242e55597d47b1a0b8ccf65155cd0f717660bc350b0567adfb3d874893838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183838077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde76a8a032643bce8d2b667f7d59dd99c4cf5550fd7fc09ae2f00cb8115a68d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
CMD ["irb"]
# Wed, 29 Jan 2025 09:26:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_ENV=production
# Wed, 29 Jan 2025 09:26:20 GMT
WORKDIR /usr/src/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
ENV HOME=/home/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_VERSION=5.1.6
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 Jan 2025 09:26:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Jan 2025 09:26:20 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 Jan 2025 09:26:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f17e9214635b0501a02171976acb1384115f219e06f7afdf8833ab2f417bdc`  
		Last Modified: Wed, 15 Jan 2025 18:04:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d068f0228421ee6e63b1d0cb0dc5902cf8934b2a11c8b6ddd9c285356d85299`  
		Last Modified: Wed, 15 Jan 2025 18:04:43 GMT  
		Size: 35.9 MB (35856720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192f373652bfae00c8222ea28d23194cda56ea70f13681c649ce189f368d74be`  
		Last Modified: Wed, 15 Jan 2025 18:04:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080db37e236e7ed1b4fa783b041fc00e10aeb6795ad0f0d2065c569b77132d6b`  
		Last Modified: Wed, 29 Jan 2025 23:29:00 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cad128126c338873372bb6b920eb2331f8bd33c5a0751de72348ddfe45c2faf`  
		Last Modified: Wed, 29 Jan 2025 23:29:02 GMT  
		Size: 69.4 MB (69424727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb041544ba409b3c0279e6071c72fbfc492376f305a9f2094b3e6082307496d`  
		Last Modified: Wed, 29 Jan 2025 23:29:00 GMT  
		Size: 1.2 MB (1170685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03982094cd41e95f02cc40f0eb746fce75477ddde4f0751bef1ae9827ac3069`  
		Last Modified: Wed, 29 Jan 2025 23:29:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96d2dd2473dabd9a48238efe5a47101838d9c72ce4f970d728e0df9724cb6af`  
		Last Modified: Wed, 29 Jan 2025 23:29:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db9d23b172376a73b4ca990623a5c64a74c60d1b14ac9d7cd6ec485aa667ac4`  
		Last Modified: Wed, 29 Jan 2025 23:29:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d272c8785d12bff23821ece0ac405d873ba23721d80e0cdbdab03604d32504`  
		Last Modified: Wed, 29 Jan 2025 23:29:01 GMT  
		Size: 3.2 MB (3243762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb7a64a9ce977902a3c8bbd8cbd5f723745fee7d6477dd68c8b7b6d3b235988`  
		Last Modified: Wed, 29 Jan 2025 23:29:03 GMT  
		Size: 70.7 MB (70667225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723dacb00f3023a09840f9054435d9f8dbaf8af8e4bd739203051259ffb22a1b`  
		Last Modified: Wed, 29 Jan 2025 23:28:52 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:581f5588a4f71ed3eda6d83d161f4649c3792a32dcd7b01ff6e3a7ecbf234451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 KB (39395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d9954263a629ab568e0f63a5bc4e159fcd5f5f7aaeb5feab1978b8126d2946`

```dockerfile
```

-	Layers:
	-	`sha256:3c0b1c36f686adfa99fd3a85658bd65cb9ee10169d97c04452528d41984c4c8c`  
		Last Modified: Wed, 29 Jan 2025 23:28:59 GMT  
		Size: 39.4 KB (39395 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:aba2f464130f8d67f0c76848b3b21c4113254a00078d83cc784f24dfcfe9c9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188193059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8f82117991f81536c96dd346ebe5b84862f53c06d76b8e87193ea7e82db829`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
CMD ["irb"]
# Wed, 29 Jan 2025 09:26:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_ENV=production
# Wed, 29 Jan 2025 09:26:20 GMT
WORKDIR /usr/src/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
ENV HOME=/home/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_VERSION=5.1.6
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 Jan 2025 09:26:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Jan 2025 09:26:20 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 Jan 2025 09:26:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd611afdfde6a92b771a8c2f4dd7b096a1311acfb8646e981977bf38912787b`  
		Last Modified: Tue, 14 Jan 2025 01:48:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bfe86d15813b0c60f1ca511fc56ee02abf50e170138311d0b9c104626e68f1`  
		Last Modified: Wed, 15 Jan 2025 19:09:19 GMT  
		Size: 37.4 MB (37390520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70da6783e184c111f39431725de46ff2da76f565b9f1149e0f73b31cfc69bf2`  
		Last Modified: Wed, 15 Jan 2025 19:09:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1817c6f23e4914326b402017c4fe0ab16324fdaf93135c337b551bb6edc8958b`  
		Last Modified: Wed, 29 Jan 2025 23:59:36 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb17a936be950c19039cae8e30fdc7b00922ddc334fa64d16c740d8328a229e4`  
		Last Modified: Wed, 29 Jan 2025 23:59:45 GMT  
		Size: 70.4 MB (70429161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab99f55d363577a4411136ce38cdc9957241d3f107563b31f7e6878fcb28957`  
		Last Modified: Wed, 29 Jan 2025 23:59:37 GMT  
		Size: 1.1 MB (1111728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64e4fb3598ef404dac6a9a8dc0ade20889f85a19f6f93607cf304c71523beee`  
		Last Modified: Wed, 29 Jan 2025 23:59:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22672bbe9076a73e260d43a526d8a215d484fac69b9d77ed29b9fe46fc78fce1`  
		Last Modified: Wed, 29 Jan 2025 23:59:36 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199d3966191baa06e441dbc2290db3b776df466d6e300d62af8428e2197cfb1`  
		Last Modified: Wed, 29 Jan 2025 23:59:37 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d73941422e030be7e7ae3b96afc5dad05b40fe3c3f917378cc38cca8c10518`  
		Last Modified: Wed, 29 Jan 2025 23:59:38 GMT  
		Size: 3.2 MB (3243872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d325526eae98a252882454a16b0ce25be5c33ade24e40de379a49647c332fc`  
		Last Modified: Wed, 29 Jan 2025 23:59:46 GMT  
		Size: 72.4 MB (72439386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0153ae77bcac7c5e151de8443e9c79e063bf949ef49407d18c55c9b9f814ffcb`  
		Last Modified: Wed, 29 Jan 2025 23:59:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:3b3464c7d93c7049efb4c53173961ba03a708adbaef867b7cddacc4ee943d72b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 KB (39485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4883806ff4a040fec60c38652d84f71e82605d1228ec45b3606e2b1eb15ad93e`

```dockerfile
```

-	Layers:
	-	`sha256:03f0699278b392f7109273f1505d4c71261218f1b8450489accb2900d5ae66bd`  
		Last Modified: Wed, 29 Jan 2025 23:59:35 GMT  
		Size: 39.5 KB (39485 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:7235e1cd4a0f514ecd3d9f4ee6b93e497d2c6162f27d8176d925578ffc369266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186864639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be817b560f03a236e8706dbf16bf152066dfde77640f50bfbb26e8e313bd720d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
CMD ["irb"]
# Wed, 29 Jan 2025 09:26:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_ENV=production
# Wed, 29 Jan 2025 09:26:20 GMT
WORKDIR /usr/src/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
ENV HOME=/home/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_VERSION=5.1.6
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 Jan 2025 09:26:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Jan 2025 09:26:20 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 Jan 2025 09:26:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb69847f873261cc901364c6e5453bc8ac36796ac8944ffe1685a0c21d2a1f0`  
		Last Modified: Tue, 14 Jan 2025 06:01:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57765333e2113c733946ad6a449c71d87cc75fb63b4f5f97450efeca74472c07`  
		Last Modified: Thu, 16 Jan 2025 03:01:19 GMT  
		Size: 36.0 MB (35965721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c24e48595308ae0e7d147bd1385fae58f5f9d57598cb1731a6c985605f6bc2c`  
		Last Modified: Thu, 16 Jan 2025 03:01:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8541c5efbee2ce4698a19c199c186ec4f79226479d310ebfa157a7962a094a2`  
		Last Modified: Thu, 30 Jan 2025 04:20:59 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464632543942b66eb41c873313be058a5900b4e6a8b29aacb5e72f89149ad3a0`  
		Last Modified: Thu, 30 Jan 2025 04:21:10 GMT  
		Size: 69.2 MB (69166172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ca69a0d2917341fe25199da382f7049f24cd3e684178b4729a2d4f2eb98952`  
		Last Modified: Thu, 30 Jan 2025 04:21:00 GMT  
		Size: 1.2 MB (1163799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8cc35a06d6f6b97336f297c11d80e4b4231d8075f3a1cd4812baab53a36760`  
		Last Modified: Thu, 30 Jan 2025 04:20:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d95c90ea1230c4b7c09f1c56d0d34153fb575f7b55ccc37e2db5475a91f6d`  
		Last Modified: Thu, 30 Jan 2025 04:21:00 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c368ef2b4622422d84a5c396f06d72e677f22d89caf95141c37d9199ba52bf4f`  
		Last Modified: Thu, 30 Jan 2025 04:21:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fc986f9ca8f78a7f1299fc87388da1eca6da3ef47dfba1c4d7ce480078b9fc`  
		Last Modified: Thu, 30 Jan 2025 04:21:02 GMT  
		Size: 3.2 MB (3243826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe2ed3b6b39863b73fb5668ce4fec4185c16e2e50daea47cf809659777aff81`  
		Last Modified: Thu, 30 Jan 2025 04:21:12 GMT  
		Size: 73.9 MB (73949206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255374d3f0ad730f40557370ea6481747fb09a11dce563bf96cea75525c03b6`  
		Last Modified: Thu, 30 Jan 2025 04:21:01 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:d0f6e4353b58aba4433b0707dbe33b538b0052f673850449df2747a71b8ad253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 KB (39485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e5f136910eb875e0ffa1e8683bbc112beee4ba1f9e730add84c87c975500d2`

```dockerfile
```

-	Layers:
	-	`sha256:273049e9776e832068c93774e894d5f69a65330830950cb7b61dba86558aa2bc`  
		Last Modified: Thu, 30 Jan 2025 04:20:59 GMT  
		Size: 39.5 KB (39485 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:2e624bbcdcf281e14629aad45a3da2aa6b78c0018973533da24432096fe97fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187501780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e3f2ea491fd99fc0ccc4c03d426044b20a7de0ad68366789a26562f19cab75`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_VERSION=3.2.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 14 Jan 2025 19:28:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 14 Jan 2025 19:28:22 GMT
CMD ["irb"]
# Wed, 29 Jan 2025 09:26:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_ENV=production
# Wed, 29 Jan 2025 09:26:20 GMT
WORKDIR /usr/src/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
ENV HOME=/home/redmine
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_VERSION=5.1.6
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.6.tar.gz
# Wed, 29 Jan 2025 09:26:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=d73584e74d692aa94644799d986df4e846fb59a43205c16bd857ed56cf0abed9
# Wed, 29 Jan 2025 09:26:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 Jan 2025 09:26:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 Jan 2025 09:26:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 Jan 2025 09:26:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 Jan 2025 09:26:20 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 Jan 2025 09:26:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27470f160962be7e0327882668c9f8725389d49d37e462a3fd04f6b968da5e0`  
		Last Modified: Tue, 14 Jan 2025 01:47:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4df1aa7bd30fed7e9b6586bc54cb71b19b917086dd400e855814722cd81e39`  
		Last Modified: Wed, 15 Jan 2025 19:01:22 GMT  
		Size: 37.4 MB (37417743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567e37351ce3140d335f5c8d0b86e4271b9f650d9e863668574c37ae434cdb3c`  
		Last Modified: Wed, 15 Jan 2025 19:01:21 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8686183c7eaaeb4b4fcbb09b19ff7750ab65b3cbb9b8d746b4b12e3a21819876`  
		Last Modified: Wed, 29 Jan 2025 23:59:46 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa05b2cbeb55c03abe3cef57999ac2502d63439e441c25eed13567b977aa43`  
		Last Modified: Wed, 29 Jan 2025 23:59:48 GMT  
		Size: 70.5 MB (70515227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e376f0b211600ea5aa5907ffdaf2855b654e28c06028ecc759345c4e25945cc9`  
		Last Modified: Wed, 29 Jan 2025 23:59:47 GMT  
		Size: 1.2 MB (1160438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b178a19ce12c75c0481d9c9443bc0c8e00acbde88c7de8163d9002a2aebcf58c`  
		Last Modified: Wed, 29 Jan 2025 23:59:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53413a62c1c7c11f8bac112ef3d8c367532256b4882110e7746b731b405e187`  
		Last Modified: Wed, 29 Jan 2025 23:59:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069b7d46015f30eb86b7b5920e61fb8485ea3e383d0730bdb80bd7bc11258a01`  
		Last Modified: Wed, 29 Jan 2025 23:59:47 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdce6b7352920eab4a7bf20b52dbf9dbcf57cc49502335d6f2f3709f3f8822cc`  
		Last Modified: Wed, 29 Jan 2025 23:59:48 GMT  
		Size: 3.2 MB (3243752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b3072bc98dcff9dcf668a5eaf49d927e25713ab50812a69b609125c1d658eb`  
		Last Modified: Wed, 29 Jan 2025 23:59:49 GMT  
		Size: 71.7 MB (71697309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cfc7efb65100f92317bb36af78c290c8748e32236e97448f01ad47f95142af`  
		Last Modified: Wed, 29 Jan 2025 23:59:48 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:c7b54f2e90bad2e711f04012e8d43e6b8b218be3ffd47cd1a0bc2be23431ced5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 KB (39435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118ae8f97edf951fc5085f8a8b55caf6dbf47defa8ed95575b9fa89932639760`

```dockerfile
```

-	Layers:
	-	`sha256:3a8c55b7d0cf6a5c3ffee0212c8470908239b82330954bb6496a1cd8e15568bf`  
		Last Modified: Wed, 29 Jan 2025 23:59:46 GMT  
		Size: 39.4 KB (39435 bytes)  
		MIME: application/vnd.in-toto+json
