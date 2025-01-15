## `redmine:alpine3.20`

```console
$ docker pull redmine@sha256:4628d32358699a8d5ccbd89f0af84643bad622756451c4eab381fca5e79760b0
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
$ docker pull redmine@sha256:71e149411a99873fe52ff8f6e4c37b5be89c1cbd048f8e3b137ff2c456976548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192799785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5323312b8a634d24c2ce2c9c7fbc834f6ca92710d1a045f4a0fdd96a8b8600f`
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
ENV RUBY_VERSION=3.3.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
# Wed, 15 Jan 2025 00:26:19 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GOSU_VERSION=1.17
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RAILS_ENV=production
# Wed, 15 Jan 2025 00:26:19 GMT
WORKDIR /usr/src/redmine
# Wed, 15 Jan 2025 00:26:19 GMT
ENV HOME=/home/redmine
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_VERSION=6.0.2
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 15 Jan 2025 00:26:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 15 Jan 2025 00:26:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d08567713ee4654619b3c081911888ef482b035de0e771dc68d2b77a58757d`  
		Last Modified: Wed, 15 Jan 2025 17:56:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8542b02054acb6fdcd8539a5d0227702477f9026747226776f845bc94d8426c`  
		Last Modified: Wed, 15 Jan 2025 17:56:11 GMT  
		Size: 41.5 MB (41485561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d0264e8f86aca9be2feba00d7429a1a400d9f459420f65d1642d215f7ac5ad`  
		Last Modified: Wed, 15 Jan 2025 17:56:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae2f474424f219bbf2e4942846bffd29f8192a21e632d72d224c3d3e77219f0`  
		Last Modified: Wed, 15 Jan 2025 18:34:39 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ddee75ba287ef44c2bb3de95f3b50f4933cbc2968e6d0eecdcf5ae7c772f89`  
		Last Modified: Wed, 15 Jan 2025 18:34:42 GMT  
		Size: 69.0 MB (68973152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29779059864544f557f5a47399394f3fdcfff63af2d5f120d0f741ca9cecf5a0`  
		Last Modified: Wed, 15 Jan 2025 18:34:39 GMT  
		Size: 1.2 MB (1195472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e14d0ed4273317d66d5e17790847a6f3d5d584a6e5742c2c3e66ca48f65bbb`  
		Last Modified: Wed, 15 Jan 2025 18:34:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9570d3b9f8349bb733b2c58ae88028ccb2313420b08457a8c25516682195f2b0`  
		Last Modified: Wed, 15 Jan 2025 18:34:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a93355a361e31a2cf730327ba06837b4131357bd2af12545a0759213b2f9556`  
		Last Modified: Wed, 15 Jan 2025 18:34:40 GMT  
		Size: 4.1 MB (4060080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0529b156d0cd21984d36f05800b1bdffe84fa8e030ec6f47504642d2e92ef118`  
		Last Modified: Wed, 15 Jan 2025 18:34:42 GMT  
		Size: 73.5 MB (73455695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0628d1f02ec88dc77bc2d0c4a0e92084ae4741333e0f5b879de73e5823287764`  
		Last Modified: Wed, 15 Jan 2025 18:34:37 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:d49dfa56e5fa5640c6e9a34640b21f543bb146b24de3a314afadb611b4558ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84eaf890d4a5f9731a063398ba30d5c863a87a02fd489304d003c7d5f10dbf55`

```dockerfile
```

-	Layers:
	-	`sha256:6f39259ede909c63011aa6898191db3a04a352470d2323bc8b6dc9a4a381aab1`  
		Last Modified: Wed, 15 Jan 2025 18:34:39 GMT  
		Size: 37.3 KB (37272 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:eb67c6feb2f3ee40a9dbe07d9ca97f690ee32869cd8215517ccbad8a3271adc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185049889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3661dc7508b4dec57f480dbf2f3c198e594ea1e1ed33da6d05eb85514c49d4b7`
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
ENV RUBY_VERSION=3.3.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
# Wed, 15 Jan 2025 00:26:19 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GOSU_VERSION=1.17
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RAILS_ENV=production
# Wed, 15 Jan 2025 00:26:19 GMT
WORKDIR /usr/src/redmine
# Wed, 15 Jan 2025 00:26:19 GMT
ENV HOME=/home/redmine
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_VERSION=6.0.2
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 15 Jan 2025 00:26:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 15 Jan 2025 00:26:19 GMT
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
	-	`sha256:445eaee55ebefeb5222aac15da4e547925bf213ed18d00782213397526c83845`  
		Last Modified: Wed, 15 Jan 2025 18:12:23 GMT  
		Size: 37.9 MB (37902665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1e5d90fdbaf124d486c361455a84fc0e2e0b5a2004d3401ba64585fad25d76`  
		Last Modified: Wed, 15 Jan 2025 18:12:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7947a52000fa2fb244f7a77d28c7d038c3002551cb41cdcb530c12954f1fc274`  
		Last Modified: Wed, 15 Jan 2025 18:36:57 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea57e548ec9fae11a52af441fc61d099c2071db50eaeb409d0fec59c5a89cb4`  
		Last Modified: Wed, 15 Jan 2025 18:36:59 GMT  
		Size: 65.8 MB (65795962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b176a4da916c96e660eb2943148d637fa47d146c01ff258a035bb21fea79442`  
		Last Modified: Wed, 15 Jan 2025 18:36:57 GMT  
		Size: 1.2 MB (1162198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9d3ef790f284c30158c34604a379eb86f7011016d8e9883464251335733d9c`  
		Last Modified: Wed, 15 Jan 2025 18:36:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0447a3606ffa25aabe7d24565914f9c8c410d0fb18a606b3a861cb346e9a91`  
		Last Modified: Wed, 15 Jan 2025 18:36:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d1256f08d0f343019a69dae09c113c6bfafcfc080cd720148a9874b1439c00`  
		Last Modified: Wed, 15 Jan 2025 18:36:58 GMT  
		Size: 4.1 MB (4060068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6905f1a734ee29a47e59242365dfe2f69f5bdd6713160ce3997471f77c29c9c7`  
		Last Modified: Wed, 15 Jan 2025 18:37:01 GMT  
		Size: 72.8 MB (72753956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b31052f5b99b3f316b208334e8aa54c4f44e296ffbd76fdfa798aa6fbfeb4b`  
		Last Modified: Wed, 15 Jan 2025 18:36:59 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:d7f312dcd072d27c36c2657d1054fc9dd749026ca7794976ee573938d1f8c200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b706b3567fcb12beb17b9d2ac1ca0deb7573f30522a20f571ade94fb6087ca`

```dockerfile
```

-	Layers:
	-	`sha256:a853689b7c1edc0b71a163571bb7ae116e3724cad0b639cf041fc5cf239a202b`  
		Last Modified: Wed, 15 Jan 2025 18:36:57 GMT  
		Size: 37.4 KB (37412 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:e269b4eb4fe8ed0d0c27f82f1279e6c9dc28586fb02c9637abb47c0edece3705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (176000334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812c866118e71fc71b29c89d6fb7264190000b7aae40d1dec3db1de23e47602`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV LANG=C.UTF-8
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_VERSION=3.3.6
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
CMD ["irb"]
# Tue, 14 Jan 2025 18:28:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_ENV=production
# Tue, 14 Jan 2025 18:28:33 GMT
WORKDIR /usr/src/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
ENV HOME=/home/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_VERSION=6.0.2
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 14 Jan 2025 18:28:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 18:28:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 14 Jan 2025 18:28:33 GMT
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
	-	`sha256:e217360eafac4a3cdf41c6264934a1a632cf72f350f1cacc67e957a1d24ec711`  
		Last Modified: Tue, 14 Jan 2025 01:52:46 GMT  
		Size: 31.6 MB (31604091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e69ea06e9cc6b26804f8cf475165319b6321b07d4dc00212b4a69085ca5b10`  
		Last Modified: Tue, 14 Jan 2025 01:52:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faed021bd09ff5e594d0bdd070f4523aa9b8d6fda1c3f0e157538d45efe85f35`  
		Last Modified: Tue, 14 Jan 2025 22:54:28 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4d298abd31f35b88b6bdcfebac19534b9c14ba4ee28423b94d020185ea8667`  
		Last Modified: Tue, 14 Jan 2025 22:54:30 GMT  
		Size: 64.5 MB (64456985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add004827a744ced37c7f61507dac20fc50241b2e872006fcb365056d04f140d`  
		Last Modified: Tue, 14 Jan 2025 22:54:29 GMT  
		Size: 1.1 MB (1133459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58f40d7334f44044cef4dc2164246a8e597b846bd75d6723d1aab47e7ce5be8`  
		Last Modified: Tue, 14 Jan 2025 22:54:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ffafb9d245cf361e13e85f968770e7f6dc0c486501d247af2a05a4a5e61b00`  
		Last Modified: Tue, 14 Jan 2025 22:54:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a09ad8b0f99092fdee12f72b2fe0948979ca21aa1da00d27e301dff9f52903`  
		Last Modified: Tue, 14 Jan 2025 22:54:30 GMT  
		Size: 4.1 MB (4060063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38b6437c5a36dc144f5af2e5f426e7d3cc1647700bf5c42b3424dd0e5098bbb`  
		Last Modified: Tue, 14 Jan 2025 22:54:32 GMT  
		Size: 71.6 MB (71646740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304c95b4708277f992e3bb3aab34cf1d14e24efd0b2b935430e738fe4930a80c`  
		Last Modified: Tue, 14 Jan 2025 22:54:30 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:2ef20fb7672e0f999339bf1cdcbf1543eeeaf1573df4e3f04773234b98930b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca91403ee8749408ecce55d54eac7460bb4d986cfda5a1e61f3dda32ce42150`

```dockerfile
```

-	Layers:
	-	`sha256:baee153986d19c721945c3b303c9815954433cdde26c4d03e114b304aa7c2140`  
		Last Modified: Tue, 14 Jan 2025 22:54:28 GMT  
		Size: 37.4 KB (37413 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:0a93a6e4dcdaae9c3911a0e8227f7655ad4bb3e9852cc23a7cbc0e391acd7fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194133382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22067430ed94e772017ea44007f3abb02f38f4a3eca67e8dc037b219513fce5f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Dec 2024 12:18:01 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Fri, 06 Dec 2024 12:18:01 GMT
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b572e645df3b8f5c248f9f9b0e7b15e0d6fa5d7790abf6a9a60db0418e2be2`  
		Last Modified: Thu, 09 Jan 2025 05:42:04 GMT  
		Size: 6.8 MB (6754232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3722ee29de480f844f1dff74474d04ec9e2e87b69a0ebd7a085138c2df3f45b`  
		Last Modified: Thu, 09 Jan 2025 05:42:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bed2e0ce24d3318bfa027ce9bcf1ba813e3105ad7f40e9dcf2c601f027d0229`  
		Last Modified: Thu, 09 Jan 2025 05:46:52 GMT  
		Size: 35.1 MB (35147502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401b06719eda174ff99bc174c9d73ef8eb534c12f166324a09153f917367247f`  
		Last Modified: Thu, 09 Jan 2025 05:46:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afbcdec5e613165284fee14e8e003be03860293d337022fbfc0249f32435278`  
		Last Modified: Thu, 09 Jan 2025 08:32:29 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d3995c032b6ea5bbe408600dfcb9daf5ce5939f096e2cd73ecab135f104142`  
		Last Modified: Thu, 09 Jan 2025 08:32:31 GMT  
		Size: 69.5 MB (69452181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0845d1420d7748aaa731fb9167557cf15c58bb40488fe4f7843e89c087129a2`  
		Last Modified: Thu, 09 Jan 2025 08:32:30 GMT  
		Size: 1.1 MB (1121167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab7a3ced0ababc29f2f742f9f7e91ff7346ac23f9e6cdde08c1277fd49d5a2d`  
		Last Modified: Thu, 09 Jan 2025 08:32:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12778eafc083262e6e81b627e971d25a0b131dcafd4bd90ba4e5a84faa41779f`  
		Last Modified: Thu, 09 Jan 2025 08:32:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc04f6adfb17afb56f7e201f002f64c372002a0eaca06f9ed3ca848930cfe297`  
		Last Modified: Thu, 09 Jan 2025 08:32:31 GMT  
		Size: 4.1 MB (4060077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac69bcf0ee2e21cd540e3e828214e115f04f7ff0b8fd03db2800a438466e183`  
		Last Modified: Thu, 09 Jan 2025 08:32:33 GMT  
		Size: 73.5 MB (73503979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82baa1b03b707e8cb8e963a5698c1fb74c848143241fb74d14d9a556ce8b171`  
		Last Modified: Thu, 09 Jan 2025 08:32:31 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:10f6a8e25296a9e511489cbc9f1f5bc0559db652301f193b2d992c49113bad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 KB (38802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af28e98a2b60b9a86c95b6b0b187431c5c522d45b05f24ef7dc01b4db2e94d1`

```dockerfile
```

-	Layers:
	-	`sha256:a6dfeece04077eacc4a970c494d9a45f12e0f6889fe3f6a6271410d735241895`  
		Last Modified: Thu, 09 Jan 2025 08:32:29 GMT  
		Size: 38.8 KB (38802 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:1cd6634e0c46ad6f63c7b9e0957366c5538485c51c8b2b6edbeba4e111e8ede9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189855025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97b5cb183af2848a5b95f3808af0fd67e88c319e35d4f9b055cb47913b20627`
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
ENV RUBY_VERSION=3.3.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
# Wed, 15 Jan 2025 00:26:19 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GOSU_VERSION=1.17
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RAILS_ENV=production
# Wed, 15 Jan 2025 00:26:19 GMT
WORKDIR /usr/src/redmine
# Wed, 15 Jan 2025 00:26:19 GMT
ENV HOME=/home/redmine
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_VERSION=6.0.2
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 15 Jan 2025 00:26:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 15 Jan 2025 00:26:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560bf2b61eeb378500d9ba9dd5edc9e853df142f37bdde675773aa04ff1d75c8`  
		Last Modified: Wed, 15 Jan 2025 17:55:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abff4a51be139486cdd1d94b8669f4d249e4b4af87b219e3043a76e1d898c14`  
		Last Modified: Wed, 15 Jan 2025 17:55:47 GMT  
		Size: 38.0 MB (38000376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb825077175bc50f14fd2b7ea5c672259c3978724a3b7908ff4de2628f23650`  
		Last Modified: Wed, 15 Jan 2025 17:55:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9f7f6f792119819aedee7dbb21cce59b6a1dbf5bd445f62099d84599a9aee5`  
		Last Modified: Wed, 15 Jan 2025 18:33:15 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede628dbbccf456566d93b182f15abc3d77430dbb4b3f2dda77ef32d7cce24ca`  
		Last Modified: Wed, 15 Jan 2025 18:33:17 GMT  
		Size: 69.5 MB (69546058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0939e846ef676952225b9482b79bfca93a0a69792de7570ceaca5ce5c0010c5`  
		Last Modified: Wed, 15 Jan 2025 18:33:15 GMT  
		Size: 1.2 MB (1170669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e645eca41242a541b502960c046011202b1905cb13c0055c78399d6ef58a4`  
		Last Modified: Wed, 15 Jan 2025 18:33:15 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cd15a3193f4690dd5fd3294661aa7f7c47acff26f096faae84a7ae35c231a0`  
		Last Modified: Wed, 15 Jan 2025 18:33:16 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57d4f772c9b3cf18520f07714c30828501177661d35796f0975baa59266c815`  
		Last Modified: Wed, 15 Jan 2025 18:33:16 GMT  
		Size: 4.1 MB (4060070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc3760b0507a9150bf8f94e25cd5a10216cb88db238cd0adc2bc626ee40b936`  
		Last Modified: Wed, 15 Jan 2025 18:33:18 GMT  
		Size: 73.6 MB (73603316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c87524cfef18d5112a9388e34d26fef17d903f503935a6b3e7d0c3763e6e414`  
		Last Modified: Wed, 15 Jan 2025 18:32:50 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:4029cd606ef4acd566cb36ade4e2eff57ada6298620eef721b498f39125aca97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd97fc78a7a61d4943468b5cea5ad9a5de2575a4fe0ce670f498006764eb19b8`

```dockerfile
```

-	Layers:
	-	`sha256:b0b4f88951ef5b6f4347a9c09c42f09ad82d7232700cb437055ee5088692deb0`  
		Last Modified: Wed, 15 Jan 2025 18:33:15 GMT  
		Size: 37.2 KB (37229 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:3867aab2bfd3ed86b7ae30e47acff3cc83a25f92819433390c74df173bb39198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194299317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4938e7e1690fba70acf2865e49c61a877efcb5d08c22a3a7503cfd860810a940`
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
ENV RUBY_VERSION=3.3.6
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 14 Jan 2025 19:28:22 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 14 Jan 2025 19:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		apk add --no-cache --virtual .ruby-493-backcompat 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
# Wed, 15 Jan 2025 00:26:19 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GOSU_VERSION=1.17
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RAILS_ENV=production
# Wed, 15 Jan 2025 00:26:19 GMT
WORKDIR /usr/src/redmine
# Wed, 15 Jan 2025 00:26:19 GMT
ENV HOME=/home/redmine
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_VERSION=6.0.2
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 15 Jan 2025 00:26:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 15 Jan 2025 00:26:19 GMT
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
	-	`sha256:0f37cc249efe39caa961589f63c31c6cf7da9d54af8f28cacadafc3b6a3372ea`  
		Last Modified: Wed, 15 Jan 2025 18:57:29 GMT  
		Size: 39.6 MB (39605929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04256c8d92f8d4dcc849c4bb1853936b94ff8c9686f10467f60eabf4b0305ef2`  
		Last Modified: Wed, 15 Jan 2025 18:57:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13238b70c8e3ccf59cd73469b0a856d8e83b44b6cc7fab04265744e740706a26`  
		Last Modified: Wed, 15 Jan 2025 19:45:58 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee67f1261c8773268de63f518e89c618e0fcd73ae41690a79dbe59985903d72d`  
		Last Modified: Wed, 15 Jan 2025 19:46:01 GMT  
		Size: 70.6 MB (70560317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b0ce1f0bd18ff634727bb21bb46472beaec98789d00ab0183498f4aeddc9fc`  
		Last Modified: Wed, 15 Jan 2025 19:45:59 GMT  
		Size: 1.1 MB (1111699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9356cdf3e748ca23202eb85b662796fea6697ee20ff89eee15d03fd26508ac9`  
		Last Modified: Wed, 15 Jan 2025 19:45:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9245f6598e2a0897dfc5e028451ccc15934bfe3456cfe0ec5d5404f05c6662d8`  
		Last Modified: Wed, 15 Jan 2025 19:45:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e956a2cdddb3083b54e184daf128aaf16054a9a329a24997c5378585ac357a9d`  
		Last Modified: Wed, 15 Jan 2025 19:46:00 GMT  
		Size: 4.1 MB (4060065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dd9d037b4843d697f673bb75ea5937abc4fbd687204e24c113748f31329774`  
		Last Modified: Wed, 15 Jan 2025 19:46:03 GMT  
		Size: 75.4 MB (75383335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8cbb788c904a4dbef1cc49fb0c0da61d16ea40ae405a3912e9734df3bca274`  
		Last Modified: Wed, 15 Jan 2025 19:46:00 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:0bf9f4ec4ca23d1dacce70c4a36cb42f134d41c0722e2311e1f9268d2556e6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b178ced787a34690a5e9ebc696348c01b378e21c138d03d9eb91b19babcd001`

```dockerfile
```

-	Layers:
	-	`sha256:bb9c038cc3888631a43fdbc7e010e976f9087858498af6a86d7ba6bfa699ad66`  
		Last Modified: Wed, 15 Jan 2025 19:45:58 GMT  
		Size: 37.3 KB (37325 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:08a58c678736be91d24c9fcf88547df80f2db9d9b942746d2dea5b8402ed68c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187667954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93582ac127c589e4a8e700cec231304b999e81f43db92c816d052839341af650`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV LANG=C.UTF-8
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_VERSION=3.3.6
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
CMD ["irb"]
# Tue, 14 Jan 2025 18:28:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_ENV=production
# Tue, 14 Jan 2025 18:28:33 GMT
WORKDIR /usr/src/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
ENV HOME=/home/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_VERSION=6.0.2
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 14 Jan 2025 18:28:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 18:28:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 14 Jan 2025 18:28:33 GMT
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
	-	`sha256:ecd6d82d37c91c57f87e994c09fc780fdd9023894cb313d0b7626a5152633e46`  
		Last Modified: Tue, 14 Jan 2025 09:05:32 GMT  
		Size: 31.6 MB (31551742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f278262a5a4f300e678053b4c72dde4f771b93715e1c3e36d452f9e1a038d5e6`  
		Last Modified: Tue, 14 Jan 2025 09:05:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951a25530fa1185c4452419bc9effdb9a45ab1f4a363502c635033a8e8dabeab`  
		Last Modified: Tue, 14 Jan 2025 22:57:03 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8bbb1cc51db5ed8e7e768d343b2392f5d9770c0749c13c2207669e93f4d3bd`  
		Last Modified: Tue, 14 Jan 2025 22:57:14 GMT  
		Size: 70.8 MB (70778592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9d617145f57e90403b11b266d5e8609d67a971275db199b4024469c222368`  
		Last Modified: Tue, 14 Jan 2025 22:57:04 GMT  
		Size: 1.1 MB (1134858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3c4dbd52f242117e54353f55be951680f87df4fa2c3f6ebe8f1a238f132c27`  
		Last Modified: Tue, 14 Jan 2025 22:57:04 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8daba047c4624cbd1809844f5f016a99e4159981d259747b3145d34bb5cbb0f`  
		Last Modified: Tue, 14 Jan 2025 22:57:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d862a73dd41e4e57550c9618d58e804f9c33014518166cf186700db0863a7b`  
		Last Modified: Tue, 14 Jan 2025 22:57:06 GMT  
		Size: 4.1 MB (4060121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae1f92a38921dcdc25d5f2346cccc64de06da6da5366e89f9260cef53d99a2e`  
		Last Modified: Tue, 14 Jan 2025 22:57:16 GMT  
		Size: 76.8 MB (76767232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2621687e80da2882c0fba96bc57dd5a90f22a5f76a1956aaf75d967d6e95ed`  
		Last Modified: Tue, 14 Jan 2025 22:57:06 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:0bffc1a6f6eb64eac0ba1b26c7c92a57dcbb49680b16818f1c5d540a2a645414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5915bd7e064be982284103a4ecaee0f4bf58d83d5d788dc50c034a25ab2d8965`

```dockerfile
```

-	Layers:
	-	`sha256:55c41904af31d135946cbc59cc1c7d2699ca70214a239bd1c6f0fea5a29f8f40`  
		Last Modified: Tue, 14 Jan 2025 22:57:03 GMT  
		Size: 37.3 KB (37326 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:2d87296542d87acc6e440fb7e3b17b2acc70e688cf5f171367716ff72336170a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188462920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba52cbfc468915c7df19200a08163fb03d89b944db48ce495b361cdfa60e05b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV LANG=C.UTF-8
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_VERSION=3.3.6
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
CMD ["irb"]
# Tue, 14 Jan 2025 18:28:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_ENV=production
# Tue, 14 Jan 2025 18:28:33 GMT
WORKDIR /usr/src/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
ENV HOME=/home/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_VERSION=6.0.2
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 14 Jan 2025 18:28:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 18:28:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 14 Jan 2025 18:28:33 GMT
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
	-	`sha256:2a4818ffd0a142f338294aa16cd42434544b9a93fe6ca8f677bcad24e4bb461b`  
		Last Modified: Tue, 14 Jan 2025 01:53:11 GMT  
		Size: 33.0 MB (32985880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce84305028a132422d71bf0aad6081212eda806fbb732a2ba72f3a1746e0e74a`  
		Last Modified: Tue, 14 Jan 2025 01:53:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb44642c94290f53ac109914cb8c91bb072f985c06b048cddc8452d347fd77c8`  
		Last Modified: Tue, 14 Jan 2025 22:28:26 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e86d49dff59303b70f83b43f916cdea429f7c3ecb42e943fe34486332cc8476`  
		Last Modified: Tue, 14 Jan 2025 22:28:27 GMT  
		Size: 72.3 MB (72287188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4a909b8629e85836f82921f05016a0e92a1a2e6af30aeadc38e0e866132346`  
		Last Modified: Tue, 14 Jan 2025 22:28:26 GMT  
		Size: 1.1 MB (1131110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca53887c5b1e3d468e2a69c1409b999c09e0b880792d520afa311cacdceeef7`  
		Last Modified: Tue, 14 Jan 2025 22:28:26 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b0de9482fe179642506396df8353eb70844f7b9d5c6df156cbf90bc5087563`  
		Last Modified: Tue, 14 Jan 2025 22:28:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1522d9aba08ea8c15f2a6fde4024d26ba871084e1efbadce106cf6ffd4395b1`  
		Last Modified: Tue, 14 Jan 2025 22:28:27 GMT  
		Size: 4.1 MB (4060062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef7f93a22366639018a29b79c96c617862edc458431035732df2f5ac47aed2b`  
		Last Modified: Tue, 14 Jan 2025 22:28:28 GMT  
		Size: 74.5 MB (74531873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35653f00c0225800c347824f90903207121ddee5a18e2fbbd56665b4bcafa7a`  
		Last Modified: Tue, 14 Jan 2025 22:28:27 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:c71237350e5c660b37deee0e45a8278ed04229e5507f8149f563722c22a132c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea7a65badbaf81680f75c4e6d34f966f05c1e776a26ba89b841582882522d32`

```dockerfile
```

-	Layers:
	-	`sha256:c5ddf13af6954001f639f2721fe275e7f74b84e3e652a86925abd683832d7578`  
		Last Modified: Tue, 14 Jan 2025 22:28:25 GMT  
		Size: 37.3 KB (37272 bytes)  
		MIME: application/vnd.in-toto+json
