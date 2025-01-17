## `redmine:alpine`

```console
$ docker pull redmine@sha256:2f1ac3261b718143ed2ab129fb3221e3efda62bc4d49110113cb5658b8ce5dbb
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

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:f90908b5dcea9bbad4e9bf3177b50f0680e09d16dacc2883d1facfd3ffaf0f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190282762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f927814a48dd6671530d841a297c0699764564f1bcfbeb98d77db48a7b70dc7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2689193fd3b8bbec6b1235184a856cdc679d39b6df12595079b3094f23e4f0d1`  
		Last Modified: Fri, 17 Jan 2025 15:31:37 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf1e7cb121dfa9d44c0528c7f521644dc74d82ea755161a20e54c28b0cd2413`  
		Last Modified: Fri, 17 Jan 2025 15:31:38 GMT  
		Size: 35.6 MB (35564280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401fe1973e859999691905b45389e29e629d96490f733575f2508c688d01ac6a`  
		Last Modified: Fri, 17 Jan 2025 15:31:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e1e6acb668f2b422a57ac77dfbc4e97e2930aafa9da5578bc4d27dc351374f`  
		Last Modified: Fri, 17 Jan 2025 16:12:49 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6c6488e02ef077879e521ec5a7de76d6d7586605c8739041abee8f29cac7c`  
		Last Modified: Fri, 17 Jan 2025 16:12:51 GMT  
		Size: 72.3 MB (72286609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8348779e81a7a9317db7f7f43dc6c071da1b972c0c66b9d788d16736a5dea14`  
		Last Modified: Fri, 17 Jan 2025 16:12:50 GMT  
		Size: 1.2 MB (1168321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92113c2d5e4b9a6aac173edfd6d2ed722102648b9257a62e7371d3e92ed842d`  
		Last Modified: Fri, 17 Jan 2025 16:12:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdac836d2adc8254e1776cc379feea594cc9fa07a3de7061b2212baa59470ae`  
		Last Modified: Fri, 17 Jan 2025 16:12:50 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363d14e9f589f304f6d821ae633bfb4966fa19e98fbe434c32d55588e5c78ca2`  
		Last Modified: Fri, 17 Jan 2025 16:12:50 GMT  
		Size: 4.1 MB (4060070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1544c434da0a674a8724addca8f7220bad6865db85e9ce74e32f17333bdf36`  
		Last Modified: Fri, 17 Jan 2025 16:12:52 GMT  
		Size: 73.6 MB (73558207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d799f27c9bdc766cd57cff0b07f78e5422647600615d231374d25222a52f1ef`  
		Last Modified: Fri, 17 Jan 2025 16:12:51 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:b8e3780b196d4961d40a04ebee7b27a5d739ad3804c61f990e7a818a6063065f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 KB (38496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97f5a7e0c0edfed3446d6eb04d6ead25620c6b310943ed0d6489893c7647f09`

```dockerfile
```

-	Layers:
	-	`sha256:742c0b566ddf6992d6fb447900b5c0f5c1a881a72b5cc2ed3cfb6f23f59cc302`  
		Last Modified: Fri, 17 Jan 2025 16:12:49 GMT  
		Size: 38.5 KB (38496 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:4fc5d35381d7722014daf05f14943243d9560c68bb8f82b46551ab833e3a517a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182262420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d99d066dbff8a0b5ad18e40a0d8a4d14ebdedb8970249105487ce8e8f8f965`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10557ebb6bb2572adf43075a3e0ad01cddaa051ed1d29bae84c264720aa25c9`  
		Last Modified: Tue, 14 Jan 2025 01:39:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324b8b066ed61af7c11bf9d6828e24aa3d6c8a74e068910aa53d3ae7b64d915`  
		Last Modified: Fri, 17 Jan 2025 15:31:10 GMT  
		Size: 32.0 MB (32029071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa4505f7d3c506d6afa4c1bb1baa836a5d3e85036abed93e7407273f13000c6`  
		Last Modified: Fri, 17 Jan 2025 15:31:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612a7d4036b14808b34985a1a6b59a6bf67c8691899cb028f58df331e52df273`  
		Last Modified: Fri, 17 Jan 2025 18:12:52 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6c6d85b69877784cd9ef5fb2a526f655e2c01f5a3310e9832e043b6ef16491`  
		Last Modified: Fri, 17 Jan 2025 18:12:54 GMT  
		Size: 68.9 MB (68909640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015fce346ff8812829524a2774fb3893968240977654cfe60c9d5751bbc490e3`  
		Last Modified: Fri, 17 Jan 2025 18:12:52 GMT  
		Size: 1.1 MB (1134893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629bcc5db07e9baac3b91337e0c21dd5f916df168e8d3bc32f7ce43aa3f470b3`  
		Last Modified: Fri, 17 Jan 2025 18:12:52 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7519e389d64648cbcdaee9cc47dfa41f9f0f3447c4bfa42c29914620276ab01`  
		Last Modified: Fri, 17 Jan 2025 18:12:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6271309ee001b15e9a5465a1fbecf13ea702c4af36c730661cce862de43a804d`  
		Last Modified: Fri, 17 Jan 2025 18:12:54 GMT  
		Size: 4.1 MB (4060062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b478208198c1b8a3f8be7071b5a29b058a7d21812766922e458f1f763289f86`  
		Last Modified: Fri, 17 Jan 2025 18:12:56 GMT  
		Size: 72.8 MB (72761313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc0e48cacf03cc442406467739d5444e66f2406a69e35fdb778067693995216`  
		Last Modified: Wed, 15 Jan 2025 18:33:31 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:67ac1044115781c0d971caf7d7e1d0c5ee3471aa5994346157538e132afbf66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 KB (38669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43557a5851b9c5b40d357bc8b82452740d9e0bd3e5b2e12e9eb3f77a03207087`

```dockerfile
```

-	Layers:
	-	`sha256:2c36e0ae05c6276e55fe89fe46e1551e00ee8f357d8d64cc294a17923e5770cb`  
		Last Modified: Fri, 17 Jan 2025 18:12:51 GMT  
		Size: 38.7 KB (38669 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:3de8136a906c89200e6cfe03e9cc0e14d5902f330095772edd29617f0ea18982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178068027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b9723d90e4922d2bee8e6172af342d3ef2ca72679163a0e51e5b4ab8e6618d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380ab3ef7501f65bfd3ad014abb3f53ea3c8615b29785844d93b4f3e5c68eeb9`  
		Last Modified: Tue, 14 Jan 2025 01:43:51 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b29d41fa770498602d6e5dcb398af4e23586ff71a3e5829fb8f03de9ab63f91`  
		Last Modified: Fri, 17 Jan 2025 15:43:02 GMT  
		Size: 31.9 MB (31887989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ec807470d2780b1c6713fda72e5dc480f32c75386c38a76e7ec16126205803`  
		Last Modified: Fri, 17 Jan 2025 15:43:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c54ca59fb41ae506e203a2ab1c8e55801201bd1e4d179127fb3514af8a75b8`  
		Last Modified: Fri, 17 Jan 2025 16:15:49 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200bf152cb2298a9de9617e46668e63b61020871dcc57dfa478b2e157fd3eeeb`  
		Last Modified: Fri, 17 Jan 2025 16:15:52 GMT  
		Size: 66.1 MB (66095338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d43f20ce91efe07a5ab95a50ea1e9d2166321b309cfbd159025b05e966b93b`  
		Last Modified: Fri, 17 Jan 2025 16:15:50 GMT  
		Size: 1.1 MB (1134874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d088a1ead6aba1e2165ed38e35bffbc1ea569cf6c8ce0136fdbac94961e924ec`  
		Last Modified: Fri, 17 Jan 2025 16:15:50 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fccbef6b2fe36c290c33ab00a500934f2eed61ba8fb5851027245833d55871`  
		Last Modified: Fri, 17 Jan 2025 16:15:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6cc20f2c9d110208292a8195149a20f753537b7b57f2dd5611e9a72bd98322`  
		Last Modified: Fri, 17 Jan 2025 16:15:51 GMT  
		Size: 4.1 MB (4060102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fddb6b90dc71e6dd75fe57f561f464e8c4987078e2abe24f983cab973c15a1`  
		Last Modified: Fri, 17 Jan 2025 16:15:53 GMT  
		Size: 71.8 MB (71789047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592aa2b9daa1667e0c4eded8cc9a9dc336884397a25d540be60952ee1fb531c5`  
		Last Modified: Wed, 15 Jan 2025 21:26:03 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:3b82038ad64dce19ea664e943b73e393870869b824a0b85df722c43555f789c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 KB (38669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd0d94999347372264319316541a2cf03e82d8f50e346985d2563049e536f99`

```dockerfile
```

-	Layers:
	-	`sha256:c930b5a9e41134adfb19868efbf1ce5214c99cadc91bec1761fe1f4c8152cb9f`  
		Last Modified: Fri, 17 Jan 2025 16:15:49 GMT  
		Size: 38.7 KB (38669 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b544ee3099072c8d95f2b09591ba0483df1eecc37610703a35a95c8771fb5959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190166654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9acdb3db4d08e05e3e384cb8105e656218735ff37855d69791eaf9431be689c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2615d5d8dfa2981e23aba3f735f6fca0982072fd5c6a64920afc860d6226df3d`  
		Last Modified: Tue, 14 Jan 2025 01:42:54 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89eb1279f6da8f72ca379f3cffc3e45283b939d68c5e52d4f507ee633ef8888`  
		Last Modified: Fri, 17 Jan 2025 15:40:10 GMT  
		Size: 35.5 MB (35499444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63ccc6f74cb3e8d5e49e43a83d094dfcb5e28b806250731e9484f20312eec0e`  
		Last Modified: Fri, 17 Jan 2025 15:40:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a967daa05af70de552dc56ae6accae0ee8e1dcae7d249bf9616135780269c5a4`  
		Last Modified: Fri, 17 Jan 2025 16:18:34 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05e9c7e74237be0eaa9530ca979a6bc72e0a211554fe971d4b141373bf1c219`  
		Last Modified: Fri, 17 Jan 2025 16:18:37 GMT  
		Size: 72.0 MB (71967985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679bf7e7c8d2e35a05572259017fe8bc21b95040b921842963427fc10d768b00`  
		Last Modified: Fri, 17 Jan 2025 16:18:35 GMT  
		Size: 1.1 MB (1096382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f19eafbd8f141d54ef9559ac8de7ccf584fe6231c9e2588e4d8783cd7ac8d`  
		Last Modified: Fri, 17 Jan 2025 16:18:35 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b311e998c8b04a568d094ce436180a370e8adfe057cdee7b13fad068333b307e`  
		Last Modified: Fri, 17 Jan 2025 16:18:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348429b80e8878413250d19f6115d97dcc6f6ab9777c17790e38a2c781942e50`  
		Last Modified: Fri, 17 Jan 2025 16:18:36 GMT  
		Size: 4.1 MB (4060063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3bbf771f03e3460693e8c8cd2702940803db080ecdc02595277ca72c48805b`  
		Last Modified: Fri, 17 Jan 2025 16:18:38 GMT  
		Size: 73.5 MB (73546858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040e8532d344a026af7119405265ffd06513e54bae1633433244e79da5d247f9`  
		Last Modified: Fri, 17 Jan 2025 16:18:36 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:32ac5e2a9e8858cef063d7cce8e29b4ed21b0d9955b364093c6c4d83912589f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 KB (38723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f459c46d9a0d2ffa62b3d058bf7a2020a94e9aede19bc328d3456cc5a1fdc88`

```dockerfile
```

-	Layers:
	-	`sha256:2fea3defba8458a207029faaaf699c1a55728b718e54758290e6f8f236996917`  
		Last Modified: Fri, 17 Jan 2025 16:18:34 GMT  
		Size: 38.7 KB (38723 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; 386

```console
$ docker pull redmine@sha256:44864d8ee85af41d864529818a432ec212e299d9b08f7a8ae5f88be467018c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187213262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b608df7ffd1dea5af1621efc2f19d853996d3696940fef817fbd3c1d8c4e88b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87b3ffc935876dd520b2c2d83888b60d14c3035f727bf8c5da31188de160298`  
		Last Modified: Fri, 17 Jan 2025 15:31:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ae1c6768d2d4fe28cbe0650c118cd247c8aed4fc3e09419c55662921b3f14b`  
		Last Modified: Fri, 17 Jan 2025 15:31:22 GMT  
		Size: 31.9 MB (31906879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd067c968bb7e28dcb5aa8bf70889ae41d9e763b6c496311a117febc7e5384`  
		Last Modified: Fri, 17 Jan 2025 15:31:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0342dc0b7bbbf400fa02116962ec5de21ec68e98df366cf693edee07b86545`  
		Last Modified: Fri, 17 Jan 2025 17:31:48 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb3ffc1ff5b3f33a1cc2fb59ca8d2c884c1bdce4c8e9f9d9e5a6a321cc16e7`  
		Last Modified: Fri, 17 Jan 2025 17:31:50 GMT  
		Size: 73.0 MB (72966396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7b1e4d08fc99177363eb582369dc42ef23ee9fc5f2f30f8a5d785b60c925b2`  
		Last Modified: Fri, 17 Jan 2025 17:31:48 GMT  
		Size: 1.1 MB (1143561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c85c0f0cb52d8af31ed6fcd6d95c6c02b226276311ac8bfe33a15a034c4f622`  
		Last Modified: Fri, 17 Jan 2025 17:31:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a90695d60b80236c644c0c238cf2c1fe49655c4a88a61c6a6453cb9967b9af`  
		Last Modified: Fri, 17 Jan 2025 17:31:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ab1f07e2389ea2a78881fe6974e151677e1b951ee785075f033e2bfd3b125`  
		Last Modified: Fri, 17 Jan 2025 17:31:49 GMT  
		Size: 4.1 MB (4060089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223f468404275830d7729cff10c8feef670334bede80233c6c0f99d1d349841d`  
		Last Modified: Fri, 17 Jan 2025 17:31:51 GMT  
		Size: 73.7 MB (73669649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea07cc1f5e96a460730f892acc2a203ae17ea22f5f226316ab54c99bd6d93b4`  
		Last Modified: Fri, 17 Jan 2025 17:31:49 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:43a50ab3dd522dcdf86888103689d5b75666521a960c2149d02f22741251e089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 KB (38434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f05bd9c8f05adc980a7b72d56aef4efb4749a9f827fd0a1ea78d69038f7c478`

```dockerfile
```

-	Layers:
	-	`sha256:649483706119f5a1786a5b7a34925768990691d255ec99c33fafdb998180f058`  
		Last Modified: Fri, 17 Jan 2025 17:31:47 GMT  
		Size: 38.4 KB (38434 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:f3b81dd6dd290aec0999d669bbed6d9957458dd57136dc8e98e3709d69d0f847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191594880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60271c4d2fc83009289b21e3a0d5b84c8b9ea18e20ab15a49e280c602ecfb74`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fa082cf274421d4c78de9388c1d638ea51a72957cb0c9671c02d801d001eeb`  
		Last Modified: Tue, 14 Jan 2025 01:45:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7251e38138bd1f3b1d3b2da072adae772bf89b273de9339f680f1030b9630e98`  
		Last Modified: Fri, 17 Jan 2025 15:37:28 GMT  
		Size: 33.4 MB (33405632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0462bce97b5d820fa3dcc666d048d5571dc5a106ec92c01d355f29262667c398`  
		Last Modified: Fri, 17 Jan 2025 15:37:27 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7412208759ecb11d6433a116c8b842185b1a20946b365bd9a8c3f773abceed50`  
		Last Modified: Fri, 17 Jan 2025 16:17:33 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadd0fb0d5e4c401d8a0a4620643e69998f128b0fb9e78ed1a563b328734631f`  
		Last Modified: Fri, 17 Jan 2025 16:17:35 GMT  
		Size: 74.0 MB (74010543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ea61a5f7d26dad4da6e275a890989ea7fc8a88f2c18873d310333a3609d4cb`  
		Last Modified: Fri, 17 Jan 2025 16:17:34 GMT  
		Size: 1.1 MB (1086978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce08d8b96f5c756c289868563bb5815d8cfc96afffc62d6841d81771325da3ef`  
		Last Modified: Fri, 17 Jan 2025 16:17:33 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f652cf4ae3669dcdd93402dd0e51de71d030fbbba8fa4b69889ed0f59bd5e13`  
		Last Modified: Fri, 17 Jan 2025 16:17:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcae60803c9b3f55b1046232d4441756808c7af786c4218ebcdebb5abeb33740`  
		Last Modified: Fri, 17 Jan 2025 16:17:34 GMT  
		Size: 4.1 MB (4060104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77f9b383049914697d4d3bc26d6a7b4c128a371c4f991788974532e087c0ffb`  
		Last Modified: Fri, 17 Jan 2025 16:17:37 GMT  
		Size: 75.5 MB (75454461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25834e4f88bea46cc7e641994e4161612a683a23d811e4499f5f47bf2fecd9`  
		Last Modified: Fri, 17 Jan 2025 16:17:35 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:2bdd28eada087f61a44904b7ed3a248182e464ddbff7a5ce0d6ef9f2322fb255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 KB (38574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747eda11559e18aed81331dd8b6158c8108be30d6ec435d516c5da1950e6d76d`

```dockerfile
```

-	Layers:
	-	`sha256:6763d41702d643c00f7de88ac15c605b657a4c7e7badd74a926f03e145a19df1`  
		Last Modified: Fri, 17 Jan 2025 16:17:32 GMT  
		Size: 38.6 KB (38574 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:003890e610c6c77d82ea38b8c17744a7cfaa239db8575bd750c51845a0f9842c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193457989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77626a7d354273820c4f137ac5645780ff2743d8c818814ef00db1499b425c2`
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f58c5f1e872ea5fb6d2093f25dc7e3e4e42116a78691c8d841fa04894fccb8`  
		Last Modified: Tue, 14 Jan 2025 03:53:39 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292160d485fb77ae1c5fce43bf832a0b82d3435ebd5dae34de5300720e53cb35`  
		Last Modified: Wed, 15 Jan 2025 23:30:30 GMT  
		Size: 38.3 MB (38261721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dd5931746c60ba76d62703d4b24cc3aa7489f49dd5e33efadfe1864f23fc37`  
		Last Modified: Wed, 15 Jan 2025 23:30:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519f359faa955a13c1bb1be811fd340f124532b73e5d9859f5c08ec434e79d32`  
		Last Modified: Thu, 16 Jan 2025 06:16:55 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786618fc15b8c15412b8c0abf2c48715d50afe505d7368d1101702615a41d60f`  
		Last Modified: Thu, 16 Jan 2025 06:17:05 GMT  
		Size: 69.6 MB (69575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186aabfdf646a1c966ad4a92addc946420cdf441ffc21f7196c4fbd4f195dd07`  
		Last Modified: Thu, 16 Jan 2025 06:16:56 GMT  
		Size: 1.2 MB (1165171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07992d77acb6a0a02fdc35aefd9f8b0df8ca00a2a8ef8fe40639a1c81acad6ba`  
		Last Modified: Thu, 16 Jan 2025 06:16:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4961cf835d4c860bc6f34da1c7e0ccf0a8ab6d3c4338f866971943cb16c53e15`  
		Last Modified: Thu, 16 Jan 2025 06:16:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440b164b6836f73a30fe07d48fc00a587f7864c5f926c7d764ee7f605d4fac8c`  
		Last Modified: Thu, 16 Jan 2025 06:16:57 GMT  
		Size: 4.1 MB (4060085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3035d783a60ca1c0397c45f5dc6e4379ec20b32dc5bbfa9606502372a1cb7b`  
		Last Modified: Thu, 16 Jan 2025 06:17:08 GMT  
		Size: 77.0 MB (77041878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec4f2fc85c4476f2995837f2d36f1b27b606b6ce51a7d2f740308a0d44db5c4`  
		Last Modified: Thu, 16 Jan 2025 06:16:57 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:ab2d399f0dc004149bde103904d05c08d9f073ccb99cae999c144de2bf7713fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 KB (38574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f7cdb24608622b3766dab61bbf4a4a505d685c98807b6e8b14538fc5aa8a2c`

```dockerfile
```

-	Layers:
	-	`sha256:b3b65b3842b1763d2fc15c80478a5723894a936b778476b55a36e70b3192e36d`  
		Last Modified: Thu, 16 Jan 2025 06:16:54 GMT  
		Size: 38.6 KB (38574 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; s390x

```console
$ docker pull redmine@sha256:eb7535b008dd61c416107864a4a3505a00af49dd38c223218609905f06744fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189604981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d747ab77309f931bc200c070273445e0d94805944f629a44fccf124731bfcf18`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 00:26:19 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 00:26:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 00:26:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 00:26:19 GMT
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715918f0e770587d15212ec4d7b5b9eeb1c07e9bf7a302047dd6fe58fe3efb9`  
		Last Modified: Tue, 14 Jan 2025 01:43:54 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3db0e0420c3ef69104213a22c89b6600ace632ea098809412687982d7c0a386`  
		Last Modified: Fri, 17 Jan 2025 15:37:48 GMT  
		Size: 33.2 MB (33193630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f516fb2c4ade68f6f1b23eafa90efa93c3e061f4ad6a151256460c3ee8b2340`  
		Last Modified: Fri, 17 Jan 2025 15:37:48 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259dd8a333ca6393209b8de84fcaac7176e67f2d1fe9dbe875d70ca3b0b014ca`  
		Last Modified: Fri, 17 Jan 2025 16:13:30 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeba5801faa31ed44a48955548f181c8c8121661be9ee46ad997bce20c69af39`  
		Last Modified: Fri, 17 Jan 2025 16:13:32 GMT  
		Size: 73.0 MB (73029433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d54de8f871b550c1123d402c5d888481c6efd436b8bbf68a3ef9424de587e2`  
		Last Modified: Fri, 17 Jan 2025 16:13:31 GMT  
		Size: 1.1 MB (1131716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88aca076fdf129897bd87daf56865bc337ef792f9feae6937632fbc83835745b`  
		Last Modified: Fri, 17 Jan 2025 16:13:31 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f586e6253d4f695fa7dd8d4df7add3a95ce8ba3f4164d09448f6a9a8132e592`  
		Last Modified: Fri, 17 Jan 2025 16:13:31 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8047f2d214b3a2ed5926b7b75a4f4581e14a2f8dfdb7225f06d10d3b10e79304`  
		Last Modified: Fri, 17 Jan 2025 16:13:32 GMT  
		Size: 4.1 MB (4060060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69671203965a202aa84fbb8f32385aabf6d75508e21d00eb9cbfd7f3285ea058`  
		Last Modified: Fri, 17 Jan 2025 16:13:33 GMT  
		Size: 74.7 MB (74719710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45425a42e64e2faa9e82fee79f7e2bae3e8541047728ce7d6c476c29ac965877`  
		Last Modified: Fri, 17 Jan 2025 16:13:32 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:d41a1281611cf24cace6c8cb3e2b61e9e0b866d0bd6eb8486d637bfa577c01b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 KB (38496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8533ab3d81328fdda5e714dc3c2c44e5dc53b76c3393061cf820c26612da32`

```dockerfile
```

-	Layers:
	-	`sha256:b4b232b59532fb716af8add8b7ec8e0abb95adc3ea7937ba74dc00682a4e8de4`  
		Last Modified: Fri, 17 Jan 2025 16:13:30 GMT  
		Size: 38.5 KB (38496 bytes)  
		MIME: application/vnd.in-toto+json
