## `redmine:5-alpine3.21`

```console
$ docker pull redmine@sha256:2ec8cd220e9952031dbdbf81c1cbd4d13db958d280290146454f76743376acbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redmine:5-alpine3.21` - linux; amd64

```console
$ docker pull redmine@sha256:37dca520a64192bfaed0afb525bcaf6ecb199065355a2504e4f02cfa53787d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189323098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56ce2de5bed6899708221100c4695f78f575ba4528dfb3a1325a6cac5eda02b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd163b5c17743f01933abd202350ee05fa691fe1415cae3cd07affd60205da1`  
		Last Modified: Wed, 15 Jan 2025 18:07:47 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a9184bf82ecc6fae78a7d24164b5f3abb8cb5750dea5636503aba0f5c30a22`  
		Last Modified: Wed, 15 Jan 2025 18:07:48 GMT  
		Size: 39.8 MB (39820627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064dbe88a353b879629342f921cdf967433433914c4c3a7359df57f0dce933db`  
		Last Modified: Wed, 15 Jan 2025 18:07:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e4a82e36efea0420a62a6573117d9f44015fcc242071608f9783357842d4f`  
		Last Modified: Wed, 29 Jan 2025 23:29:15 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f307035d91016a8d5b597cadde22855314af61ba1bbc76fd696f0e3fbdf26a`  
		Last Modified: Wed, 29 Jan 2025 23:29:16 GMT  
		Size: 70.7 MB (70716892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22094addc3c3f2860f2c3b05257757a3b21af888fa303101543324d1a4d0d46c`  
		Last Modified: Wed, 29 Jan 2025 23:29:15 GMT  
		Size: 1.2 MB (1197862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23dba5a2193f34221a005324428ab321fc5ed40e3666ed92ca4f1d2021ba83c`  
		Last Modified: Wed, 29 Jan 2025 23:29:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f583e02ff1af502e7501597fb1d0424794b1f8230ef1d4f4d0892d66b51387f5`  
		Last Modified: Wed, 29 Jan 2025 23:29:15 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08e5778ecf6093f3a6ac263f3087c9f492a2090905dd35b827743764d2c0f2`  
		Last Modified: Wed, 29 Jan 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28c2bcd973e7b3232ee0f5b561656e47354d14b96111c06900f66835c2d80c1`  
		Last Modified: Wed, 29 Jan 2025 23:29:16 GMT  
		Size: 3.2 MB (3243728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1851da7f296c9219221736ede9e0163fe19277d18a1dc60d04bad185ace08f42`  
		Last Modified: Wed, 29 Jan 2025 23:29:17 GMT  
		Size: 70.7 MB (70698285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178ea2f37df6178b6c877c3bae128d3b8c5730b62e9b2bd9f24cc445af4ac2f2`  
		Last Modified: Wed, 29 Jan 2025 23:29:17 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:77282aa2da821c270eea78bdb290039d3f042dcad7b8f1fdd37c15028d527a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852c4f42d0a2183a8e138f0d54b27921708f6cbdec2bdbfdf8b21b8a99bca2dc`

```dockerfile
```

-	Layers:
	-	`sha256:a2611395d1937ffc52fc8ab511aaf53c96ccdc0c28a66e966830df04bdd2fb8a`  
		Last Modified: Wed, 29 Jan 2025 23:29:15 GMT  
		Size: 40.4 KB (40359 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:0f370117573f96495de3ca33f80402b75d351332d2068398a8a3121e8417c6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189300281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5340b3f185748e2ff4fc96a3ae1240f5784b07c8c722df37d12c9b985625f04`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2615d5d8dfa2981e23aba3f735f6fca0982072fd5c6a64920afc860d6226df3d`  
		Last Modified: Tue, 14 Jan 2025 01:42:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bed836937d7bb2e4758ab6944d6284409e08a10aebc3b6270f717c431195d6`  
		Last Modified: Wed, 15 Jan 2025 19:39:50 GMT  
		Size: 39.8 MB (39811647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538fa991644a90c96c2374ef03858e97d72ac185811b60c8d9af1fdfb3bdaa85`  
		Last Modified: Wed, 15 Jan 2025 19:39:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7402b37ceb0d18ed8e8d63426f66969886c8c1c636e8894ded211760b9895f24`  
		Last Modified: Wed, 29 Jan 2025 23:45:42 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a5bb800faf1a9818110b7fcd0d99253072609a8e14c7ad1c6d231fea607c87`  
		Last Modified: Wed, 29 Jan 2025 23:45:45 GMT  
		Size: 70.4 MB (70419244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d20ca530e215d5e58d127bad8fc121a1f1d579cce35bf2aa06ced3fde5ebe8`  
		Last Modified: Wed, 29 Jan 2025 23:45:43 GMT  
		Size: 1.1 MB (1123965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a83fd53b1eccea5c70e295ff34abe54bf4d28fa7c8dc753e6f372bfb1fabb1`  
		Last Modified: Wed, 29 Jan 2025 23:45:42 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffefc2a99ecc246e0bd67013b235b21b858494b421c37d22325b64145b72bad`  
		Last Modified: Wed, 29 Jan 2025 23:45:43 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbedb98ffc79a526e607c2c920b352f4136959bfb051ef8a2352c00d4edeaf2f`  
		Last Modified: Wed, 29 Jan 2025 23:45:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22cc079a743e61485a4a000ce7f617dac2c407ffcaf6bb72b53620cb9594d0`  
		Last Modified: Wed, 29 Jan 2025 23:45:44 GMT  
		Size: 3.2 MB (3243756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce893b918a3786fd490c6bd771946939abbe6134dd4375d9838edde6f31e6d1c`  
		Last Modified: Wed, 29 Jan 2025 23:45:47 GMT  
		Size: 70.7 MB (70705320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d70ef0fcf53be148f73d356b5ac47377bba99ea863a6c712c4af7ddc35730e`  
		Last Modified: Wed, 29 Jan 2025 23:45:44 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:6beaa3250981f1f659d9ea399ff847903547dd9113ea3c3edfff565f2ba58a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2941fc8cd5d0d011e054321377f62564854f5caf1756cbb094420d9d1c0ca5`

```dockerfile
```

-	Layers:
	-	`sha256:a9ba58b637f24cfde28e88516f81b4851ecca864d0445e5d071de06baee02af8`  
		Last Modified: Wed, 29 Jan 2025 23:45:42 GMT  
		Size: 40.6 KB (40577 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; ppc64le

```console
$ docker pull redmine@sha256:24e2a190329405ad5fdc00b6f1c2253fd9ef8c4d2be655f00f96915b81430a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190491029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ad5d6bd28b3fe14bb578abf1b4ac01d955d41432ea87dfa1a300c564658cd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fa082cf274421d4c78de9388c1d638ea51a72957cb0c9671c02d801d001eeb`  
		Last Modified: Tue, 14 Jan 2025 01:45:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69746e6b5fad1aa797f89ad20b927ef266f50e357f491d1b5c4cff700a8bb4c`  
		Last Modified: Wed, 15 Jan 2025 19:06:54 GMT  
		Size: 37.7 MB (37663399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9bab794cba6fe557908d7d31e5166b32429b7ea03837e89d434e76ba077a09`  
		Last Modified: Wed, 15 Jan 2025 19:06:53 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82872685bd46aa7a91734cec5038f6f7cd1cd8ae34d22eadb183330651506d26`  
		Last Modified: Wed, 29 Jan 2025 23:55:38 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b1496569d665de7b5466ada1040d8e38b56dc0e6fcd5829dbc5adc81cd09b5`  
		Last Modified: Wed, 29 Jan 2025 23:55:40 GMT  
		Size: 72.3 MB (72307694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11814fab5d4892ea1b85f5ffea7713b8f8bbced44ccabbd56747c2aef2ba8785`  
		Last Modified: Wed, 29 Jan 2025 23:55:38 GMT  
		Size: 1.1 MB (1115265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc1e2db7136d0978684656b6bb82d035f36cc9705df635eb17c75e67fb8eea3`  
		Last Modified: Wed, 29 Jan 2025 23:55:38 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2fa226d490b93f8e5ef10c7bc2a9fb2ea27425a4aa7f46258d4f53f3841f97`  
		Last Modified: Wed, 29 Jan 2025 23:55:39 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7735e8a18dcc9de9e8d15d4456255de2ce0b0450d69bf6c1eb616eadf807de5`  
		Last Modified: Wed, 29 Jan 2025 23:55:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d789a5d6ce7c81f0e312a82fb0105cb6ada5cd15d780fba88d3ad21ea915cae0`  
		Last Modified: Wed, 29 Jan 2025 23:55:40 GMT  
		Size: 3.2 MB (3243714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2424c7cb9185cb1b50eaf6a32df065179ca0484d1919b90a0bf14ae59ca35eb0`  
		Last Modified: Wed, 29 Jan 2025 23:55:42 GMT  
		Size: 72.6 MB (72583365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931210dd50bdc60cd8033da1d913dcdd588996018b3bc33a6d539a464e465f01`  
		Last Modified: Wed, 29 Jan 2025 23:55:40 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:9022caf597388064e033774bf9e03c272202e77ca6ff204cf54c5c2102a9ae1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df915c54b8b5b919f5da0314ba1978179774a6f6d232adf2201d65f1b06d61c1`

```dockerfile
```

-	Layers:
	-	`sha256:9df89c99e13e77bfd5202b758df06dfee6a899984debee5f850f35be66d05b89`  
		Last Modified: Wed, 29 Jan 2025 23:55:37 GMT  
		Size: 40.4 KB (40426 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; riscv64

```console
$ docker pull redmine@sha256:e21bbc63310ae982cd5e38965f9d14cfc3dbeb902fe7f15c54dc86b755a17bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187465252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8f2c02ab148300b2b6e459a782a6ec2a76c28e5c12703ad03c6fbadd607fbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f58c5f1e872ea5fb6d2093f25dc7e3e4e42116a78691c8d841fa04894fccb8`  
		Last Modified: Tue, 14 Jan 2025 03:53:39 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee55fddd6f026359c3fee5b9e7e01ab03ec35ed3d32cb6bb4ecb11418d66c54a`  
		Last Modified: Thu, 16 Jan 2025 02:02:32 GMT  
		Size: 36.1 MB (36145304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b701e17867f4e4f557f001ac13f7fb040d4cf813da672989943bdc623c360e4`  
		Last Modified: Thu, 16 Jan 2025 02:02:26 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca1f78d73137bd834f58036a503b6e5838862e46981a971174f6ee15d542949`  
		Last Modified: Thu, 30 Jan 2025 03:22:35 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb49ae2ddd83ced4ee327a4edf9b046fdd12e33d440e69e8c755e9fc291a31b`  
		Last Modified: Thu, 30 Jan 2025 03:22:48 GMT  
		Size: 69.4 MB (69444868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50b13f8036083c56d8fc0d19c325808384e45d5bb7952e8a1ce332f8504bc5c`  
		Last Modified: Thu, 30 Jan 2025 03:22:36 GMT  
		Size: 1.2 MB (1165182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48119c92650983684da40f3e9e98960291f2948ed8d27bcd0cb8e3026c9ccbe4`  
		Last Modified: Thu, 30 Jan 2025 03:22:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a566f9c85b4bb400b404de65773fc1e6a52812f806e3262513d9dbe37b4a0c`  
		Last Modified: Thu, 30 Jan 2025 03:22:37 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d638e5700d1fc3c857ea4c4a11eecee3e13bb83ffca90c95b159d33ed3836927`  
		Last Modified: Thu, 30 Jan 2025 03:22:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0b6685295e8725d8f4d90b2bb658622e4ff0a01654349b5a24843213075dd5`  
		Last Modified: Thu, 30 Jan 2025 03:22:38 GMT  
		Size: 3.2 MB (3243770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8b7a6ea31914e26f72a8047c1a5d40ae0a2b28081a9a1cbbdf5f94c4c02db2`  
		Last Modified: Thu, 30 Jan 2025 03:22:49 GMT  
		Size: 74.1 MB (74111880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cf2f7fe1f368b29bd25c68da43564fc6da0d8e67c2420ce7543319df749ac3`  
		Last Modified: Thu, 30 Jan 2025 03:22:38 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:97c09327f829fc821c4c67e1ef4a2cee61d62f1f244a194b81ba32c677037ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbbf234f1118b1f698a020b4bf5139e8e4c8e1fa70e5a4b9b96aefc7dad4905`

```dockerfile
```

-	Layers:
	-	`sha256:219bdb1c957afb70bd9dbe8b38cd2e63546d3152975ec2829337b5a525667680`  
		Last Modified: Thu, 30 Jan 2025 03:22:35 GMT  
		Size: 40.4 KB (40426 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; s390x

```console
$ docker pull redmine@sha256:24c97511b0bd5ec5bafa0a7a1880b7c7635059fbe55634ae300925064a499141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188639212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa1156f85319be3cdf3b86dec6f0236a08a66b84b5d8d4f6f8d750d6a693a6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715918f0e770587d15212ec4d7b5b9eeb1c07e9bf7a302047dd6fe58fe3efb9`  
		Last Modified: Tue, 14 Jan 2025 01:43:54 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dd472c764d89718aa3b71c4e9c999d8f7748cf2336c55b9c08522316a5484e`  
		Last Modified: Wed, 15 Jan 2025 18:58:38 GMT  
		Size: 37.7 MB (37668559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60ac847b4c0a3bbc2a9a1e8e58bebd0baa8890d7975840eaef7a57e03538d19`  
		Last Modified: Wed, 15 Jan 2025 18:58:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554c83912b75c6ea56bc9208315f80ef9494c19e00d9bbd861d46e33adff7992`  
		Last Modified: Wed, 29 Jan 2025 23:56:30 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c94982d6d8149928dd57b0bde64c41fe7faa269501017df252196dbae9435dc`  
		Last Modified: Wed, 29 Jan 2025 23:56:32 GMT  
		Size: 71.2 MB (71220075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2ef92cea09bfea1a83139bd8f4c87bf4b15ff51dc16703d30e244dfb5efd91`  
		Last Modified: Wed, 29 Jan 2025 23:56:30 GMT  
		Size: 1.2 MB (1161444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858a7d5e390e00e94a9e04d83cbfacc0ab76218969bc976f60f6868dbb701a35`  
		Last Modified: Wed, 29 Jan 2025 23:56:30 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e62f98013c1056927f3d4a77c5fd9da9ab87c83ea3752821290dce7ed571193`  
		Last Modified: Wed, 29 Jan 2025 23:56:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7478996ccbfadcf53f293aae66fc9706a3ef0236fd4b960f9260a92f1fd00f4b`  
		Last Modified: Wed, 29 Jan 2025 23:56:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b904b6afee87c78ca2747d3d78b3f0dc7593188607570f9a4e63bf6dce89331c`  
		Last Modified: Wed, 29 Jan 2025 23:56:32 GMT  
		Size: 3.2 MB (3243729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44831a90e2dc27be0df2db57fb15cfa1776d595a621f45f14dd2268cf8d7d6`  
		Last Modified: Wed, 29 Jan 2025 23:56:34 GMT  
		Size: 71.9 MB (71874549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3526e108abdd92eac0f008c124fe672838a96dcdfcaf69393efca62416f73c57`  
		Last Modified: Wed, 29 Jan 2025 23:56:32 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:caeec71343905d1e68df925dcb78c342cb6f09aeeca6396be9e10e76543e33c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2bc33699f46d75350ccb1eb25313987e08c3ede024ba16eae7e3d1d001866f`

```dockerfile
```

-	Layers:
	-	`sha256:c37d5ae5027427eb3c31b88b3a8405a5047c50022b3f73585882def85d5cb435`  
		Last Modified: Wed, 29 Jan 2025 23:56:30 GMT  
		Size: 40.4 KB (40359 bytes)  
		MIME: application/vnd.in-toto+json
