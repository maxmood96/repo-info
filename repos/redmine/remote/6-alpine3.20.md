## `redmine:6-alpine3.20`

```console
$ docker pull redmine@sha256:0ed75075d3574749d8e13eacf3878965c665fdd4b58d30642c0f505c29d9c10a
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

### `redmine:6-alpine3.20` - linux; amd64

```console
$ docker pull redmine@sha256:803afa03a60dc3015d42e8d7d7ae7b4161407c1bdd847015fd1a2c769d9f3a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187952895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d323ca98afd38edd36d95c128d881ee2fe6c5a8cea86c9b1315ab0c92f00eb5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f712847978a47d97ec7e09731e94eba221f1944257e2193b821160ff5582fc24`  
		Last Modified: Sat, 15 Feb 2025 03:09:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b55737f83481fa74a2ab763cdd22d6ad084937b38e0c7059c98f0b3494920d`  
		Last Modified: Sat, 15 Feb 2025 03:09:49 GMT  
		Size: 35.3 MB (35287514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a7222998cec8eb73851fbb8fb7b25bf14f24431a832736479bba606173a211`  
		Last Modified: Sat, 15 Feb 2025 03:09:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17658edcfc6f466705133f89d93d84d5fbc6986d49e46212878909520a02aeb4`  
		Last Modified: Sat, 15 Feb 2025 05:51:53 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d5e34ed0f4d38be1f3bdcde753ff97a79e20b59da51b87885389dabd1988e5`  
		Last Modified: Sat, 15 Feb 2025 05:51:57 GMT  
		Size: 70.4 MB (70398920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8495283d13363d0e9cad77bd0bc932a6ed422d4035ccd03a23bfa9e68658c8e`  
		Last Modified: Sat, 15 Feb 2025 05:51:53 GMT  
		Size: 1.2 MB (1166462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0702ee1980b716d025641e8b55817dc777750e853e1bf0dc82554b93d1315827`  
		Last Modified: Sat, 15 Feb 2025 05:51:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c5ffbfbbf507c84c061d3a08373498b050c698d763e8c55469815217b31fda`  
		Last Modified: Sat, 15 Feb 2025 05:51:53 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11255b455b575f9e5f0e87aaab4f304ea504b4fde24d519e569be2e37464d8a4`  
		Last Modified: Sat, 15 Feb 2025 05:51:54 GMT  
		Size: 4.1 MB (4054634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb067c89f40f86ae78706924fd541a71e7d992fc85774bb88b896a08c1d90617`  
		Last Modified: Sat, 15 Feb 2025 05:51:58 GMT  
		Size: 73.4 MB (73414651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c506140b373bb1c0a8bbcea7aa6152ef33af47e5108573f946a68f8103ef68b4`  
		Last Modified: Sat, 15 Feb 2025 05:49:46 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:cb4b5f7bfe9b4554ef85bc7435c3553f719c73d0d22ff70a853320621a795022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2468fc8f882c4ec90c30ff5b4853a682e9d24aca50cec18c274cfc8e3e0153`

```dockerfile
```

-	Layers:
	-	`sha256:eb85438681bdb6a6d933b4018e2523428b075e61e03d63e66bfa2057d88bdc9f`  
		Last Modified: Sat, 15 Feb 2025 05:51:38 GMT  
		Size: 36.8 KB (36792 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:aadece197d57eace59ef4703c4f2bd1aa49f76b63a1f7fa94d01c1d2a576b775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180215780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4fdcb3ba3f3b988f88b95332f2d73bc4d46b2577edaf0e0a65ad377a798790`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c33e30311f7bfd2e574783afd81b2b022925223ace47a3475b924f32b157bc`  
		Last Modified: Sat, 15 Feb 2025 12:58:07 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902f463c4a9aea5ffd81e51085579bf943c7e7f2f6e25aa12add73afc08776f9`  
		Last Modified: Sat, 15 Feb 2025 13:02:02 GMT  
		Size: 31.8 MB (31784384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaa33923fcbdd9b0af3d9b28f694afd0fdf05fe53f0ed063a9b407bac1149ad`  
		Last Modified: Sat, 15 Feb 2025 13:01:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc1eecb9aa730622490be7ef493264e2c0b028e0a664a0761df760b5d68070d`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b90b39d1893346eb01d79f4b86008e6f2eacd07fdca15c9e9356f39cdc8917`  
		Last Modified: Sat, 15 Feb 2025 14:52:04 GMT  
		Size: 67.1 MB (67141578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2c246567b69c6fd0db2f5fa13d90257a36b4e91512ab1b8c6bcccb826c2802`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 1.1 MB (1133511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8defec96f09aa563486f38c93dad06b9c05091ae28c5a6f74842dda43001909`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5761ece2d4112a91a82562af84528f851676a50cf6f8bb417fe1ea51e82b237a`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e136e2a3a5597c7ef37b0be24e7ab0838eb9694f3f3dcb481d5718356c90f1ad`  
		Last Modified: Sat, 15 Feb 2025 14:52:01 GMT  
		Size: 4.1 MB (4054562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a417896cf2346e078357627e76cc6b5fdc07ed52b22dcabb3bc5b5a863f30e52`  
		Last Modified: Sat, 15 Feb 2025 14:52:05 GMT  
		Size: 72.7 MB (72725395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c016acbf22f40acc120be0b3515cb386dfdc9f62f09483b996e396c9cfdee9`  
		Last Modified: Sat, 15 Feb 2025 14:52:01 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:fcb2f431e5409f29affa0a60dc795ad135fe9173df316abe92f6887ecd70003d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0387eced1a9c560ba8cf74e166b547020f5bd35504ea90ba165826066fe80c4d`

```dockerfile
```

-	Layers:
	-	`sha256:e92d69c29bd34f5b2e98ed4f003648b2b511e89dff9f6ea4d441d4a84f2bc7ba`  
		Last Modified: Sat, 15 Feb 2025 14:51:47 GMT  
		Size: 36.9 KB (36933 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:80eb6bd83bbcdd9a56b1104ed4fd7cdacab89a68fb75fea51bbde2106569cb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176067253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ca8a5ffbdba8f89747b42c1a074e1d3fba0d4206e5522412a69d436379aff8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
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
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799e57590c350f854e3f043f25424960a35650d3b131e18c9cb90402ce911024`  
		Last Modified: Sat, 15 Feb 2025 20:49:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c3db92d3cb7bd38e0475467920f10bbf740d5b9cfb7c7b7f473965a1c80ed`  
		Last Modified: Sat, 15 Feb 2025 20:51:13 GMT  
		Size: 31.6 MB (31599489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711d62a2368b81c36686d988db2275e9a2767fc31111e524363fca340850fb0`  
		Last Modified: Sat, 15 Feb 2025 20:51:09 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdf9a6b1540c7cb650161fbf2ea9d4a378fb1592da60060cca21379e1bd80aa`  
		Last Modified: Sat, 15 Feb 2025 19:01:40 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41990a91a1d641fdc7ae7c16b698f7f085ea085f3ea2379a2f30873f3e0a7e1b`  
		Last Modified: Sat, 15 Feb 2025 19:02:00 GMT  
		Size: 64.5 MB (64472215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c649baa0d6e2dcbacf8f1e10f78b13223e1091adde471b22a6155e09a5ebcd3`  
		Last Modified: Sat, 15 Feb 2025 19:01:47 GMT  
		Size: 1.1 MB (1133486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a1aa52f14f2c9b29faedfef9bf3af013a4a59e4c12987afe173547480a4fb9`  
		Last Modified: Sat, 15 Feb 2025 19:01:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915eb0bc08a5616dca10c1057efec9732caf667c329561cbb445e72646592ec0`  
		Last Modified: Sat, 15 Feb 2025 19:01:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cc8a7bef0ea7ce1924945b44c13b8fad91d862e2f0c0d01895b8a0edefae41`  
		Last Modified: Sat, 15 Feb 2025 19:01:55 GMT  
		Size: 4.1 MB (4054569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb26c08bb6a3fbab419d665e9a33f04d4fae3ead39d51203982010c7d63d945`  
		Last Modified: Sat, 15 Feb 2025 19:02:10 GMT  
		Size: 71.7 MB (71707708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f561d5f2c993b9287f8f70c4717107b0fd5ed04dc1e04b5d677ba0a42b9e5d`  
		Last Modified: Sat, 15 Feb 2025 19:01:51 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:7957d7fe38de3b2357de49a44ccb2e67e5b8c84e5c13d290db5d08938f6fb6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba2fae9fed8b51770718d5947eb91c525397e32aa44e150804f5df3087bcc9d`

```dockerfile
```

-	Layers:
	-	`sha256:a7e73dc075be1673f94bd7ba98df9e2e4e4c03cc4373993c3d1ff9470c192adf`  
		Last Modified: Sat, 15 Feb 2025 20:50:55 GMT  
		Size: 36.9 KB (36933 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:8bbf7f010d76b4c9b2cf7c149649f0a0d07fc72b7ac7d28acc4e205a5b6f592c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188874352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92207cb8dea191393b6f7aa19d86876ca55595b3f3d478c6b65602d6eabbc9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66821f213e2071472f4c29c4b6c7310a5d934f9d4ecf3ddaa6487a2ed00afc3`  
		Last Modified: Sat, 15 Feb 2025 13:00:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f0ac8517929d07bf85291c2a6aa8d8964afb6955b48ba76bdcd381e2b9f83e`  
		Last Modified: Sat, 15 Feb 2025 13:35:25 GMT  
		Size: 35.3 MB (35269320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0716f77f137277988b479bf9011de2a7458892db6217a33d730ac64ade59ce61`  
		Last Modified: Sat, 15 Feb 2025 13:35:23 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f341d95ea7754b0689763978ac98d950409e3326793bb6ce6bce440adffd8843`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5434d93ed94bdeac5dc135b0751c72e4b6e27e3497f464ea3de219a9fe5c3768`  
		Last Modified: Sat, 15 Feb 2025 14:52:08 GMT  
		Size: 70.9 MB (70881912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9906e3f9cf5d7c97547a03e58e7e884672451eb546784ecc8ca2b70a6c31ef`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 1.1 MB (1093087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72606c5343f5e5bbc8f2500dc132e333b922843fd9b157889a8a615a4372d897`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a97064d70b51bc4c9e35c682b2550f02c0ecac777671bf3c74f2d24a50ddd5`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ad820169aa17420c04f328a3f2182e953aac83a5d83a715b8fe89ed66c5d6e`  
		Last Modified: Sat, 15 Feb 2025 14:52:01 GMT  
		Size: 4.1 MB (4054568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f25030470fc0d723ce95f81a716dca8f55f10cfe488c845fd728157b344c49`  
		Last Modified: Sat, 15 Feb 2025 14:52:05 GMT  
		Size: 73.5 MB (73480486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353d3ef77c0d5fe9a652bac65ae21b9eaa48e2b4215602c1a1533a110ce26d04`  
		Last Modified: Sat, 15 Feb 2025 11:59:23 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:175363b5ca55f553e0b134f84b163407c9f34bda1241034f7d91e8cd3c824a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad78800cbcfe25407240fdf7c10b3147c0b6acd0eeaa79dc8f3a0add7cef0a08`

```dockerfile
```

-	Layers:
	-	`sha256:5db5045a5c970eb8e1b05241b1b0e3e84db31198c1ff3c01185b4f52b6323af3`  
		Last Modified: Sat, 15 Feb 2025 14:51:49 GMT  
		Size: 37.0 KB (36971 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:89eceb1b2fe2f84f88ef4002929d357c170b517843a32d5817390ac8f1b8755c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185041086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e260c5000d46f306484a39328d5a8e423b273bfd7e4684b7a586c61c5d4b6f52`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
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
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0825e7a3fae7960eddbfbb85f43d3e34787bd0d475306f7fccea1f34da077fd7`  
		Last Modified: Sat, 15 Feb 2025 03:09:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139307f24eb5ea6604afa62fd213b43961c70e307ca8170272b25c990776fd78`  
		Last Modified: Sat, 15 Feb 2025 03:09:44 GMT  
		Size: 31.7 MB (31663662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fb09b2e207a57a2128deb769404546ba9c6d181e198c55480fb36918d1e204`  
		Last Modified: Sat, 15 Feb 2025 03:09:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12c8ff8964d1d22e1b089854285b022f7e53228a38e48f6e4f1fee54041270f`  
		Last Modified: Sat, 15 Feb 2025 05:51:53 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b144b054477a8e787e45d65483c2b123f97f881c9185f1836eb3a1ee617a18`  
		Last Modified: Sat, 15 Feb 2025 05:51:56 GMT  
		Size: 71.1 MB (71135252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f3992fc1f650d0c1df6f3e542b3a483e5f7da4da5bb912e3b681ae2d79bac`  
		Last Modified: Sat, 15 Feb 2025 05:51:53 GMT  
		Size: 1.1 MB (1141399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caa71a2dae7655e6b23645474c3efde538d789ff53ed1a4a31ec182bfeeb002`  
		Last Modified: Sat, 15 Feb 2025 05:51:53 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462a929bd8521eb1ab8e76123d217acc2304e47cbb584179404ed7dc9ba8ef30`  
		Last Modified: Sat, 15 Feb 2025 05:51:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afce56a95f317a81b83221370b239b336c221c23c2fbdeba6486d0bce4a15ee0`  
		Last Modified: Sat, 15 Feb 2025 05:51:54 GMT  
		Size: 4.1 MB (4054574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1131645c09e3ee349d8cc4b376de59b307ddc84b9c369f7f6e7919ed6396cf`  
		Last Modified: Sat, 15 Feb 2025 05:51:58 GMT  
		Size: 73.6 MB (73570711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e7661ddb21bd1ba66fa6a0496a5db694435e64951f104b3ba5ff307e326321`  
		Last Modified: Sat, 15 Feb 2025 04:09:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:8c3fbe42f45f1c095a46943900aef3a77baafa5f69da515b81a6fd4e174cfc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfce9d194bc3baa343657d22af01db9729faaf2b91760db9aa0092f4630a5a4`

```dockerfile
```

-	Layers:
	-	`sha256:319741e3c0bf99f5b47f8097f08171974a9f83a5b084d786826db637b89185c5`  
		Last Modified: Sat, 15 Feb 2025 05:51:43 GMT  
		Size: 36.8 KB (36750 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:07991ee1abf73efdcd1b2c73817ab19c00e76b5c15a6ba025ed62c97dd99a8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189344239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac745dc31f948e746da233f8fe8dc5db539b1f07d9694cc7bc00a1a39ee27b0e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
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
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e852b146a20983addee8d631674affb3933753f57b053982007590be27c65f`  
		Last Modified: Sat, 15 Feb 2025 11:49:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b18e0bbc801378f83931d03c3a5a1b443fbfcb8d8728d18867fed2d396dced`  
		Last Modified: Sat, 15 Feb 2025 11:51:03 GMT  
		Size: 33.1 MB (33144717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7324f04ce44898228dcd919546db5d9a1dbc56bd8f243f1cfe44d818f4f9acfe`  
		Last Modified: Sat, 15 Feb 2025 11:51:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543ad534f0da94e2f8623edc0d685c9eba7dfb35ac01115ce24ea9d139486c9`  
		Last Modified: Sat, 15 Feb 2025 11:51:02 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555476562963fd71d66c886f199a967329ac883bd63c0e960dd04825ad30d36f`  
		Last Modified: Sat, 15 Feb 2025 11:51:06 GMT  
		Size: 72.1 MB (72118501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856cf9d9df722be178392ea70f5671307a98f599b8a67d4c4045f2e255e601c`  
		Last Modified: Sat, 15 Feb 2025 11:51:02 GMT  
		Size: 1.1 MB (1083748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db37b35dde3af8300505d772fd84add52c170fbd43c61659c76510567e8d3eb3`  
		Last Modified: Sat, 15 Feb 2025 11:51:02 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee2528c479da7da10c5c10a1757f5ec4ddfea706a0ec5f50492c38b2a5271c8`  
		Last Modified: Sat, 15 Feb 2025 11:51:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe8d6c9a5bbcb43643a03a2f08c02991fe63956e34763d523c8060a6feac5ca`  
		Last Modified: Sat, 15 Feb 2025 11:51:02 GMT  
		Size: 4.1 MB (4054579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dfc41272243d466605e229fdc8bab66e283eb23b32f1eb0f462d47c92a912b`  
		Last Modified: Sat, 15 Feb 2025 11:51:05 GMT  
		Size: 75.4 MB (75363197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5ed157dcc3590fa2c964dbf80203cd96faa51e4d58959e1dd8a326b3465ac1`  
		Last Modified: Sat, 15 Feb 2025 11:51:02 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:fdef991b99bf5a6887b026bb39f1f6b352fc08ee7c4943456930fb9e575f2aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0dbe9983607362811bbd82397486e24c259a8f274f5199cbbd7025dccac4f7`

```dockerfile
```

-	Layers:
	-	`sha256:92183e72269fade8f698e7e6dc026b91f8d9ed6e171784da30302e4eb4e5d3af`  
		Last Modified: Sat, 15 Feb 2025 11:50:53 GMT  
		Size: 36.8 KB (36844 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:acc1b4918628a7eb15f53f5a52c96d03204da37f25ddeefc399260c301a950d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187725156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c9f8ca5c59aad640f20dfda2ab22efed686f737359fc2220e033973978576d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_VERSION=3.3.7
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Wed, 15 Jan 2025 12:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 15 Jan 2025 12:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Jan 2025 12:03:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 15 Jan 2025 12:03:22 GMT
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
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
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
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb69847f873261cc901364c6e5453bc8ac36796ac8944ffe1685a0c21d2a1f0`  
		Last Modified: Wed, 15 Jan 2025 07:32:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703b13c3738bcfad450312b6c3271d13582ed04a28739b68831f26b53ebd99fa`  
		Last Modified: Fri, 17 Jan 2025 18:26:13 GMT  
		Size: 31.6 MB (31552550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e3724aa281a150ca69aee1f729479410507f445405497dd77a4e15000217e1`  
		Last Modified: Fri, 17 Jan 2025 18:26:08 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a688d6e86b02c1b5abd2145297bad6a85fbd9a5caa82212e113aa9b817b94b2`  
		Last Modified: Thu, 30 Jan 2025 02:21:33 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff714b843434edc307b7658a382a59195576f1cea29fa4450ceeb3f2e190782`  
		Last Modified: Thu, 30 Jan 2025 02:21:43 GMT  
		Size: 70.8 MB (70782375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05105281b11d349fd238aebe1dbd8e7caa4049132f5ae922b88329f5c6c0cec7`  
		Last Modified: Thu, 30 Jan 2025 02:21:34 GMT  
		Size: 1.1 MB (1134858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd69d37c5e50437d33b0770f5187e8f393cd990d0dae33016d487f4611cd946`  
		Last Modified: Thu, 30 Jan 2025 02:21:34 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22deeeb2a2ca9ad31c23a397a3654bf0fea2ebef5e583b5f75e6e630024aeceb`  
		Last Modified: Thu, 30 Jan 2025 02:21:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09adb05eb69839e686975fd18569a1a6290c157663accddd9608a7a2bdc8ded5`  
		Last Modified: Sat, 01 Feb 2025 13:09:29 GMT  
		Size: 4.1 MB (4054589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4814065e3242f3b30efc824665be1ea837e98b36373540a4a36da9975aefde71`  
		Last Modified: Sat, 01 Feb 2025 13:09:41 GMT  
		Size: 76.8 MB (76825035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5951765f5a54be66d36c26cd7b5732ae73dc23e170f50ceaca7774b73c1976c3`  
		Last Modified: Sat, 01 Feb 2025 13:09:28 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:dd729e1045dfd03c4298b19b81225f515497e4d3a61f8eb491caf9cdd4afeca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a6dbe447f5c1f08cebc5da3c49bba7a90a145a4be0c0fc26227393502d7e42`

```dockerfile
```

-	Layers:
	-	`sha256:a79f96814bedcf5bd342faad7cfa3f41ade66edebc09ed79c28867554f2fb680`  
		Last Modified: Fri, 14 Feb 2025 23:50:56 GMT  
		Size: 36.8 KB (36846 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:5159fd19c25937a7f2d33d9e0695571b9bb4dd0d9bf10209e5588a8e3554e44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188524605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c9a6ac609141130cdbca6cd530ef42308332d071e8342fd1115fb59c217614`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 31 Jan 2025 19:49:37 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
ENV RAILS_ENV=production
# Fri, 31 Jan 2025 19:49:37 GMT
WORKDIR /usr/src/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
ENV HOME=/home/redmine
# Fri, 31 Jan 2025 19:49:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_VERSION=6.0.3
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.3.tar.gz
# Fri, 31 Jan 2025 19:49:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=48a139e9416f97922ab48231912fed8aa4c48d4a96b8f507124b11e4335218d6
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
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b006249d95e84161a990851d62951b31901f108373dcad021480ecc86230e9`  
		Last Modified: Sat, 15 Feb 2025 14:50:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd88ab3575d8aded6876be52b070251e0d4a7a0cc6c6e54b95888edd687eceb`  
		Last Modified: Sat, 15 Feb 2025 14:52:01 GMT  
		Size: 33.0 MB (32987627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0375b248d72681774eb9738b3ba7c528e5ebd5f132ad434f342ed949b772a`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85f2396151d9512d276f943d9e84b38b49f56ec09691b9d9f79019feb1ffdcf`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4697b703a8caf0482b6d6f0114905cc00d0d4996ff5909ff36db1eee41b9ae4`  
		Last Modified: Sat, 15 Feb 2025 14:52:03 GMT  
		Size: 72.3 MB (72285867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad508336e18eca6b3a2aa062d5b0fd71d4ece2dfebf5f80cbf5d2c127c863c14`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 1.1 MB (1131132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ba38efa2ca3a5a3d52d82178c90f0e8df21e8caba54fab596c18c7351ab1fe`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311b48ed2640f4930b244c1057c4d608a8f8c2ab836e528e2f791cde2cc7dff6`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e52029ca43a6be2544e06816ecdbbf456e2a664e28fab84b34a4ad8d0be5634`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 4.1 MB (4054579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae849d883e596ddc81f107f3c9a52221e4b5584569ba795d3990ed6ce1135b7`  
		Last Modified: Sat, 15 Feb 2025 14:52:05 GMT  
		Size: 74.6 MB (74597459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64707296165c3268a2c558f038ec0515a58480401c769408142ed5dfcdfb5831`  
		Last Modified: Sat, 15 Feb 2025 14:52:00 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:52104928d2d626c5c5ba9c37946a531a491df4e38026a09be3c90fb52949ac9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52d63e704fda5cdf8edd98aa9a203118121a33c8c93667a4f6271acba49c189`

```dockerfile
```

-	Layers:
	-	`sha256:80cbeefafc6becd114173cfa52d896539ef28416e14327463881ce8fdab5e072`  
		Last Modified: Sat, 15 Feb 2025 14:51:53 GMT  
		Size: 36.8 KB (36792 bytes)  
		MIME: application/vnd.in-toto+json
