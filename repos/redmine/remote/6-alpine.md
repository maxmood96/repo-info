## `redmine:6-alpine`

```console
$ docker pull redmine@sha256:4005ee0b1ac15d51790bdb614ea6a0c18e605ddfd62af468185e5762cc41f383
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
$ docker pull redmine@sha256:55362ea5bc41f508002274e2aa63a86e3de2e8793367c2159fadc8bd73fbf56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195451964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f64f212119305880fd8ef67e63afd35d61465a3594adac4c138ce05389994c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22100f21be3b64da427f67a2320e4244b54f9374ac48cd9e7936b29f04929da`  
		Last Modified: Thu, 12 Dec 2024 22:35:07 GMT  
		Size: 6.7 MB (6741331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e8e484c0c03f043fffca19de7041e86a95c66839bb6916c886b73a7e9fdfea`  
		Last Modified: Thu, 12 Dec 2024 22:34:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c629587a50a6c1cdd41b82131fe7c42f116871d148113ed44aec0816150df0b`  
		Last Modified: Thu, 12 Dec 2024 22:35:07 GMT  
		Size: 35.3 MB (35311599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce64bf084d5c96f006869253dc4efa25e74837017db957ac22c945ad033b05a`  
		Last Modified: Thu, 12 Dec 2024 22:35:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98d582107f6859a844631e961b2120051484267568dbcb0dac709c069e7344e`  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb240e0817b54cf371ae140b39bf0149b74ade5942c2d5599b37ac988b6c8000`  
		Last Modified: Tue, 17 Dec 2024 19:31:36 GMT  
		Size: 70.8 MB (70841040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50556332fcb9be7c65b4de4e865cd2b6c9d56824e1086bda774e222a77cfe85f`  
		Last Modified: Tue, 17 Dec 2024 19:31:35 GMT  
		Size: 1.2 MB (1197844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3200be7faac4783efaee21a664f27bba81d67acfa6b106f5dfab1d514afb480`  
		Last Modified: Tue, 17 Dec 2024 19:31:35 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbafe43b5954b498a4f86ad5a2c98d05771fadfe80f67475533d8c0f9b5c10ac`  
		Last Modified: Tue, 17 Dec 2024 19:31:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd9e0f36ed26a7492c6a773c1cef48f062d51114bc88f6162801d61d55cb81f`  
		Last Modified: Tue, 17 Dec 2024 19:31:36 GMT  
		Size: 4.1 MB (4060065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b0d2752df27a676e920219a5a73d162f41925892575495af146cc9169ff2e1`  
		Last Modified: Tue, 17 Dec 2024 19:31:36 GMT  
		Size: 73.7 MB (73652165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa47ec9d2d5aaa2961928519eb6937dbad1aecd6f70dd939718410ca9222a77b`  
		Last Modified: Tue, 17 Dec 2024 19:31:36 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:6a6387686fac5426907a37e4d8d1c0c55b06457d5c5a75a191c61723841822cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277d42f0f42eb870439bbbe9ef2daaaa4fde777e30d14ac5ab3176e052037ea9`

```dockerfile
```

-	Layers:
	-	`sha256:06642e3ecab39d71c294435d158f196e4789a8c420baf92ba0a0f9b62f6d8b34`  
		Last Modified: Tue, 17 Dec 2024 19:31:34 GMT  
		Size: 39.8 KB (39847 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:21b29200d4348e2e35fbc0fe4f6ff7e54bdf54db75d22ecb02d8ba3590e71b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187189881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d09e1eebcb25dc37ff5d3da93437fc5a0f64bf533f32da5ab823f257484a21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b12c95f1fe69503a4e99b4118a13b41c40d0844feba72e2e756a769be5fa7`  
		Last Modified: Fri, 06 Dec 2024 22:32:43 GMT  
		Size: 6.6 MB (6568172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ca0d2bb66a7dcb23798d7aa23885d8544420f7868a1046f3f039325e9bbe07`  
		Last Modified: Thu, 12 Dec 2024 22:38:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28fbdf9c6aa2e61e0897f6e09a3031cdb361ef949585d6c88a24b70b8a158ed`  
		Last Modified: Thu, 12 Dec 2024 22:44:55 GMT  
		Size: 31.7 MB (31650253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146965d9a90634afaf43d0565f581b102ca823703f2fa923b13457eb5d2344df`  
		Last Modified: Thu, 12 Dec 2024 22:44:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f93bcffef1883776512b92ec0d9aa35cd0aed667adbdc270ca6b6db7ec78dc`  
		Last Modified: Tue, 17 Dec 2024 19:33:18 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b848a75706a564e2ccad56d6bea490d7685338f1c4035c7ad59bdd0fdef157`  
		Last Modified: Tue, 17 Dec 2024 19:33:21 GMT  
		Size: 67.5 MB (67538734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb90b9b5a989095877430e41df0c44566df1711d21edd044be7f6dd14a6c724`  
		Last Modified: Tue, 17 Dec 2024 19:33:19 GMT  
		Size: 1.2 MB (1163952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27f2fd2046c32b1e49005e63663b828237f9e3b4cdf1b649952fa87962fa631`  
		Last Modified: Tue, 17 Dec 2024 19:33:18 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99af07b0a9b9d0ac496ca86e17a3e8c818a0abb2d514c3c4486d24464688200`  
		Last Modified: Tue, 17 Dec 2024 19:33:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87165ebe5acf2b94804f9d8b11b8a07d984363ed47f36d2c04454055fd7a1a`  
		Last Modified: Tue, 17 Dec 2024 19:33:20 GMT  
		Size: 4.1 MB (4060010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908fe8a7424785facf4af80e927a3ae69a318665e321bd041862b0db4e4da5ad`  
		Last Modified: Tue, 17 Dec 2024 19:33:22 GMT  
		Size: 72.8 MB (72838096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3e4256a8c59f5ad109e9af8a6de358ea9e4d75ba6eccde0b3f521782e8a7ae`  
		Last Modified: Tue, 17 Dec 2024 19:33:20 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:b43f41be95c7e193819351ac0ae4edf7f54f05a5484a491855c24f5fb70a2c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 KB (40019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e31fa6d029344795574dc260f1cf0eee2af296876f971b0547883bc422156e`

```dockerfile
```

-	Layers:
	-	`sha256:2569f7e2e53dc45cea1597c0ad71bf33a0ee5a94af91c22bc50ca065f0b0c376`  
		Last Modified: Tue, 17 Dec 2024 19:33:18 GMT  
		Size: 40.0 KB (40019 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0cc3e7ebe995049ec2a2e0fcdf9bdabd0c63e725977081bccb5986ebb2eb853a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182950213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774d153e2b780cd55a5c717376eca097c831db63821663fd48608917df198ed7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b26c224a9a1e46e5dfbc9bf70fcad8ef517f0a3c0bcf4815427a79622b385a`  
		Last Modified: Fri, 06 Dec 2024 22:33:32 GMT  
		Size: 6.4 MB (6408987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a6cefa53cbec58b80f6c0754a11c80ccf91e1b3e090d1a5b9687f91648e830`  
		Last Modified: Thu, 12 Dec 2024 23:18:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6742d287c1a9e78818a2f19114c275f2f291c53d2619718d204bc00654b73b`  
		Last Modified: Thu, 12 Dec 2024 23:34:55 GMT  
		Size: 31.5 MB (31525888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65b2ba08c050532c36ea0ac8412fc9e901682c3e94197cf36e9bae610e21570`  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e154a9023fe1bf24c0e94c182ac41e8ea9628a58dc1dbca6a11eb0628bccd2c3`  
		Last Modified: Tue, 17 Dec 2024 19:33:37 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729e5b90fbba5d5a7712202ceb1d75da233d47ee2646c777d69cd27d883b2e41`  
		Last Modified: Tue, 17 Dec 2024 19:33:40 GMT  
		Size: 64.8 MB (64811929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351c45224a6c811f4ede354b6f1d7afe00f2fe4b28017330b50d1a1557dbcdf0`  
		Last Modified: Tue, 17 Dec 2024 19:33:38 GMT  
		Size: 1.2 MB (1163943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57b98c55cc7049a185adaa01b5994b24bdd0862dc62586e8c03a1bce0961a6`  
		Last Modified: Tue, 17 Dec 2024 19:33:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd29aebab722e3ec2cfc84eea78742d5042d813503a2de143c43879a0bd394e`  
		Last Modified: Tue, 17 Dec 2024 19:33:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9078f00ae5b3f811a1b13912e1f85357df02f95314ed01a142e8b472d2446f3b`  
		Last Modified: Tue, 17 Dec 2024 19:33:39 GMT  
		Size: 4.1 MB (4060059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e71408023952be303785361ba982ea17efec05601afba3136fa8eb427a664ce`  
		Last Modified: Tue, 17 Dec 2024 19:33:41 GMT  
		Size: 71.9 MB (71875889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd6828717b890135b960dbc311b5d8bebb448e25127b6fe80761a2f120232ec`  
		Last Modified: Tue, 17 Dec 2024 19:33:39 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:ffc354f8764ae60686af278a51c70b6ed97a53d8a84bbb34a58c5d32a3e642ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 KB (40020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc2cb41733280d00ce2d2322c376b312246160efbad34cf9c3cf81c1be3115e`

```dockerfile
```

-	Layers:
	-	`sha256:b57dd1a4a46279efd8ddf5f901e4e96a6fe617e705098a9d698f92f4d1a7e152`  
		Size: 40.0 KB (40020 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:d204c3efc584be6645b6468c6622973152d6316f1192ba8a37118db8abc12bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195476676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9204d0224bdb4f2a0dda32fbe9ddb4d4e3245f0c8c3d47f1a8d2246061c8cea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8768c1cb67d700107587f1a01b3b69ecc681b49e487dfc7a461ef242515c6c`  
		Last Modified: Thu, 12 Dec 2024 23:11:44 GMT  
		Size: 6.8 MB (6776469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375ce81c945782093cda3e7e6c9689a6849c2ef2dfe5385ab4b09180f84f6445`  
		Last Modified: Thu, 12 Dec 2024 23:11:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e1e8e137fcccb8286d1149bfe095e4a7869052fc96c54a3f65bafde57231f6`  
		Size: 35.3 MB (35349822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a790c4c967ece1d862ca876f2ca96858358c94bec624e272163e2b8715dbd8ee`  
		Last Modified: Thu, 12 Dec 2024 23:26:32 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8f3d2b4c9d39a7545c515fe4ab7b7d2a2029d663ebe9757d45acc1157bf0ad`  
		Last Modified: Tue, 17 Dec 2024 23:30:50 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f86c8c8fcbce3788dabdb23a6019e9d02d63dfb87b1f015b398e1cf9d828924`  
		Last Modified: Tue, 17 Dec 2024 23:30:52 GMT  
		Size: 70.5 MB (70542675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983ad27b5721147f89a2186b02f87adc2359bac48915151723ff06e38197cf12`  
		Last Modified: Tue, 17 Dec 2024 23:30:50 GMT  
		Size: 1.1 MB (1123952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7800124c294ca27fc4bf458e76c9decebbcc2e7f3dca4db522d3f8ba6b42dc84`  
		Last Modified: Tue, 17 Dec 2024 23:30:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0175d99272d7de2c9c32665b5aae6bc82933b5d458e56806465d2a08829b14f8`  
		Last Modified: Tue, 17 Dec 2024 23:30:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779576669308061979b193e31daf7c2bf1728dc6af941f33999bf0ba2d8838db`  
		Size: 4.1 MB (4060096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0922ca438c0bd1231929ce05557ae8b0a159b5df5e9a41060c5520c2c06017`  
		Last Modified: Tue, 17 Dec 2024 23:30:53 GMT  
		Size: 73.6 MB (73627000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2ac1784d09ddb21340884964c06b327894f207b9a5730e1d4a1da6ac13dc6`  
		Last Modified: Tue, 17 Dec 2024 23:30:52 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:08ab0ed2b3e9b497e0aff85b9e368b3178bf7e9b82eee36a41fbb09419df9897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8d60a0fbfe8537e983c0c20b86f4b9362fca65fe1b8ee3287989fab22da234`

```dockerfile
```

-	Layers:
	-	`sha256:fdd1fa11a3eb08ef75ab0f406756f21d68ceac711a729d9e9bff8c23b7b50893`  
		Last Modified: Tue, 17 Dec 2024 23:30:50 GMT  
		Size: 40.1 KB (40074 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; 386

```console
$ docker pull redmine@sha256:d9e63ab36345443d0f67d4d004d329769adbfc95ab28b724d490ba31d75a49c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192144416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79066c17102df207897d004b5c7803626b19aee82377f1e41f146c3c117a6fd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af60f1cb4b6e732678c8e027d3afaabf456155c5d2d5a048b9a09304e7d1e86`  
		Last Modified: Thu, 12 Dec 2024 22:35:10 GMT  
		Size: 6.8 MB (6812912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f60202703919e30a94e46eb9cb4f21679f8d43abbe0596a5b4d33746b1db126`  
		Last Modified: Thu, 12 Dec 2024 22:35:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2a005e9537ea77476d4b2c7990047c1b16d0a35fc3ad873c344d51ceea63a4`  
		Last Modified: Thu, 12 Dec 2024 22:35:10 GMT  
		Size: 31.5 MB (31538629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73a5ec640647400802816d4431860654755e23303318d2d744c777c7afcc133`  
		Last Modified: Thu, 12 Dec 2024 22:35:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6a49a9e65fc4454394b169314cddc6984dafee006a391048acbe4765848570`  
		Last Modified: Tue, 17 Dec 2024 19:32:12 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca77436e4c40daed2457195f63c7f502f3b2811b4d07e153e41f8298d03f9de`  
		Last Modified: Tue, 17 Dec 2024 19:32:15 GMT  
		Size: 71.3 MB (71328942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b06e2a6c5e903083d6efb91f3b1a71e2f09dba408488b05070c6bc60b7870d4`  
		Last Modified: Tue, 17 Dec 2024 19:32:13 GMT  
		Size: 1.2 MB (1172813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34972ed5b0d6954f911cbbd5d23af040d1efad9f6664b651e9aa3f0da9b455ab`  
		Last Modified: Tue, 17 Dec 2024 19:32:12 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1c81811abb57648c93718c86dcc50031b1031f283a827d9592e101cb319812`  
		Last Modified: Tue, 17 Dec 2024 19:31:27 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5875d81ec9a34743fa5ee2c46ee06fbff464ca8a4e17933b4e7509dd6ad94c5c`  
		Last Modified: Tue, 17 Dec 2024 19:32:14 GMT  
		Size: 4.1 MB (4060101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba0c2220d1c4fea07e3dfb01f412f8def09b235eb8230f21ef3ed54671786b0`  
		Last Modified: Tue, 17 Dec 2024 19:32:16 GMT  
		Size: 73.8 MB (73761465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dc5be93e78214a659eadbf4767473d9cae85d470e8a7505b7bb3aa9d1f204a`  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:0fab3efd997e0c2ce9d3b2d4b97cb0ff0b8b0ad6676c1cd24ebef99adae58362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ea27e4c1bcf87200bcf97b888333c93512d53286131a7353abdc368aec30b9`

```dockerfile
```

-	Layers:
	-	`sha256:7261b060119a546c85cdd6d7ebbc2bc36e0b2c193d1e5a666d4d03b2521a1578`  
		Size: 39.8 KB (39785 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:e2501e7698c2f17ce167a6f259e98779d3e90da4e8dae4f22d428d0c35c4af7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196684875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebf47865c1531e35d5a5c1d238d0ac0cd311ca171e4d6ab2f2d6647cec9e3d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676156afc2c12432e0980f532fdeffea339a7cc94a718922ec11b6d5883876af`  
		Last Modified: Thu, 12 Dec 2024 23:10:38 GMT  
		Size: 7.0 MB (6953097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7491226cc0abb0eabfcc83b89733822f2d8340bd052ce4e91ffade3e9bc6d3`  
		Last Modified: Thu, 12 Dec 2024 23:10:37 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f20e5605459374df16abf4fcdfff26e227310216bd9886a4acee39aaeb2579`  
		Last Modified: Thu, 12 Dec 2024 23:23:14 GMT  
		Size: 33.0 MB (32998225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325fe29375035d9984a2067f14f284bd76f79b98c4d13f0544dbf6634a7e5d8d`  
		Last Modified: Thu, 12 Dec 2024 23:23:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be47aa26e25ecdee578a4347697d0fea0a83bb10c382c340dd6cd47eaaaf9e9`  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abea51fbcdb199cd491dc2c324b38de58fab6940f42e7489b59cb0d81cad8594`  
		Last Modified: Tue, 17 Dec 2024 19:37:23 GMT  
		Size: 72.4 MB (72435653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba5015c8275ff9cd61bf09ad2257c3d6818386cc0168c202fdaa4de2d721c03`  
		Last Modified: Tue, 17 Dec 2024 19:37:21 GMT  
		Size: 1.1 MB (1115190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4653640fbec8c5d50cf1486a167a238e03188a20a3631c597263b2156ad8a8`  
		Last Modified: Tue, 17 Dec 2024 19:37:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156566e411ada2bccae1f82d47068136348982874964254d5fcbb118286216e0`  
		Last Modified: Tue, 17 Dec 2024 19:37:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441c10a38f5a4591f5eeb521a0f6af99f408a36c432961ad9d6512ab43a8cba9`  
		Last Modified: Tue, 17 Dec 2024 19:37:23 GMT  
		Size: 4.1 MB (4060107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff78c0eb312c0f2249eff53fdfa9209bc9b07719017121205507c62a2bababd`  
		Size: 75.5 MB (75542016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ae8033bda558c6672e1332e29d664836014562856f5d80d94f5d904dda9ddd`  
		Last Modified: Tue, 17 Dec 2024 19:37:23 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:c1e18d84100ccfd9f5e43b5079c0e956771f204472cc3c60ae2e1a78a65336b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 KB (39925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00c5c6b2ebe18ee05ad6351860c5328fdd4138f8a4d25f752af0b57b185cfba`

```dockerfile
```

-	Layers:
	-	`sha256:4d434c118f00cd10671aa2723776037fa0b30ed07978db47e1c6b1f8a69c751b`  
		Last Modified: Tue, 17 Dec 2024 19:37:21 GMT  
		Size: 39.9 KB (39925 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:936bbded7234390f24997241437a075481cbb756b5d89ce8c5b52369cc63da45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193465540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b87e5ffdc786ad3be35d55ba862a5624aa8d847e06edd65e6fa702c283d3bd7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7db57ce6582cad423aa019d67c20ca5f5e16ec97e975335764cc1996c665f`  
		Last Modified: Sat, 07 Dec 2024 00:25:25 GMT  
		Size: 7.0 MB (7000654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b63656a2dd88416c17c13243099944dfea98286c4cdac0fbbd1551c76ce582`  
		Last Modified: Fri, 13 Dec 2024 08:26:39 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983c7eeff23753c494f2c539cd9b38e037e9b354056d9a3ad6e9dba54a8a33dd`  
		Last Modified: Fri, 13 Dec 2024 12:03:29 GMT  
		Size: 31.3 MB (31311554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e643f2261112d696935c20a29c89dafb919109e3ac41ea01211c3681a61f7910`  
		Last Modified: Fri, 13 Dec 2024 12:03:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc525904a63d170585d36573608a47c97622ff0ba869bc2755698490e8468155`  
		Last Modified: Tue, 17 Dec 2024 20:31:17 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0210bf24e94aa05afd518307113d59b9ccb457434edc52ba98de68e70a8d25f`  
		Last Modified: Tue, 17 Dec 2024 20:31:27 GMT  
		Size: 69.6 MB (69552778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c585031e2acb8e7c5a5daaf16efcebe6e82fe624450a36ac21dd831e976cc14`  
		Last Modified: Tue, 17 Dec 2024 20:31:18 GMT  
		Size: 1.2 MB (1165130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80f6beab5424c3ba824832a5de8943c523491ed20dee03d69abdc4d60ece6c`  
		Last Modified: Tue, 17 Dec 2024 20:31:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d0d4b48ababd9c6c48509e539c39f68eb911e1b3b844547fe87996cf1b0a56`  
		Last Modified: Tue, 17 Dec 2024 20:31:18 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bd3816007f501c70c4bed533118b08622efe27b1e9a6a4e6bea98b5b5b7c85`  
		Last Modified: Tue, 17 Dec 2024 20:31:19 GMT  
		Size: 4.1 MB (4060022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51d5d1db7c76699a235cefcc34d145d9c110b55642daff7e8b6e3d753b7ae33`  
		Last Modified: Tue, 17 Dec 2024 20:31:30 GMT  
		Size: 77.0 MB (77017899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b91690d8f6bfa8d7e85fd997958a1fda491c509ab9a309ad0e1476a57fce0a`  
		Last Modified: Tue, 17 Dec 2024 20:31:19 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:ccfaff1e881fe6205617ed687c9637c42660d3e4038633299810221096b6d8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 KB (39925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f030b55d82d2a5eb73c970e9f5fed220caf59bcadb5941c0507778ce6b9ec54a`

```dockerfile
```

-	Layers:
	-	`sha256:5b04b4635a48ba13f228767b8bb8105e7ea9daed0499f915e0336046ea4dea30`  
		Last Modified: Tue, 17 Dec 2024 20:31:17 GMT  
		Size: 39.9 KB (39925 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:afd79d28740a46d58b64f0b5a1d06f91b6082f529fc458a65599e71e76663b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194749406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75761d5e03e3bb3490653cbef37262b51179b14a5094d3e047634e50531aeb0d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV LANG=C.UTF-8
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_VERSION=3.3.6
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Fri, 06 Dec 2024 12:18:01 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 06 Dec 2024 12:18:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Dec 2024 12:18:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:28:14 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:28:14 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_VERSION=6.0.2
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Sat, 14 Dec 2024 00:28:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Sat, 14 Dec 2024 00:28:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:28:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:28:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:28:14 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:28:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b1f2773e2373f026433fba037fb86a595d266626e42b662f8860b751051e6f`  
		Last Modified: Thu, 12 Dec 2024 23:30:57 GMT  
		Size: 7.1 MB (7120254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864ec4ce260568825466b713bba3f9b2fa5a20892a04198640c61084b49eb264`  
		Last Modified: Thu, 12 Dec 2024 23:30:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b4968fe585d95350f5b783349a96b3c374014aabb7194420884403d370892f`  
		Last Modified: Thu, 12 Dec 2024 23:51:53 GMT  
		Size: 32.8 MB (32778273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179a4112b44829f776bef61721047109c4474951e2a22356eb2fe2305e4fdfd8`  
		Last Modified: Thu, 12 Dec 2024 23:51:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8e04b5df2b0d1127a035e55134e68445033c6cf030edd21df40d292fd58031`  
		Last Modified: Tue, 17 Dec 2024 19:38:23 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1818f9c61cf356e887215bdb505c3795b4476e71a9c168167e0901d4bf803712`  
		Last Modified: Tue, 17 Dec 2024 19:38:25 GMT  
		Size: 71.4 MB (71357842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66dc872779c8a25418f15a4e070c4038bbd9062d9ef3b4a894d889c227e26bd`  
		Last Modified: Tue, 17 Dec 2024 19:38:23 GMT  
		Size: 1.2 MB (1161440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92d7826f0348b948c2e58c5c555b3f4b9645e74be670f66b638a33bb6f02f21`  
		Last Modified: Tue, 17 Dec 2024 19:38:23 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5029346b03f5991e5cbc45484b2b7deb41766249e3e4e4000ba4ef68495985a1`  
		Last Modified: Tue, 17 Dec 2024 19:38:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aada8726e32463ed2dce588a07652adaa007b254834aa2171af178fc97d7136`  
		Last Modified: Tue, 17 Dec 2024 19:38:24 GMT  
		Size: 4.1 MB (4060081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52907682d639c974a38524ee827f7053aeb5b8dd4c9a07840a81c71a2197a30`  
		Last Modified: Tue, 17 Dec 2024 19:38:25 GMT  
		Size: 74.8 MB (74798516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92489d4f7a40e4500cedcb8badfd671527fb7edadc8c9b11bb2ab7a8a7788900`  
		Last Modified: Tue, 17 Dec 2024 19:38:24 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:5392714f5448445b6305879bba71017827e631b9ca305d135c2bfd5130461f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1d8672441ad3c5297b9a3e0267d634b617704b808833def265cb745ac40833`

```dockerfile
```

-	Layers:
	-	`sha256:3748b018a008682a09e4b9c1da480f6123bc00ac83afb3fb1691fbfc97b5f97a`  
		Last Modified: Tue, 17 Dec 2024 19:38:23 GMT  
		Size: 39.8 KB (39846 bytes)  
		MIME: application/vnd.in-toto+json
