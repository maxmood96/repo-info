## `redmine:alpine3.20`

```console
$ docker pull redmine@sha256:880090ded509024a793f9b07fc2642887859cfc627762d8d18f4d29dc45bf48e
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
$ docker pull redmine@sha256:03300092c674fba314c15d13303bc61528a9f19a8fc4a2bfc91efa73d79523a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187900997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6135b17a3dc24ac233ac54ce71fb84450c4a8326db33c1c20535458729b7bdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
# Thu, 23 Jan 2025 00:31:52 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_ENV=production
# Thu, 23 Jan 2025 00:31:52 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
ENV HOME=/home/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_VERSION=6.0.2
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jan 2025 00:31:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:31:52 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 23 Jan 2025 00:31:52 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af9c474b1fd911043d5c0089a9b2dce8b573658542791aeeb75b0b028d48395`  
		Last Modified: Fri, 17 Jan 2025 15:31:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bd4b4e7686c356482cbd8bd4d6cac57b05a11b30f5397850c8ce966564c962`  
		Last Modified: Fri, 17 Jan 2025 15:31:37 GMT  
		Size: 35.3 MB (35284503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a356c0021182c48aaea4a6fa39834747cd22d62fd5604f7654cf9852a0d285`  
		Last Modified: Fri, 17 Jan 2025 15:31:36 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fcccdab922661d30417ba29bd90d5e75a0902c346adc42838c363c2f791993`  
		Last Modified: Thu, 23 Jan 2025 01:31:37 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778babca2ab92a60fb4de4e4e1d5df864c6f0cc67942df1dbdd5324a56ee260`  
		Last Modified: Thu, 23 Jan 2025 01:31:39 GMT  
		Size: 70.4 MB (70389195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52e3170107177c3a8e4f29956b7a38f514542ef33e76ce985018ebeee52635b`  
		Last Modified: Thu, 23 Jan 2025 01:31:37 GMT  
		Size: 1.2 MB (1166441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c30f8d6a7711f7ab687879c06d8d8ac57adfc7fb99bdff2207095de38bd4613`  
		Last Modified: Thu, 23 Jan 2025 01:31:37 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092ca48a5a23b289046d90dc7b10bfb7af21517373669cbc8808acad8444f09b`  
		Last Modified: Thu, 23 Jan 2025 01:31:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8315984ad1ebe0bce983557ad337270ad87df46f5a45f2c05e017dfa305f604d`  
		Last Modified: Thu, 23 Jan 2025 01:31:38 GMT  
		Size: 4.1 MB (4060070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b70625dc365a169a8b8b05f0565e7da16300cc5f984209cb51a8e75937895c`  
		Last Modified: Thu, 23 Jan 2025 01:31:40 GMT  
		Size: 73.4 MB (73370709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373f85969394837248a96118d2d56adac6dee418fc743dad3b22e97e454c2eb`  
		Last Modified: Thu, 23 Jan 2025 01:30:43 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:a23dee016c57b3aa95c9e03f5ed8e19315b7b010de6359ea51939c358e817ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2279a9ffbe77b8627362635cf178487d575d4b2f20a8a30a76659c4d7d176e8`

```dockerfile
```

-	Layers:
	-	`sha256:9b99dddb43e3d528266df3b14c7d2840cc48dc09db521b7948848fe307c991ad`  
		Last Modified: Thu, 23 Jan 2025 01:31:37 GMT  
		Size: 36.6 KB (36592 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:cd29d663195feda701ed73b7f29e11983a1adcd51132a80edb8d021d46683b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180132525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14274d9b82321e5deed0e4ad5ac4f261abc890af3eb8cdc4ceb72822159226cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
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
# Thu, 23 Jan 2025 00:31:52 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_ENV=production
# Thu, 23 Jan 2025 00:31:52 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
ENV HOME=/home/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_VERSION=6.0.2
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jan 2025 00:31:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:31:52 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 23 Jan 2025 00:31:52 GMT
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
	-	`sha256:7746f5356f4d806184842c20dab2f7db298a72c7e16a631e5490bf7734f2074b`  
		Last Modified: Fri, 17 Jan 2025 15:34:13 GMT  
		Size: 31.8 MB (31782519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a670c2951bbf62896ac8e40687939f687043457bdedb36c6ddba4921455f7255`  
		Last Modified: Fri, 17 Jan 2025 15:34:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d67edbd50a84e4ee4106bbed5e12fc8bcf1e4883cc399f2689daf62066aa21`  
		Last Modified: Fri, 17 Jan 2025 16:15:44 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53094262ac905b0e6409c315de5666e068d51ef70419d1c2b3e7f9d9006528c`  
		Last Modified: Thu, 23 Jan 2025 01:51:37 GMT  
		Size: 67.1 MB (67117332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b557630f92665f49dbe73b678ebd08c0b505d4d51fb5606d2d4a37e8dd9526`  
		Last Modified: Thu, 23 Jan 2025 01:51:35 GMT  
		Size: 1.1 MB (1133487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c598fd9b3df764975b2086b7022d33034d9e9a14de1ed5f5d0fff7c4adf7b5b`  
		Last Modified: Thu, 23 Jan 2025 01:51:34 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3b2630ec4e53ccae5e82a2e0dd67a841ad0b9f0f10db98ff3f1a4b49bceda2`  
		Last Modified: Thu, 23 Jan 2025 01:51:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820b8cc731d8e476a9a03494783c05701ce861aa32599622a52c9a5c3147c1aa`  
		Last Modified: Thu, 23 Jan 2025 01:51:36 GMT  
		Size: 4.1 MB (4060083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa8a1eeb10cd4ef129cc70e65df9ef42cd1b3a984b79a9a5b5a0f36c3f1bf49`  
		Last Modified: Thu, 23 Jan 2025 01:51:38 GMT  
		Size: 72.7 MB (72663817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f999f4027d37aebce4f93764f9e36c6793991ae0d76ff39ee085768295df2a4`  
		Last Modified: Thu, 23 Jan 2025 01:51:36 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:f94624b33e7eb039e1c3e19054e5d1cd4cdc4b8ebec40e7a5e0a6e07defc33a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bc74f927629a4867e0b7ade7890a9ff3d13d59d21e898acbee96e34af99ac`

```dockerfile
```

-	Layers:
	-	`sha256:bc78e9f65beac30f21dbd32aabdb75c04d52d35334fe36913632dad6e8add815`  
		Last Modified: Thu, 23 Jan 2025 01:51:34 GMT  
		Size: 36.7 KB (36733 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:d0e44711eb41a6f9dbf7130ca1d1093d900beb6d7aa7ed7445776833d4536972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (176019153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493ae1454b9d20a60b30305dc5ec0389978984f0917ab3264220e56f65a86396`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
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
# Thu, 23 Jan 2025 00:31:52 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_ENV=production
# Thu, 23 Jan 2025 00:31:52 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
ENV HOME=/home/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_VERSION=6.0.2
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jan 2025 00:31:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:31:52 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 23 Jan 2025 00:31:52 GMT
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
	-	`sha256:f7857cd8737af9a8eea315935d7d3ad7c3a82e44fffac567ef03f6b497990b7b`  
		Last Modified: Fri, 17 Jan 2025 15:45:23 GMT  
		Size: 31.6 MB (31602052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dc1f2cd02b6bb43fdaf613016e91db8e2234e6ab6224ae35d45a93e6b3dda1`  
		Last Modified: Fri, 17 Jan 2025 15:45:22 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b2cb413eadabd561e7d630fcf388acf7d1bce204dc58d55b96a05c801a84bd`  
		Last Modified: Thu, 23 Jan 2025 05:27:00 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6ce610ab56069fe6ace812e1389740c84cebfbe6b0b99a7fc2ef013a5d99d5`  
		Last Modified: Thu, 23 Jan 2025 05:27:02 GMT  
		Size: 64.5 MB (64459549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a05303f7cbb80ce7b713d643b856c67c3e2388156fc3f64bd9d8d9f5117d1e`  
		Last Modified: Thu, 23 Jan 2025 05:27:01 GMT  
		Size: 1.1 MB (1133468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87bd61268df5c20e044136bb9f4610f1570409950f74471579e57d90deebef4`  
		Last Modified: Thu, 23 Jan 2025 05:27:00 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8ad4fb8767741688cbf9c78173f26b463d2f962eb89d900dd36d07dabd5c6`  
		Last Modified: Thu, 23 Jan 2025 05:27:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b28677900f9a248390fde6ff24cc1aeb44e1b5f17d6d7e4beeb92f5a47a906b`  
		Last Modified: Thu, 23 Jan 2025 05:27:02 GMT  
		Size: 4.1 MB (4060107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75248df1c257640e1fa72d4ca24eb2511eab6a89687828c731095ab8a88290c0`  
		Last Modified: Thu, 23 Jan 2025 05:27:04 GMT  
		Size: 71.7 MB (71664646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaf62850498822413283527d27023191aa7bc06ba79bc6769f7b9ffedddf9a3`  
		Last Modified: Thu, 23 Jan 2025 05:27:02 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:317c936075b930c2f2b205f6bc1b8de21b38713ca92b7ff08f2ec9fd1258e034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdcff00745591eff74ac4bb2a81cdf08069941852dd10ab1ba8b69fa802df59`

```dockerfile
```

-	Layers:
	-	`sha256:4a3f6294606b2cb461ee9123188074aa6f69d1a4670a7ed74a944503057c3651`  
		Last Modified: Thu, 23 Jan 2025 05:27:00 GMT  
		Size: 36.7 KB (36733 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:beca578d0a13f71cab1f57dda7df071098258365def340889eb4426878758d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188804115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea1e17042dd0230e1e6fd230e010fc94a7d74e363c1edfd44ae59cdeaf86600`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
# Thu, 23 Jan 2025 00:31:52 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_ENV=production
# Thu, 23 Jan 2025 00:31:52 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
ENV HOME=/home/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_VERSION=6.0.2
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jan 2025 00:31:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:31:52 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 23 Jan 2025 00:31:52 GMT
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
	-	`sha256:caafaee6c97383e599c4b611cce429b0e07ba9ad8b337b34b13fcf110834706a`  
		Last Modified: Fri, 17 Jan 2025 15:42:32 GMT  
		Size: 35.3 MB (35269965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1e3f95b7155d84ae3a16166bcfdbd240ccc473b96bc35e0b4aca771410b154`  
		Last Modified: Fri, 17 Jan 2025 15:42:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98288518488021859cda63b2273d1308d08052972f5b1c99d2d4f5012540af9`  
		Last Modified: Thu, 23 Jan 2025 04:27:13 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16c53736647389c1c0acd51de1fd543ab6009f6ab0f620f2a9d5c18528d822c`  
		Last Modified: Thu, 23 Jan 2025 04:27:17 GMT  
		Size: 70.9 MB (70872499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ca8fa2b8906081a69903ea9a215f63c7f29358518ab0b34cd19c761dbcd7de`  
		Last Modified: Thu, 23 Jan 2025 04:27:14 GMT  
		Size: 1.1 MB (1093046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8606ca91a3e19f071a88b730fcf7dca29fd873fbcc514ab212a1720c4e059a`  
		Last Modified: Thu, 23 Jan 2025 04:27:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566c99501c793c632eb5919bbf3cf387ee070f4cc7094d8f3acae46561b07b1e`  
		Last Modified: Thu, 23 Jan 2025 04:27:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edce2c4435d2f8200f7be6a13500ac4d590065b45e72edde9ba815334e41bd5a`  
		Last Modified: Thu, 23 Jan 2025 04:27:15 GMT  
		Size: 4.1 MB (4060069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d53a9460ba0630c04be384b3a46044f2de77d4feba6b4dab94811acce3aa5c`  
		Last Modified: Thu, 23 Jan 2025 04:27:17 GMT  
		Size: 73.4 MB (73413955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727eab850955072aa4b95ea74b272218a3f38fbb7bcc9f713b08896674b23c09`  
		Last Modified: Thu, 23 Jan 2025 04:27:15 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:b3282e2db0ccd01fa7aa3a774fb1b254b448af66b52ea7085127356585bc7f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73029fffd763539d706c5bba31acd1d3dac0218a999ded6b63bfaab3763be31`

```dockerfile
```

-	Layers:
	-	`sha256:3ae552ad7aac0360f59e5716baba0cdee9c1183664e48cca72b90edd1ba85354`  
		Last Modified: Thu, 23 Jan 2025 04:27:13 GMT  
		Size: 36.8 KB (36771 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:20d021c6dd7e15448d5cde79217155aeea9ecc921492f81248a9b6f1e16fabd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184978460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf7881dd693d7fe2a194750d0687b129b9f993776e3c37d4eef150706c45450`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
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
# Thu, 23 Jan 2025 00:31:52 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_ENV=production
# Thu, 23 Jan 2025 00:31:52 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
ENV HOME=/home/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_VERSION=6.0.2
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jan 2025 00:31:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:31:52 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 23 Jan 2025 00:31:52 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76e68f0a14398fc38c22fe689ccdbe9efc47dd74545ef7d9a34649f6f391aa0`  
		Last Modified: Fri, 17 Jan 2025 15:31:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0359f30246be2d06710c6987628b7467e90dbabdacc03435c50f73fdf652e0f`  
		Last Modified: Fri, 17 Jan 2025 15:31:12 GMT  
		Size: 31.7 MB (31662256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fc27b86f75f6219d32a6b98fd674cf6828288fd7d26bfbf565789c3c211cdb`  
		Last Modified: Fri, 17 Jan 2025 15:31:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1634b3f8b92c6f77bb229f516c43d085a9afcf5bf7788b6ba94ba126c1422c`  
		Last Modified: Thu, 23 Jan 2025 01:31:40 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea35e30c6ac4ff1aaeff9872d5756acf703957e46b5a2a36682fb9410d0e8f8`  
		Last Modified: Thu, 23 Jan 2025 01:31:42 GMT  
		Size: 71.1 MB (71130789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0298c40b9cc07bfe4f2f6d1c6f4a6828efa9a379b99bfc4cbbded76ac97d2c`  
		Last Modified: Thu, 23 Jan 2025 01:31:40 GMT  
		Size: 1.1 MB (1141312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85d070a69905b0fc5df5b19549ffaca9521459c3012e02b4b04aac3461966df`  
		Last Modified: Thu, 23 Jan 2025 01:31:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a10deb504d83bbceacb9a307d138993d3a30b17c452faef9d13466959e58ef`  
		Last Modified: Thu, 23 Jan 2025 01:31:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf5c19d9bf95fbebf9d902b67fe739153d4999d2a8bfa419e54261f000ea2fa`  
		Last Modified: Thu, 23 Jan 2025 01:31:41 GMT  
		Size: 4.1 MB (4060055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff73be96d0b233be57742652f08c968bba3380e27f1e7362f519d0cb1b9ff1a9`  
		Last Modified: Thu, 23 Jan 2025 01:31:43 GMT  
		Size: 73.5 MB (73509263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a8afb2e17e408875542cc71969d02fd7838a5d8ef562728aebb010dfc11da4`  
		Last Modified: Thu, 23 Jan 2025 01:31:41 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:ecd131f41efd333b669d9c8fd8e467dd69c53e3126fb13f25a6cab6c343c737f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aa1c4c9deae86b8751ce053ba605e05275d2c3de27bcae8bed72a9b3e628a8`

```dockerfile
```

-	Layers:
	-	`sha256:2690af0ceac9c71794196c3ce5281a6a35d5c3a9eaeb0adb53c8aea749da1564`  
		Last Modified: Thu, 23 Jan 2025 01:31:40 GMT  
		Size: 36.5 KB (36550 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:971d0bbbab89845bd07455ba554ae1a88ca0330046af765a70ab248900d7ab1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189262757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c86e2a42754ac07977da97279f6f9514e22845b2d8c4aed3ecfef25c2166bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
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
# Thu, 23 Jan 2025 00:31:52 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_ENV=production
# Thu, 23 Jan 2025 00:31:52 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
ENV HOME=/home/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_VERSION=6.0.2
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jan 2025 00:31:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:31:52 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 23 Jan 2025 00:31:52 GMT
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
	-	`sha256:c209f5498ef3ad8ea7bb504c38f131ba50cf619a1851c75719ed8999b14e1b6d`  
		Last Modified: Fri, 17 Jan 2025 15:40:08 GMT  
		Size: 33.1 MB (33141129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e42e4c0bcbeddf68ab30e361f517c6280df5af0f0ec68a16549e7d1d49b8cf`  
		Last Modified: Fri, 17 Jan 2025 15:40:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accede89681b5328221967ac15052a08362d452fffb07824295b0afbefd6463d`  
		Last Modified: Thu, 23 Jan 2025 01:55:08 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3361ad1b46eeadb9a062ec461ce6bd6bf15402d232f4599e4048c66e0b36930f`  
		Last Modified: Thu, 23 Jan 2025 01:55:10 GMT  
		Size: 72.1 MB (72099114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da512c5657d2ba669509b07bcebc88f59b3ba33a6ff08966e1e7964597590808`  
		Last Modified: Thu, 23 Jan 2025 01:55:08 GMT  
		Size: 1.1 MB (1083636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5839870b835429453336e8d4af50cdb0f8d6746b0adaffbe948b14bb449b98`  
		Last Modified: Thu, 23 Jan 2025 01:55:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2abfc71b31b11039be152118c95d4a16e7a4483974ea173dc4ea76bb5f12de`  
		Last Modified: Thu, 23 Jan 2025 01:55:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cf29380593dc6c38fd82748ee434b28f1ae8b0a359e1d599b8363709e7638e`  
		Last Modified: Thu, 23 Jan 2025 01:55:10 GMT  
		Size: 4.1 MB (4060093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8428b34348f0319ea2d651e240d150994cdd3c7293fa66fc2bf3ff6ccb145f59`  
		Last Modified: Thu, 23 Jan 2025 01:55:12 GMT  
		Size: 75.3 MB (75300567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7af25653ff267138120751fbec1f7dd923480c652101f41954c9cb1d617ad`  
		Last Modified: Thu, 23 Jan 2025 01:55:10 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:5b1efcffea05cd8a374f2298d20dc8f52d305ca15f26a66c31f42e18e39f3799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d586bed5ff82f988a30e5cf7354e485de3a039f10242c771ca16ca04103b5c`

```dockerfile
```

-	Layers:
	-	`sha256:8048f8474f356b5595dc5bd650626ff16754567fd4c322d8264b66edb8f19071`  
		Last Modified: Thu, 23 Jan 2025 01:55:07 GMT  
		Size: 36.6 KB (36646 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:ef3518251b013d0caa38546cca9e388c10b08e92dffdc64b6917bc2070faa2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187695046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00b85ddd6c7a427be6564c8916417578bbedfdf798aeec9476da6e42bcd4f97`
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
# Thu, 23 Jan 2025 00:31:52 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_ENV=production
# Thu, 23 Jan 2025 00:31:52 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
ENV HOME=/home/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_VERSION=6.0.2
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jan 2025 00:31:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:31:52 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 23 Jan 2025 00:31:52 GMT
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
	-	`sha256:703b13c3738bcfad450312b6c3271d13582ed04a28739b68831f26b53ebd99fa`  
		Last Modified: Fri, 17 Jan 2025 18:26:13 GMT  
		Size: 31.6 MB (31552550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e3724aa281a150ca69aee1f729479410507f445405497dd77a4e15000217e1`  
		Last Modified: Fri, 17 Jan 2025 18:26:08 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5be5fed7c6a42a40d8c3a39096eef5c2b8d598df9420cded1132b9fcb277f15`  
		Last Modified: Sat, 18 Jan 2025 03:26:05 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb351b3bef38e27e83af5ba163cb509bd08400b172ec520950eea08a823d684d`  
		Last Modified: Thu, 23 Jan 2025 03:53:27 GMT  
		Size: 70.8 MB (70782414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6958905c64b6ba461da9f30fdb2c034531f28add1a3da725a88aa6d5fe28e78`  
		Last Modified: Thu, 23 Jan 2025 03:53:17 GMT  
		Size: 1.1 MB (1134858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac89ad94a31e41c43ad7dffc7bd532b3d57f9a6483ee079058021bd08f6987bb`  
		Last Modified: Thu, 23 Jan 2025 03:53:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eda11949096002bedf49e47e29aae692cd7d1c5558843e704dbcf37bbee4b7c`  
		Last Modified: Thu, 23 Jan 2025 03:53:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea49836510b9f1b21864e9f213f598395053f9830f730fc5c66d99a9addc270`  
		Last Modified: Thu, 23 Jan 2025 03:53:18 GMT  
		Size: 4.1 MB (4060115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca88dc3039e97f86214a54716b70381c51fc80c64603ee76c6268210205b4771`  
		Last Modified: Thu, 23 Jan 2025 03:53:29 GMT  
		Size: 76.8 MB (76789368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd47fabb4048a26e4bdfa3779b0618d5651b442a0e9abc579a089f96a1013e6`  
		Last Modified: Thu, 23 Jan 2025 03:53:18 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:31451606887c338f4af578b5bc3307182be523bc0db0ca14820c76540f066469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33be2fd5355922fe3ddfd1dec73f8c795424910f6f82022ffc94beea5ed0880`

```dockerfile
```

-	Layers:
	-	`sha256:3de67fde2b09eaf22e7c7386869306964294f709485d8bf92874c46d5ce31ff4`  
		Last Modified: Thu, 23 Jan 2025 03:53:16 GMT  
		Size: 36.6 KB (36646 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:2ab8357fe76810e77968994159f40f620666bc17d7564d870b096c934af57d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188474420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6084b7f436eb78cb4c382213c136c1c6874554bfce74f47f9c5a1b1c3835b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
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
# Thu, 23 Jan 2025 00:31:52 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_ENV=production
# Thu, 23 Jan 2025 00:31:52 GMT
WORKDIR /usr/src/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
ENV HOME=/home/redmine
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_VERSION=6.0.2
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.2.tar.gz
# Thu, 23 Jan 2025 00:31:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=d06e8b1b0c0c9210d2ed6207d2a3f729c26a996255e47c3b0bd4782550150e45
# Thu, 23 Jan 2025 00:31:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Thu, 23 Jan 2025 00:31:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 23 Jan 2025 00:31:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 23 Jan 2025 00:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 23 Jan 2025 00:31:52 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 23 Jan 2025 00:31:52 GMT
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
	-	`sha256:60f7fb7cf1b7038b6fe65507b9be7797a94cf06f6599371eed9880da50a374ef`  
		Last Modified: Fri, 17 Jan 2025 15:41:00 GMT  
		Size: 33.0 MB (32983647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff43768b36ebe41cbd93411def03ae863c0d7552ca990d44737eb3c2d1b8f9a9`  
		Last Modified: Fri, 17 Jan 2025 15:40:59 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49293b683e8831b27d077c19fc7ca0c9b80486a5eb3ee8919566c2c4f6e0e3c`  
		Last Modified: Thu, 23 Jan 2025 03:25:59 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb464bfa6913e43d3e9a07317adb50efcbc4843b257833d74235b8e84106e19d`  
		Last Modified: Thu, 23 Jan 2025 03:26:01 GMT  
		Size: 72.3 MB (72288136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b47105a05959227277827abcf93551e4d2229c4c4e52ace37601481f0fe504c`  
		Last Modified: Thu, 23 Jan 2025 03:25:59 GMT  
		Size: 1.1 MB (1131117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a3be27a5649df5ef71af63a4230e1b5fcf0ab0084096b85feddd7d63c3b569`  
		Last Modified: Thu, 23 Jan 2025 03:25:59 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6f81340d334d6da77b44e2c2cd76014795c1cc383ae2adc43109f9b922bf01`  
		Last Modified: Thu, 23 Jan 2025 03:26:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4203211829d2aefb321e3f6f290f28cba5e7dfea3512703e8b0c6a4e66c5831`  
		Last Modified: Thu, 23 Jan 2025 03:26:00 GMT  
		Size: 4.1 MB (4060069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce3b0eb30c5541e4bf0f4f401caa66c55130f53fe5282db6aace9dae6517812`  
		Last Modified: Thu, 23 Jan 2025 03:26:02 GMT  
		Size: 74.5 MB (74544310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d15e39ce23c4bbe1a935018426e9ca1cb32298194ee79f37a031229124ee3d`  
		Last Modified: Thu, 23 Jan 2025 03:26:01 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:dba025fbfb176b6484b0d1d5b37f793988e366b372fcc3a406aeaf758eba722a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36d61e9bd809e61ae87480e654a4bc2e387125e531ceaeadf5d0e8e1873afe2`

```dockerfile
```

-	Layers:
	-	`sha256:4bebe23746b6de2c35bdabe84e282195591262acb67592b0432502f86b01bd40`  
		Last Modified: Thu, 23 Jan 2025 03:25:59 GMT  
		Size: 36.6 KB (36592 bytes)  
		MIME: application/vnd.in-toto+json
