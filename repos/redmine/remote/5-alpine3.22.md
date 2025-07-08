## `redmine:5-alpine3.22`

```console
$ docker pull redmine@sha256:67edcb17193a8b6637b39a87958f89626f9b82e65e79aa8bf589672d17257688
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

### `redmine:5-alpine3.22` - linux; amd64

```console
$ docker pull redmine@sha256:ba4cdef38ea43b53dc9c8c862ea37e2b192f1e4a60ef8182e5be983b84733325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190448207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ae4b581144640de3242d020696841cf54f195f9375d196f186d028a51de7f5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:00:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:00:32 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_VERSION=5.1.9
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.9.tar.gz
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=cc0ddafa6fe6f5192236a27cec64e3466023a12c92c1da4abb680248639f678c
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:00:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:00:32 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:00:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522ad4c993aae9f229d493707aa5e0af3140470619d0ec81a67637dbf6b1da46`  
		Last Modified: Tue, 03 Jun 2025 13:30:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8fb040c4faf7d9220591e3321bc9c771e59cf804593e896acefd80ef6f6e9b`  
		Last Modified: Tue, 03 Jun 2025 13:30:59 GMT  
		Size: 33.8 MB (33834050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa3828beeb85dec48fbdb1c7a7a29718878a4306f32be568a3945dae5f62a91`  
		Last Modified: Tue, 03 Jun 2025 13:30:56 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1a20eb188861acbebacbb893b2b9a2bea1ad3af86846b85c495c91b9ba7a9d`  
		Last Modified: Mon, 07 Jul 2025 23:17:12 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb530ef83be59b58957f342f32f442dafb8aa76bf0c01663c256e20f06d9b3cc`  
		Last Modified: Tue, 08 Jul 2025 01:50:33 GMT  
		Size: 75.1 MB (75059799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5535d2573ad250e7640852f8ce816ec79cb63817a17dee61cb7cf488c5b35d7`  
		Last Modified: Mon, 07 Jul 2025 23:17:16 GMT  
		Size: 1.2 MB (1168539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33608e1d551e77d7f0948fc316484068f8fdfa2e915efd80f21e5141ff86c773`  
		Last Modified: Mon, 07 Jul 2025 23:17:20 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdd19c85d86c21978e331e20029711f6f39b72206108eb2562b1cd2f827d355`  
		Last Modified: Mon, 07 Jul 2025 23:17:23 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f99754baa0a1e6d41d76db495f01dadf909ed18a0d467f5ec8edb07dd14d0d`  
		Last Modified: Mon, 07 Jul 2025 23:17:25 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503a52ab69caf556c61aac948223696ef60de1928d758dd65c73c5c53b1e1e17`  
		Last Modified: Mon, 07 Jul 2025 23:17:29 GMT  
		Size: 3.2 MB (3249834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0626c28017220d581b39a362c75b1789df0db23d287bd68939905c55c76ca3`  
		Last Modified: Tue, 08 Jul 2025 01:50:32 GMT  
		Size: 73.3 MB (73335167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f383e186d0d833485bd6c223385e7ed3f6b186d3eb6a29c33232ef0b97ee0981`  
		Last Modified: Mon, 07 Jul 2025 23:19:56 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:a8bdb6cefd9fe604388d4657c309b2955625b82c6617b32a52d45f8809d9c7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd35cfde02ee260086d3a576188374d93595a7e41665cd201a62a051df28078a`

```dockerfile
```

-	Layers:
	-	`sha256:a02248a0b12d0e2deeb1cb4890222e8fadc1e06df696fc9afd22fe2aa88f23f5`  
		Last Modified: Tue, 08 Jul 2025 01:49:48 GMT  
		Size: 40.6 KB (40559 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; arm variant v6

```console
$ docker pull redmine@sha256:8c2a724b5783e6746403e177c7a6fe5426ced94e45629195da0c563ae5f2bf91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182062503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef134455bbe5a66c71e443ea14ee64b4d0f61fbdd01dfe98eb18ca6aeccd921`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:00:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:00:32 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_VERSION=5.1.9
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.9.tar.gz
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=cc0ddafa6fe6f5192236a27cec64e3466023a12c92c1da4abb680248639f678c
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:00:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:00:32 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:00:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c91b400dce72b0b6821109c8cd8b30e2b7f0da467f2906fb512173d0c3b9770`  
		Last Modified: Tue, 03 Jun 2025 23:13:12 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc10e25224d4d39cbe901b00f6b11f2b75fe7abfd57970d8abb18fd387002e`  
		Last Modified: Wed, 04 Jun 2025 01:50:40 GMT  
		Size: 30.1 MB (30075580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436ba38427bffe99232908382ccecf705cb6b882911a9dbcadcb43f244c4b2a9`  
		Last Modified: Wed, 04 Jun 2025 00:11:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65ae78fffdc0f709183f6fdc969941bd45ac57f5ca2f32e990bf33740e7f91b`  
		Last Modified: Tue, 03 Jun 2025 23:11:03 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d14d6ff01441959062966ce5b7d0a77819cd994d6f893189a4b3f7b55babcd`  
		Last Modified: Tue, 03 Jun 2025 23:11:08 GMT  
		Size: 71.9 MB (71864689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdb31d28df6c905f3d231b576b0e386ca8c9ac46d95343f9a31c1d29787ba88`  
		Last Modified: Tue, 03 Jun 2025 23:11:05 GMT  
		Size: 1.1 MB (1135050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bfe79b4a975876d6a006befaa1dafe6ae503db30575056d84ba63a148364e9`  
		Last Modified: Tue, 03 Jun 2025 23:11:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b4c67932bbdef35c60b0eab59b52bc97bea5564e0188b1d0df8c583c853885`  
		Last Modified: Wed, 04 Jun 2025 00:11:36 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02ce5e371428366a4e766ba43a2ba38496ca4b4198099c2bc4e9339916a979f`  
		Last Modified: Wed, 04 Jun 2025 00:11:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c519673af6d8354f940192399edab6bf93341d3c6fd6f6ebb0721bf116308ccd`  
		Last Modified: Tue, 08 Jul 2025 02:12:46 GMT  
		Size: 3.2 MB (3249841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188d11c8a87cb7cf5e17b51f06be5815c9d3543803959e4e969c2f45375e6184`  
		Last Modified: Tue, 08 Jul 2025 02:12:52 GMT  
		Size: 72.2 MB (72232442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82d8960aca32209b48b7760cc97f158c16620df997430468e0a8f08d6b0d95e`  
		Last Modified: Tue, 08 Jul 2025 02:12:44 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:a1d798133b7bda459cdac15d4881b7aa2a5bcd3bfb2e3c337281e37cecf6ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe548d9b54ee45d7b62cfe2b3bdabbab76882f98b2f795b30d3d0d06062820`

```dockerfile
```

-	Layers:
	-	`sha256:0dda56322b22c832ecd981fecd3765dc7904a1d297c12d398f1d27933769a803`  
		Last Modified: Tue, 08 Jul 2025 04:49:39 GMT  
		Size: 40.7 KB (40726 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; arm variant v7

```console
$ docker pull redmine@sha256:e9cedba9a9f8d52dabc0b0ab7f6ae2206ae5ecf1585c09b59c420e3f866b7383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.3 MB (177335079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4bad5b94e17dfacc668a522d780139e0f0ef3035efe93467bfff4a01c81f67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:00:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:00:32 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_VERSION=5.1.9
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.9.tar.gz
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=cc0ddafa6fe6f5192236a27cec64e3466023a12c92c1da4abb680248639f678c
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:00:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:00:32 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:00:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515553b759e392d75aecb0e255f515eac2b780b60c7e96f356592aa5e3a6b63`  
		Last Modified: Tue, 03 Jun 2025 17:47:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e424b0e7cdff027db1191499a32ab1f208e2891f5d626f89667a5e07e0c710`  
		Last Modified: Wed, 04 Jun 2025 01:50:39 GMT  
		Size: 29.9 MB (29935538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c55ff029826aaaec66add553e8142bf552af7ac747e741f21d08414302d92e1`  
		Last Modified: Wed, 04 Jun 2025 00:17:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db150b1e8c5e21dd9486dcd063efee7908005f573daf24aca12c02fa1267b50`  
		Last Modified: Tue, 08 Jul 2025 03:49:46 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6fc259cbba1b4d2b3bc507a5ec2a7f55834a1b01b52e72bec54312d3a184ce`  
		Last Modified: Tue, 08 Jul 2025 03:49:50 GMT  
		Size: 68.7 MB (68674110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c670df153517b6454cf4faefa1e2bfd4c3ea78106ed1567a484cd02ee58c7649`  
		Last Modified: Tue, 08 Jul 2025 03:49:46 GMT  
		Size: 1.1 MB (1135021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d98ca3c532bd56ad345f18c85ba23f3e0a0b24076bca7d35d480626450d1dcd`  
		Last Modified: Tue, 08 Jul 2025 03:49:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25aa1caaa465df30cfeed813d1771044e9179e3a88694a7e53535432b59aba1b`  
		Last Modified: Tue, 08 Jul 2025 03:49:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc51df4e469dda18dc1c9e1dac77ac5ac904c4fa018507de6856a365d122e6a`  
		Last Modified: Tue, 08 Jul 2025 03:49:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d1824f30a9b0d2be7d35ec6445f60d83aa8adf17b8c37f04e8359dfec8c7f8`  
		Last Modified: Tue, 08 Jul 2025 03:49:46 GMT  
		Size: 3.2 MB (3249929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278b3dede68947c9390f159c99118f340dbdd8a5b31725488fa17fda200c529d`  
		Last Modified: Tue, 08 Jul 2025 03:49:50 GMT  
		Size: 71.1 MB (71117324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52b8b63b58e3b4ca73e672ec10730cf6880b57eb4d0ed4a8e343feb4750ead7`  
		Last Modified: Tue, 08 Jul 2025 03:49:46 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:0cc7aad648edca5817ff75bcb36e2677ca79180cdf189af709e73cbac89a3187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc5b0198e5fab5c41103110ededd86617fe44991221a9c0b390d20b3b204de6`

```dockerfile
```

-	Layers:
	-	`sha256:c25390994fdfdb743369592917c8d4c022bf5adf5eb8adae4bca3f63cf71d71b`  
		Last Modified: Tue, 08 Jul 2025 04:49:42 GMT  
		Size: 40.7 KB (40729 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b22696afaf769b6a0f445b273aa4472b2f65687879d53e0ba77fbeb74fc7e32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190648132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6326d8e67eba842eec662d2da2e269f39e221a5ff3a2f31e5a8cd5e200e03e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:00:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:00:32 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_VERSION=5.1.9
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.9.tar.gz
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=cc0ddafa6fe6f5192236a27cec64e3466023a12c92c1da4abb680248639f678c
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:00:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:00:32 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:00:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa1406583f8460034b744a081db0fd06d6f3f1b350a17c5d5c2772f8fc1d5d9`  
		Last Modified: Tue, 03 Jun 2025 13:39:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b842a680302f3084d4e3bfb6508d71e259343131070338d1f21b9d0f945e2f5`  
		Last Modified: Tue, 03 Jun 2025 14:35:44 GMT  
		Size: 33.8 MB (33781170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0dd9bea5343b6958ca9be172e525f0197ea6669f8a976fea67e579a3cff2b9`  
		Last Modified: Tue, 03 Jun 2025 14:35:42 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61685b14a351086e6d78307545efb8b3dd8fbdc2e0c6f217447c9f1f8c5f230`  
		Last Modified: Tue, 08 Jul 2025 05:15:06 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3253f565347f9f958c803010a3170612712fccc1ea307098cd61506eb5218cc2`  
		Last Modified: Tue, 08 Jul 2025 05:15:09 GMT  
		Size: 74.7 MB (74706329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd507daac2ccb01718bec9ad7e250aab9041a4d91ab930bbfac07a4778dabb4`  
		Last Modified: Tue, 08 Jul 2025 05:15:06 GMT  
		Size: 1.1 MB (1096898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2b09fdcc166d35d7b3b226ce4e19480e1dee2afd5742a1e10842e1e3911448`  
		Last Modified: Tue, 08 Jul 2025 05:15:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844e75bb9e9289f9e0f572688cc8fdea2e573feafd19ba653db35844ba17601d`  
		Last Modified: Tue, 08 Jul 2025 05:15:06 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3778f34d849ba557a3130049a4be22e6532f95e4eb291b720dd3fa22cc08f0b`  
		Last Modified: Tue, 08 Jul 2025 05:15:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87ace008d6c45e040646d8c7597f7ca6bd8d236b6d00a67617b6a9a4852742a`  
		Last Modified: Tue, 08 Jul 2025 05:15:06 GMT  
		Size: 3.2 MB (3249973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e669bca943188693b06685f8d395780a35a1499d0af8cc0fdb9f4d79f4fa1f`  
		Last Modified: Tue, 08 Jul 2025 05:15:09 GMT  
		Size: 73.7 MB (73673842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7e90dba87f072a6a8e471d4b7a2c0f7bd43aded59508e40f4004b1da2c4400`  
		Last Modified: Tue, 08 Jul 2025 05:15:06 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:44bdebb9c9f7c907295a7c580ee9794b7074f2bacb52dcfed2c162afbc7a5d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271ba0f3863dab7f82502e01222e6827068db59c5164d820f0693b724613417a`

```dockerfile
```

-	Layers:
	-	`sha256:c6eed3ad17a950c8a0b3b746fadb9f280923b33cb25e7739e44ccfa509c2d07f`  
		Last Modified: Tue, 08 Jul 2025 07:49:33 GMT  
		Size: 40.8 KB (40777 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; 386

```console
$ docker pull redmine@sha256:922cb023f7b64de8f78a81b903c5426257c2a74e77f64f2a68bc928508faf0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (186992931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cdbeaf36bad0eb5b5f4e9e385551e1143bca8424711aabe090991cab1701d8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:00:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:00:32 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_VERSION=5.1.9
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.9.tar.gz
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=cc0ddafa6fe6f5192236a27cec64e3466023a12c92c1da4abb680248639f678c
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:00:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:00:32 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:00:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4400bdf10ac1b2186114bc821a98672b5d574f46d4bf117f1bcc90c755b346`  
		Last Modified: Tue, 03 Jun 2025 23:04:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d5b314548c1145dd3b8719975f7f00130c0aa5cfe2ac8eae48b4a5cdcf121`  
		Last Modified: Tue, 03 Jun 2025 23:04:10 GMT  
		Size: 29.9 MB (29941531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582fb7338a13319ae3b056839c91c11654917ac8d5a29168a472bce82f6df44b`  
		Last Modified: Tue, 03 Jun 2025 23:04:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f40d485a492f3cf504c1ac8ee92d8c5aac6cda3740c98b56043db2a23f0c80`  
		Last Modified: Mon, 07 Jul 2025 23:03:21 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7d3ea8c58be7c0ab58f5f6262c149beb0880137fd7d2d422e7c603ab1f8580`  
		Last Modified: Mon, 07 Jul 2025 23:03:27 GMT  
		Size: 75.8 MB (75835151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d90a6ff5c6ebd52168ca046b2e0e497c8baf4076c04c959adf2af579136339`  
		Last Modified: Mon, 07 Jul 2025 23:03:22 GMT  
		Size: 1.1 MB (1143835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70be44241065fd037f384308ef5b4304bdb1d63597d8c8d2af3f37e46f7074bc`  
		Last Modified: Mon, 07 Jul 2025 23:03:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c9ce8faaf25b06d4ed792c434e70e5e597183a4693382c8e2c6df9b63d8113`  
		Last Modified: Mon, 07 Jul 2025 23:03:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe514ea14beb6887b9fa4b1234937e3b69dceb49b449aff1165a1836429a85a`  
		Last Modified: Mon, 07 Jul 2025 23:03:21 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3c7bfac0693b3d48d26a461be77c77bac36f2badf78aae59a3090c527acb07`  
		Last Modified: Mon, 07 Jul 2025 23:03:22 GMT  
		Size: 3.2 MB (3249850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afe60345cda3b3660120ea6b3bdd7e9edefa8163a94421337195308d4e08590`  
		Last Modified: Mon, 07 Jul 2025 23:03:28 GMT  
		Size: 73.2 MB (73202556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a075ccca9d6490c76919c04a40f5dc1896b90a8a4dfaa13996d7990dcb727b9d`  
		Last Modified: Mon, 07 Jul 2025 23:02:59 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:ecfd2a81f7883a82f86d3ec297ae9d8697c6b1b6de5c02d62eb3ad0d58740c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 KB (40505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44cfb81273c85b28935449b7bd6f8a10d58470f70cd4d6fee800f14a1d0c235`

```dockerfile
```

-	Layers:
	-	`sha256:2aa8de603543fff0d24f89de4075def5f27554f9dcecc05b7712eef80e1df998`  
		Last Modified: Tue, 08 Jul 2025 01:50:00 GMT  
		Size: 40.5 KB (40505 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; ppc64le

```console
$ docker pull redmine@sha256:13c9386ccfa690e656c9ac49ed003e3b564fdc45b3dde067d79b65e2cf40c5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191643727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41489ff502cfbca41d323b29d1fa84b099fd17e4a095d783cd29af0f78caf906`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:00:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:00:32 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_VERSION=5.1.9
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.9.tar.gz
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=cc0ddafa6fe6f5192236a27cec64e3466023a12c92c1da4abb680248639f678c
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:00:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:00:32 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:00:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc492aa09ba6ba094b03567606500b7aa632647756572ee386cf287352e6e8c6`  
		Last Modified: Tue, 03 Jun 2025 23:12:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdfc1db593a3165e3f5b8bc813e1fea48847f84f9510e17b5a6390343269869`  
		Last Modified: Wed, 04 Jun 2025 01:50:43 GMT  
		Size: 31.4 MB (31411518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bc7b2603a6fa50956167504b50eca059e49492659fe38f853b189302836a30`  
		Last Modified: Tue, 03 Jun 2025 23:14:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97edee7fa9d1a410cd5179be5160fe12955f0550cb81ba4d469bf7aed39eda46`  
		Last Modified: Tue, 08 Jul 2025 00:50:53 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b863a4c40d9c5036c9c3ed5c743d66f110a92ecd95fb65d52b64887a1de1e199`  
		Last Modified: Tue, 08 Jul 2025 00:50:58 GMT  
		Size: 77.2 MB (77185385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c867e1cda86686dd6549ab71267296c0b50a4716aa12be046fccf51f6de7f5b`  
		Last Modified: Tue, 08 Jul 2025 00:50:53 GMT  
		Size: 1.1 MB (1087418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63a7a146035b08a359602f722a56da8a935d44b20ea4c4f81aadb71ed6451b`  
		Last Modified: Tue, 08 Jul 2025 00:50:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034224a34d0b377eeb091e32c929772e7031a5b43164583a67938185436df63f`  
		Last Modified: Tue, 08 Jul 2025 00:50:53 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8956aa2c881a5d0b891d677c1a3d28129634bb3fc51544a1ed9f9c2413fea1`  
		Last Modified: Tue, 08 Jul 2025 00:50:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1b822c50808fd7eac314cfff193ec21b5ed8d9ea6b5504f9c57c0c16904a4a`  
		Last Modified: Tue, 08 Jul 2025 00:50:54 GMT  
		Size: 3.2 MB (3249874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ca7ad2ce701ffaf66e47dabfd487219fb74c8dcf7cda2c489e5f58e1ec861`  
		Last Modified: Tue, 08 Jul 2025 00:51:04 GMT  
		Size: 75.0 MB (74975369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6621990434a7df68c262f277426b6fa53e49f7fa808de01d3bd8e064840ef719`  
		Last Modified: Tue, 08 Jul 2025 00:50:53 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:581f021461bf05537697e8322a19090f791996c8c0dca12443e5b0aa19708a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280c54c47c6d8d29fe5a9902ed438b8636e3f641119ed6e3df1bdd5a688e0250`

```dockerfile
```

-	Layers:
	-	`sha256:013f03e83e3d753e014340438470cd0e71941df8e817821d84865f52a078e6cc`  
		Last Modified: Tue, 08 Jul 2025 01:50:04 GMT  
		Size: 40.6 KB (40627 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; riscv64

```console
$ docker pull redmine@sha256:c6244e967991381151b931da25800e89137aa74b2a26561d0c8cf4e5ee13f943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183812329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c726d343fd51a5810e1f19727e034588e074cab7c2ec527b109ba8b9f683b843`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Fri, 30 May 2025 21:26:15 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_ENV=production
# Fri, 30 May 2025 21:26:15 GMT
WORKDIR /usr/src/redmine
# Fri, 30 May 2025 21:26:15 GMT
ENV HOME=/home/redmine
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_VERSION=5.1.8
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.8.tar.gz
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=50a30cd16c43d0ae64f256866c8cef4b0e9dd818d6feef489fa24507fbde3a7b
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 30 May 2025 21:26:15 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 30 May 2025 21:26:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 May 2025 21:26:15 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 30 May 2025 21:26:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b27f4dcb19381de3632bdf83ba047ff02e37c9fec5aa239238c22a48c3abba`  
		Last Modified: Wed, 04 Jun 2025 00:11:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccd72ca850fb7f2cbbde33208d008fc0ba07f9e11b17b5ec4aa3228514b7b73`  
		Last Modified: Wed, 04 Jun 2025 04:49:55 GMT  
		Size: 29.8 MB (29823122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01383d5f50102cd2c86c6a05ed83871bcb1f03e628b63fee0f6fa10d2eb0fb85`  
		Last Modified: Wed, 04 Jun 2025 01:15:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476406a8e6c5a5147f500a847c6a7678525633a601ea037da7593cba2cb15da9`  
		Last Modified: Wed, 04 Jun 2025 01:07:16 GMT  
		Size: 915.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c682515ecb8f32d9d86a95b241ed92078e8a658cc3e4347327cc4bcb373b9b7e`  
		Last Modified: Wed, 04 Jun 2025 01:07:22 GMT  
		Size: 72.0 MB (71970766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cad97958a58ce7fecaf7ae68c77c9a92aa4c6f1c6c606cd8348b848b2d74fb`  
		Last Modified: Wed, 04 Jun 2025 01:07:17 GMT  
		Size: 1.1 MB (1137263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fd84ad7779505c9d79b08a29b9446c7fd97427f3d5607fad84a56171408171`  
		Last Modified: Wed, 04 Jun 2025 01:07:17 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673133e1b6ec780ebeea46b2c6dea292731429f7ab5de68fea523ab48a9ddba3`  
		Last Modified: Wed, 04 Jun 2025 01:07:18 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5436e774ac6e6c8bc1b3ba8ec2300b7693227458939e111334a4d82b6b429`  
		Last Modified: Wed, 04 Jun 2025 01:07:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c2a666a3cecd63c17350f7661a4dd5ddaca88065a2f6bed7df314b39a9faf`  
		Last Modified: Wed, 04 Jun 2025 01:07:19 GMT  
		Size: 3.2 MB (3248074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc33d12b85b9120ca772c99cf0f6806d4580e3220907b883a507bac59b09123c`  
		Last Modified: Wed, 04 Jun 2025 01:07:23 GMT  
		Size: 74.1 MB (74115314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9f413125defb7072b2b39a1337ca2f7b67cf2243723752c7eb35543f2d9b94`  
		Last Modified: Wed, 04 Jun 2025 01:16:52 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:791100ebb206c265d998afa59ef4904caabda315f0ce4c58b098c6a7e69068d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c302b50eb367b46a450a693b76592616d27c748a0aef0743497c4da80f2d8473`

```dockerfile
```

-	Layers:
	-	`sha256:8741adfc4d767bacd31c3773878f81207199167cd72e57e00b3e184988ad0702`  
		Last Modified: Wed, 04 Jun 2025 04:49:36 GMT  
		Size: 40.6 KB (40626 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; s390x

```console
$ docker pull redmine@sha256:7d332750dba1f003689241fe5380e1382990bbc43884e9415a7f71e58b87a902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187647942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821eca09d18c812ef9dc06f090ec6c2b5a14c169746de35da1dee7b0dae9d93c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.2.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=1cccd3100155275293ae5d4ea0a1a1068f5de69e71732220f144acce26327a3c
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:00:32 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:00:32 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_VERSION=5.1.9
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.9.tar.gz
# Mon, 07 Jul 2025 22:00:32 GMT
ENV REDMINE_DOWNLOAD_SHA256=cc0ddafa6fe6f5192236a27cec64e3466023a12c92c1da4abb680248639f678c
# Mon, 07 Jul 2025 22:00:32 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:00:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:00:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:00:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:00:32 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:00:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0d9969f70d5a36f4277e7e9319832436722d175377dcf99975210c3a9b5eeb`  
		Last Modified: Tue, 03 Jun 2025 23:15:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e2cc0ed7b6fdd78178db804414668dfba662b6fe799e16c50c09ecf4b877b1`  
		Last Modified: Wed, 04 Jun 2025 01:50:41 GMT  
		Size: 31.3 MB (31263281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4edb676af518fe0b9b03ae69493ffbb1c6501eeb523535198f7e2bc3eab26`  
		Last Modified: Tue, 03 Jun 2025 23:15:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f767a8b0211ea98afd9e11b852fc29d77d9cd68738733a688ebc2dbc1d49e830`  
		Last Modified: Tue, 08 Jul 2025 03:56:24 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5b504a7a179d0204bc7c62a278352da0ec485da2ed6dfaeec5ea1375242929`  
		Last Modified: Tue, 08 Jul 2025 03:56:30 GMT  
		Size: 74.0 MB (74041397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dab8acbacc74fa051541012cddfbf7209006be59a0fb38989f4862c21c6e25b`  
		Last Modified: Tue, 08 Jul 2025 03:56:24 GMT  
		Size: 1.1 MB (1131784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4537d616c13da8121109501601f32672db743992a4dd2ec85cb0dae152bebcb`  
		Last Modified: Tue, 08 Jul 2025 03:56:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced92a0d55aef364e0e2dcd5c2d1d04c20cad4a0e965cdd15104468866ad017f`  
		Last Modified: Tue, 08 Jul 2025 03:56:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a54fc3b60406e70b510067f6796e2cbbd4912fd56a124b9c81ff1029c28db29`  
		Last Modified: Tue, 08 Jul 2025 03:56:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7eaa61ca4c785117441815b543959bc7a431d561b823148203c277edbaaa55`  
		Last Modified: Tue, 08 Jul 2025 03:56:25 GMT  
		Size: 3.2 MB (3249964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c5db1f7d63fa7abd627499b45052ec0ae0922d487dac1e2c3457ac9f26c82a`  
		Last Modified: Tue, 08 Jul 2025 03:56:32 GMT  
		Size: 74.3 MB (74310009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c177a2455ede1957d6854b0eb1a75a8075605b06fea7595ee889a341d60d02ea`  
		Last Modified: Tue, 08 Jul 2025 03:56:24 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:f96e2094685c68f5d868d2b812d0b75d3f868636ae983bfab426b52b1a6c191a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e125fbc22b73f8a6b89309d3144524c6c782ba74c247e7b68ef8178bc6e57ce`

```dockerfile
```

-	Layers:
	-	`sha256:4007c1d5fa9ec57dba40b9ab787a6bf6afee477db3a7c82ea6fdae20dc2fa7e6`  
		Last Modified: Tue, 08 Jul 2025 04:49:52 GMT  
		Size: 40.6 KB (40559 bytes)  
		MIME: application/vnd.in-toto+json
