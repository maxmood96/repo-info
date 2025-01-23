## `redmine:alpine3.21`

```console
$ docker pull redmine@sha256:24a5c48f82ff32f739e2e4f24258a60556ed5bb311fb833ec128129adfc67934
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

### `redmine:alpine3.21` - linux; amd64

```console
$ docker pull redmine@sha256:0f892890f44355f59b59990c000099e720c3a8ddf679e8c550611a138748825f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190291259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d3e72ce77d10441f08a2ed202a0dbfcd036f40b96810c3df1b37115d593b32`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:2c245f854cd82b5ed050a1545382fb5d792d25713c70b22f0e4f1f6083a94483`  
		Last Modified: Thu, 23 Jan 2025 01:31:45 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d3ff29678c299e5357375ef784122c390668c2e6a92eb34de965983b10d90`  
		Last Modified: Thu, 23 Jan 2025 01:31:46 GMT  
		Size: 72.3 MB (72286739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f47aa8666c4430d633f9bcdc1d53548284dd1146040dd878fce76415cb061bb`  
		Last Modified: Thu, 23 Jan 2025 01:31:45 GMT  
		Size: 1.2 MB (1168322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11de2bd83f84f88bc4504d5019aeae61788615e6c7c2371eccefc23bf47eaf5c`  
		Last Modified: Thu, 23 Jan 2025 01:31:45 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d12d44fd7a5d85b57e2373a443341b64ddf7c885fae8e5401ed093a88f6b4c`  
		Last Modified: Thu, 23 Jan 2025 01:31:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ca17a732fb69a2c40c9d462b27de7cd8e36b830385d6183b166f73a28884fc`  
		Last Modified: Thu, 23 Jan 2025 01:31:46 GMT  
		Size: 4.1 MB (4060086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef2356f0031b9df1128f5bb81d714643eab56a2d99afa021dc9669fbb784d4`  
		Last Modified: Thu, 23 Jan 2025 01:31:47 GMT  
		Size: 73.6 MB (73566296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee0952867d40b6347187ff7ba1506f306fb5f3e5bf1b4694cd4f35b47e88b4`  
		Last Modified: Thu, 23 Jan 2025 01:31:39 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:10254633c035d2720be463abb7424cf2772b7680dfd347b25f4507b78843939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e41e79bd3fc709379a78e425467019c6828ed158ef01bdef9e9ef1af369241`

```dockerfile
```

-	Layers:
	-	`sha256:f90a43d48a22235cdbf812ec9721d7d282fa5a9458d1195c4cf322aa9c312be0`  
		Last Modified: Thu, 23 Jan 2025 01:31:44 GMT  
		Size: 37.8 KB (37815 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm variant v6

```console
$ docker pull redmine@sha256:64db9fc51e45bbc61378bbc31f110f46eb19dbbd5c43e38b1a4d6a40a4cb8aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182258820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d5302e7a82fcc93aac4b2d573f0aa38ebcf1e9c1487d426bf1c99f3e207f00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:5093a9c1e09067e57f9dec9d91ddcfc3ef4ce61e086f08fb67ffc5a36a782b6c`  
		Last Modified: Thu, 23 Jan 2025 01:48:07 GMT  
		Size: 68.9 MB (68909858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca1577192e5a763baced6f62fe1c949050387fad9e026124e69c027f3c0658`  
		Last Modified: Thu, 23 Jan 2025 01:48:05 GMT  
		Size: 1.1 MB (1134888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8f2240acfee2cc190e71d1c363dd3295786d9b9890fd5ad48ee5b9a422227a`  
		Last Modified: Thu, 23 Jan 2025 01:48:05 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6967658a838294aab93df9b8bd7808932fd6f260db1886ff72570897cb4ab8a1`  
		Last Modified: Thu, 23 Jan 2025 01:48:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d954911de2e36b24c73cf3dc6ac2315c86440621710cf3974900d0580c6b6fd5`  
		Last Modified: Thu, 23 Jan 2025 01:48:07 GMT  
		Size: 4.1 MB (4060094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e983077745f7a4197fd20d12337091e1f0cb55049924b552882462e12d79a2`  
		Last Modified: Thu, 23 Jan 2025 01:48:09 GMT  
		Size: 72.8 MB (72757216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9c012ab00937c0fec792d89ac032f6a32656515addb000db07c124af80d5c`  
		Last Modified: Thu, 23 Jan 2025 01:48:07 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:248ca046a609de6a7f2c997dd4c340ae402570a3dff66321854307a424116d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7710937e7466d37fb4ea8a36f8bcd13fa7112dfffffd5a448ae0a55bf1c33f`

```dockerfile
```

-	Layers:
	-	`sha256:cbb8052b701198dc71ef7bb8838bbf70336ce6be3e3a9295c0ec49c345db2509`  
		Last Modified: Thu, 23 Jan 2025 01:48:04 GMT  
		Size: 38.0 KB (37989 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm variant v7

```console
$ docker pull redmine@sha256:212a8de348152f7a3b2514a5c07fbb6b36198a2c7dc5fce8a33f7ae94a9ff8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178086211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8eb84c75ed22582b5dbab489c1c8ea558ca59528ddaee588d6cabf50d602fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:dbced16893abb6d32b873337c2b4d19e542f627763d554fbba972b76f6aded42`  
		Last Modified: Thu, 23 Jan 2025 05:23:45 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077809b9acfc3d49b119d0406ddd5db851efb9f943531336056e8af0b318d5a8`  
		Last Modified: Thu, 23 Jan 2025 05:23:48 GMT  
		Size: 66.1 MB (66095308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4ac6269323d8085ad39bb30d1659c9e7b0936e148c05b4c25f3b45638cc669`  
		Last Modified: Thu, 23 Jan 2025 05:23:46 GMT  
		Size: 1.1 MB (1134866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8ce9b4106f2baf314785edd84b020a0764563ce9b6903db10b400b504b9a55`  
		Last Modified: Thu, 23 Jan 2025 05:23:45 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2812bf45a596603b850c9bb360fceb4e9ada45e3d055ca9feafd0d6dfdda2138`  
		Last Modified: Thu, 23 Jan 2025 05:23:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9007c6c5494d602d2ebe6699a2e95ae1e3362be6a22ab904b54d78e15c455d0b`  
		Last Modified: Thu, 23 Jan 2025 05:23:47 GMT  
		Size: 4.1 MB (4060095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7e21bd1552e8375223b7c0af84d04cab639f979ba8c007af0c6d7079c34c17`  
		Last Modified: Thu, 23 Jan 2025 05:23:49 GMT  
		Size: 71.8 MB (71807026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea2e1246e5f95f5986e046b1d714b5b04c0d183a9130c62e47764505f9c4e7`  
		Last Modified: Thu, 23 Jan 2025 05:23:47 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:f9785d1bc5a939a83bd76d4d743e6f8c29e2526938030b586b4ac1f7c8695fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e84bd74aa5ec258b7dac6f8238e5b51696b5f263128a9364716a4bd82f7ee10`

```dockerfile
```

-	Layers:
	-	`sha256:c6aae552f0f89399dd24d1f34e913df0695f7464ef24c57de047741f7560c5f1`  
		Last Modified: Thu, 23 Jan 2025 05:23:45 GMT  
		Size: 38.0 KB (37989 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:f9d26dc71ed6f500ce3e9279067060cd2af96be68e6684da576c560d2c360c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190176951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a63eb16467478c17beca01eb2e0fe79c5abc321c472eab7a77c800478c73b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:0f0745a3b261527e8b4016876f04aed701394108e643525c81f4a0e118d1f7ca`  
		Last Modified: Thu, 23 Jan 2025 04:24:21 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde0ba0d7c25e06fab4f2a3b33ef102c6087e8516f70c794797d9fa8af2e7e5b`  
		Last Modified: Thu, 23 Jan 2025 04:24:24 GMT  
		Size: 72.0 MB (71968074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33a2bbc165a93017053db02ca6da9ec4e169e65d140de5815168e1c570d2019`  
		Last Modified: Thu, 23 Jan 2025 04:24:22 GMT  
		Size: 1.1 MB (1096384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c4637f4e3bf67077fc62f67695737df44fad083f57ea37d1f9074f8c390de5`  
		Last Modified: Thu, 23 Jan 2025 04:24:22 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a39293f9d8edbfc28ba2c6b346b114ab6a23d002fc067d3e2767ec7c6ee3fd`  
		Last Modified: Thu, 23 Jan 2025 04:24:22 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e19c66a5c72e193f8072531776a22d56d426925f66f1d0152e50993bf4cef2`  
		Last Modified: Thu, 23 Jan 2025 04:24:23 GMT  
		Size: 4.1 MB (4060069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cf3320b57b78cee9554cc7980fa557c3b4f2d23be6643c9daea5e0ed445bcd`  
		Last Modified: Thu, 23 Jan 2025 04:24:25 GMT  
		Size: 73.6 MB (73556809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006bc876c810e9f538c90c12c9726e22b8039fa55aa4a3bc8af89b1d2578998e`  
		Last Modified: Thu, 23 Jan 2025 04:24:23 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:8b24fb7b0d926894d28a81ff4367b43a3e8b567e5a8345191382d2271ab8a3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8486a002387fa679565dfad3ccc815afae00790c63625fbd558d333ccaa1f1`

```dockerfile
```

-	Layers:
	-	`sha256:e3af7f6d4e5bc1edae9bc21e15fb5e71a5549989424ce37418233ced4dee9584`  
		Last Modified: Thu, 23 Jan 2025 04:24:21 GMT  
		Size: 38.0 KB (38043 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; 386

```console
$ docker pull redmine@sha256:04ee8dd3d7d69e966e3838536850661eaa6ac93d970ab2908e37d133994eed2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187220883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c837ef077eb6166f88f3c863140d32ee79cfdfea25fd96bdc5a7b08ce7091df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:71b66780523b9037f294efec2c055519248f2eba6ffd2159412d32ee413f2816`  
		Last Modified: Thu, 23 Jan 2025 01:32:33 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228dd11223c855bc696363f771088527c263a4755c6eb0a027d521d8074a860`  
		Last Modified: Thu, 23 Jan 2025 01:32:36 GMT  
		Size: 73.0 MB (72966011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dade2dd5de3a2a011aec3c2259a2193ad0d9c627a5eeabf35010b5ec640812`  
		Last Modified: Thu, 23 Jan 2025 01:32:34 GMT  
		Size: 1.1 MB (1143570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ed56da43e2939c4cb8a280e9305b61bbcd0c090885799d9aa4c26c6d9c7294`  
		Last Modified: Thu, 23 Jan 2025 01:32:33 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff0e8917a33f047b5acabf116e4c71e23d084668e3d57fc739c888bcd8014d0`  
		Last Modified: Thu, 23 Jan 2025 01:32:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572cfc414f06e4368d5a95a4aeffc87f30cf67a708a9b5f23553039af2b8901f`  
		Last Modified: Thu, 23 Jan 2025 01:32:35 GMT  
		Size: 4.1 MB (4060077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fc4be0d1ecc28e9dd9cb260afa26ddd6f884a84c868aeedfd82de0370dd652`  
		Last Modified: Thu, 23 Jan 2025 01:32:37 GMT  
		Size: 73.7 MB (73677405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b41002be40367524adb89cfc9c85dc3d700571d43cb7635dcd70892d3454ed`  
		Last Modified: Thu, 23 Jan 2025 01:32:35 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:11004079d171efc945298ce5ce1033f48e4053b03a9da08e0203382e19c176c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ce8c43322db82a3df027f442d9e099a8e7dc65a21fa696b4e9f0e5f4d2733d`

```dockerfile
```

-	Layers:
	-	`sha256:ec544f3d00d8aeecb574b141ece0ff84840f42ecb1b0c3699598598718c5119f`  
		Last Modified: Thu, 23 Jan 2025 01:32:33 GMT  
		Size: 37.8 KB (37754 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; ppc64le

```console
$ docker pull redmine@sha256:f5628086c0d07692838c6790ba501d10ade2fc49465aae53caa60a2e6c6106ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191604082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9d6c098b0fd6e78b8da4bedf11f621d70dfc40adfa37cc4443ffcb0f3ec2fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:97f34c1d2e09c4c9783b20d488236259ed853fe5dd9c6eedc4a1f1c599fcd444`  
		Last Modified: Thu, 23 Jan 2025 01:51:05 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd15d8124e29022d26ff8923799cce3de5a52fa2d8c88f0392449cd9c7dd1045`  
		Last Modified: Thu, 23 Jan 2025 01:51:08 GMT  
		Size: 74.0 MB (74010428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122e41d9ec230d6094de016eb3dca97c4689d28cdce7c29106289023edb4a1c`  
		Last Modified: Thu, 23 Jan 2025 01:51:06 GMT  
		Size: 1.1 MB (1086982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042dfcb39bf4fddea0e7a0d9f894fec985865486b223bc713f27d5ad8a1587d`  
		Last Modified: Thu, 23 Jan 2025 01:51:05 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851083da938ad3dfec865f0f16d12fa14ac6197116ec563e6659cf5315c79d33`  
		Last Modified: Thu, 23 Jan 2025 01:51:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c297045825ae43cc6b416d0aab92e1562acbf4d30168c8b9e0f4c85eed07a9db`  
		Last Modified: Thu, 23 Jan 2025 01:51:07 GMT  
		Size: 4.1 MB (4060089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444852c50513d74ef5f33ac0a651354bcc6fae9c5ed5ca5cf2deb6ec1a91a93c`  
		Last Modified: Thu, 23 Jan 2025 01:51:09 GMT  
		Size: 75.5 MB (75463533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253515738962787d06cc470d09c6bfe1bd9b9e7731e95c2b770d8a516722d00e`  
		Last Modified: Thu, 23 Jan 2025 01:51:07 GMT  
		Size: 2.3 KB (2302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:2ecb3b0da55d5431e7ad81d175afe2859324c798f709d4fd0dbe026a9723a1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4582aba73a97db53dc1471e38741f77b7a352d4b936898a28e370994dc902ef`

```dockerfile
```

-	Layers:
	-	`sha256:cbd87f3b405c29bd0adfa3f3b205c3f16144a547c3ea3cb4392fbfc91aea4dd3`  
		Last Modified: Thu, 23 Jan 2025 01:51:05 GMT  
		Size: 37.9 KB (37894 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; riscv64

```console
$ docker pull redmine@sha256:65d15e42f7517f06bf67afd44be827735cb8ac271b7af75d6c540789fddce8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188295216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2947a66b93ed5f3762a58ee31abeb302f21b672d49c14cc3dcbe362cb01099`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f58c5f1e872ea5fb6d2093f25dc7e3e4e42116a78691c8d841fa04894fccb8`  
		Last Modified: Tue, 14 Jan 2025 03:53:39 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9268d7da2031a16625d5cd04558c011bebeb920c4c9799bacaee0ee8103674`  
		Last Modified: Fri, 17 Jan 2025 16:57:50 GMT  
		Size: 31.7 MB (31696974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed8ecf49dc85b0f6228b49179627b3ea56001b396a15c156113ba061dc5c34d`  
		Last Modified: Fri, 17 Jan 2025 16:57:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7bcb8feae490fd67f6382d7b73711aa4663305c2059d12ce0b19f6d3ed88a3`  
		Last Modified: Sat, 18 Jan 2025 02:09:50 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac0f54626d27ff1264b9ea7c286d22a5d46fa60ef0f27ac775376357a8476d8`  
		Last Modified: Thu, 23 Jan 2025 02:52:09 GMT  
		Size: 71.1 MB (71086481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de6d535b118f3110c646d09c738134fcf759c9e1b4a8a63f8027a8bf653e5a8`  
		Last Modified: Thu, 23 Jan 2025 02:51:59 GMT  
		Size: 1.1 MB (1136704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9507f6050058eca103a46bef889335b9ecc21cfe7fe7064fad4e80cd2d112e5a`  
		Last Modified: Thu, 23 Jan 2025 02:51:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539142952bec66d142f5f03182bfae3f5561a659f7f07af646a6985a38ba6b0`  
		Last Modified: Thu, 23 Jan 2025 02:51:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77890df3afc02bc159dde268385e79d44d1a77164db0bab712a96f52b3ba5aea`  
		Last Modified: Thu, 23 Jan 2025 02:52:00 GMT  
		Size: 4.1 MB (4060120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4deb281a77f2c9da35087c6267410ca5675c61bb7b9ac4cb6cb238c53b0db73b`  
		Last Modified: Thu, 23 Jan 2025 02:52:11 GMT  
		Size: 77.0 MB (76960874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dc403a36239a75ca1651205bad5fe0904ee9fd65d3bcba6d3479d1009e380c`  
		Last Modified: Thu, 23 Jan 2025 02:52:00 GMT  
		Size: 2.3 KB (2298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:65d9d040fccfb0d51009fcd04aed2a9677a77a72f083061cf40afcedc174dc80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218c589d364754ff83d38795a3c83aaaa16037fb0ddb32b21cb0d9e93f51b2bf`

```dockerfile
```

-	Layers:
	-	`sha256:fdb293afe8392b517e5772388ca460ff8b4de41209be483794aef6000d40a3a0`  
		Last Modified: Thu, 23 Jan 2025 02:51:58 GMT  
		Size: 37.9 KB (37893 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; s390x

```console
$ docker pull redmine@sha256:a0f0e9881cf64a1e70647e300828345b8a7e5b2abc94471d5884f21a891548e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189613272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdfa4443d2c4147794b618bd070c675b9bc913606b96725ea81dab34b10078d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
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
	-	`sha256:8f3856a909077d5ddf372c941e05e1eb36117b0b18f9d65e9b88f5e7661c4bf4`  
		Last Modified: Thu, 23 Jan 2025 03:22:42 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e506043582470f55d0c6808aa8e02c224870a0ddbfa22dc5c2d2b2ddddd1eeaa`  
		Last Modified: Thu, 23 Jan 2025 03:22:44 GMT  
		Size: 73.0 MB (73029501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3789af8404a77a5892bd4e402a9293c1c06101d9cd996856ac75807ed91383f9`  
		Last Modified: Thu, 23 Jan 2025 03:22:43 GMT  
		Size: 1.1 MB (1131712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d9e01621d331fc8537d3a34f125b2eb1087f3b3ab3d7169e8192efe9b44827`  
		Last Modified: Thu, 23 Jan 2025 03:22:42 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166203d31f4ba53b69a9672e5707bc2df6ad249c2f4707386d7699ced8a2b451`  
		Last Modified: Thu, 23 Jan 2025 03:22:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14319eeee92e3b2ec5ae01c0527147b3df2360e90703565307da7d70284348d`  
		Last Modified: Thu, 23 Jan 2025 03:22:43 GMT  
		Size: 4.1 MB (4060070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb2f97a4f54d5eae4ea818fd70cfd608ddae8bcdce4ca344ca9e5e85affee5`  
		Last Modified: Thu, 23 Jan 2025 03:22:46 GMT  
		Size: 74.7 MB (74727674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442162f24b184d9a9e4e3f15bd3e298c397073f165f9e6d0f71a019e4bc8e1b`  
		Last Modified: Thu, 23 Jan 2025 03:22:44 GMT  
		Size: 2.3 KB (2301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:a8ca4c4dce8eea52c6c5bd74cc76c98cfa0a60ad009dbee1f1877f9ede3df749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac292f8b6b1885505ba770e14d8ee471af6e7f870bb689d662189ed34d5230cc`

```dockerfile
```

-	Layers:
	-	`sha256:4b2648bc7b590df27c8c3133a4b4ae6808a6df2be7743ea5ea381d6b0eff3f68`  
		Last Modified: Thu, 23 Jan 2025 03:22:42 GMT  
		Size: 37.8 KB (37815 bytes)  
		MIME: application/vnd.in-toto+json
