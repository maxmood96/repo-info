## `redmine:alpine`

```console
$ docker pull redmine@sha256:201bf4c5d57d262e22ba1c885678408b7492e4f0f4ab463ff305dc0d61a9251f
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
$ docker pull redmine@sha256:0ef51811cf7404c62d6d14fe5fe8c428e77c1fa46b87f137cb2d604cb7e6b160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195290328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3869d4de5aade321ba3a42cdfe3411a607c85877309e9d40948f848a82bba08d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV LANG=C.UTF-8
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_VERSION=3.4.6
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
CMD ["irb"]
# Wed, 24 Sep 2025 15:00:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Sep 2025 15:00:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
ENV RAILS_ENV=production
# Wed, 24 Sep 2025 15:00:28 GMT
WORKDIR /usr/src/redmine
# Wed, 24 Sep 2025 15:00:28 GMT
ENV HOME=/home/redmine
# Wed, 24 Sep 2025 15:00:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 24 Sep 2025 15:00:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 24 Sep 2025 15:00:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 24 Sep 2025 15:00:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 24 Sep 2025 15:00:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 24 Sep 2025 15:00:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 15:00:28 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 24 Sep 2025 15:00:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eaeec204ac0d74a964ec358b0e8f0357e9b550f813a3074a14d2c125e48e53`  
		Last Modified: Tue, 16 Sep 2025 17:09:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4dfe5f98ee0518caed06bae663dd796bf5f363d506268a4f3335ff7b169495`  
		Last Modified: Tue, 16 Sep 2025 17:09:59 GMT  
		Size: 41.8 MB (41771213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5c8600158fb724f427940dfacafa3b7e2bd2363fc080f116445ddb29d0732a`  
		Last Modified: Tue, 16 Sep 2025 17:09:50 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0c6dde3a312056a1cb9e8ef9c5bf9d0e8db74b4b15845cdd97967d36e0bc65`  
		Last Modified: Wed, 24 Sep 2025 21:32:28 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3d9d9b8f53b4a6b078507eb2c6125a2b2b990bf2194967dabd6b60f660a172`  
		Last Modified: Wed, 24 Sep 2025 22:52:47 GMT  
		Size: 75.4 MB (75377240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf4d2fa9a8b255c307263ea9f1d76bf6da55632263872212eccb7ed19b3f3ce`  
		Last Modified: Wed, 24 Sep 2025 21:32:29 GMT  
		Size: 966.5 KB (966470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da8a8bcb49231855a0f759fb2409279e4be16cd57d81f764d8c241337f6f04`  
		Last Modified: Wed, 24 Sep 2025 21:32:29 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d70e44962729ecc9cd872da4f47e136223bf22c342d300fafa4e356e73303c`  
		Last Modified: Wed, 24 Sep 2025 21:32:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae85e9074a1e17050981a03e126e95eaf37df0d9515bdda3c18f9145eb7c334e`  
		Last Modified: Wed, 24 Sep 2025 22:52:44 GMT  
		Size: 4.1 MB (4140804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b365358eeb45da45fbc9afbcddc4ed774880b03b20c907d4eee9a1af2f14675e`  
		Last Modified: Wed, 24 Sep 2025 22:52:48 GMT  
		Size: 69.2 MB (69231063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8961fd1f6f4ecd14366f8334400ea43dfa47e76606e3e9bc2b0c46a81a036e07`  
		Last Modified: Wed, 24 Sep 2025 21:32:27 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:c12d601c137f76b3e45f30160f7e977e0d811c296a672c3f5898df2c79173a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f220ad26716f38f091ecf84bf2e8b01cd18bd4a27221eb134292989fcccccac`

```dockerfile
```

-	Layers:
	-	`sha256:e48016da5b84081e35f4e9b9284abbf30c7b0704bac907bb3e08e6599ea00b17`  
		Last Modified: Wed, 24 Sep 2025 22:52:21 GMT  
		Size: 37.8 KB (37800 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:c745d89ab996e33f1dbbb4c593f4b6ca0af969a7df459a482c4e1633b35a3ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188007096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180b13a9c864ae4c053cf024bb367b90c1617c0a890b85826518d9c894b5f197`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Tue, 23 Sep 2025 19:31:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_ENV=production
# Tue, 23 Sep 2025 19:31:28 GMT
WORKDIR /usr/src/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
ENV HOME=/home/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_VERSION=6.0.7
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 Sep 2025 19:31:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 23 Sep 2025 19:31:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e749f40903fc8c363b20271f0d659c019b7541c985c0fff98929bd8f47ad95d7`  
		Last Modified: Wed, 16 Jul 2025 03:10:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d1d4e03a7fbecd69c3a28cf026859ddd2ac815af3d86ceb0e550ba1c72366e`  
		Last Modified: Thu, 24 Jul 2025 18:29:14 GMT  
		Size: 32.1 MB (32100277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7128ae21f785e1b4597a019e0af372c3f8295d8c4637decedc296f3dee17ab09`  
		Last Modified: Thu, 24 Jul 2025 18:29:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa258513a168c3015bd3959639b82dfebb5baecee9f5f6dfae967621653465c7`  
		Last Modified: Tue, 23 Sep 2025 22:08:04 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0708a200d7b51ba7d36c5bf1189b2156ab5217f8c220de6d4822c96945a4206f`  
		Last Modified: Tue, 23 Sep 2025 22:08:10 GMT  
		Size: 72.2 MB (72158505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab7357c9c317c20d3e16feca3987fe1a9dfd60d641049bb7dc081d055e82000`  
		Last Modified: Tue, 23 Sep 2025 22:08:05 GMT  
		Size: 934.6 KB (934560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbd12c4b14004a5de37ce206a6c8e4242d0c8708fa009c5e70ec27344bfd37f`  
		Last Modified: Tue, 23 Sep 2025 22:08:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477ebcc9df71e18b19f67bab709a318885d47f1b3ce358d8071b216e4321f779`  
		Last Modified: Tue, 23 Sep 2025 22:08:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3d03b9026bfc0b210a03e8940548b8ce370d101367c8eff9e0832f54bc932a`  
		Last Modified: Tue, 23 Sep 2025 22:08:05 GMT  
		Size: 4.1 MB (4069887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ce139063ce517dfd5fbe8cc066163604fc87d10e0753453a9c9bbd70911025`  
		Last Modified: Tue, 23 Sep 2025 22:08:11 GMT  
		Size: 75.2 MB (75239110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e89a43a0aafe9de85e87fd5b176b504551a3fb8bd60352a3aa944b03f72fb`  
		Last Modified: Tue, 23 Sep 2025 22:08:05 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:fcd158ea13ed5eac0aaec3768826bbe46a6674bfdf992897b52759fa76c4a342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d72cb6602f286bafe0a2def0f2f88a7f2a9b921b8ec9d307e0e581a4d5f070`

```dockerfile
```

-	Layers:
	-	`sha256:e35e33d9eba665a858c5dbe17a57ce39a765569bd55e50336815d1afc22432fc`  
		Last Modified: Tue, 23 Sep 2025 22:50:51 GMT  
		Size: 38.2 KB (38186 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:51acd27902f17d3cb95dbbc82d35376f9c8b48f031389d10ecb09f9449b3511c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183256527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e687ccfa903a00759db2bd66310f104296494727c57151431af89be6d174db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Tue, 23 Sep 2025 19:31:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_ENV=production
# Tue, 23 Sep 2025 19:31:28 GMT
WORKDIR /usr/src/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
ENV HOME=/home/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_VERSION=6.0.7
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 Sep 2025 19:31:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 23 Sep 2025 19:31:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b77cd865d0c67b298abaf8807a4136a70f54c59294ed70401ffdb2b65368440`  
		Last Modified: Wed, 16 Jul 2025 03:17:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b481856eb3c874e37881028cbaaf3a479dc287401717803c9da0f17821e9ffbc`  
		Last Modified: Thu, 24 Jul 2025 21:53:31 GMT  
		Size: 32.0 MB (31962302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bb1dd3d36ebe4fd18546b9cb64247d00ed316bcbf544f675adcde41f8f62b7`  
		Last Modified: Thu, 24 Jul 2025 19:00:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59189fb8a7e1ec4d18dddf4e5e607da344a209502b86cba5df0cd9b368f3aa48`  
		Last Modified: Tue, 23 Sep 2025 22:18:54 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3354d3e076139be94a0188d5a6155b737a9b703f0fc35c0b6789d2b678a30963`  
		Last Modified: Tue, 23 Sep 2025 22:19:21 GMT  
		Size: 68.9 MB (68946757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c66b82020d4f6b421672f2ad67c22c3992933e1c04c2e655b0063867157953`  
		Last Modified: Tue, 23 Sep 2025 22:18:55 GMT  
		Size: 934.5 KB (934533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d73596f99400532463b44ebfeedfc865c8f3c4d47f7e981c99da370675b96c`  
		Last Modified: Tue, 23 Sep 2025 22:18:54 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bd4a216f001262610b20febf08bf22376d13698b4330657daed0d9e999af68`  
		Last Modified: Tue, 23 Sep 2025 22:18:54 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c50671b1687a6ae34a9317c2aa26ab270f86e8deaaef671aebf3050362c58df`  
		Last Modified: Tue, 23 Sep 2025 22:18:55 GMT  
		Size: 4.1 MB (4069888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4841937b95f75c80488c8b3fee1019f9729c646578f402494239014d75e9a3`  
		Last Modified: Tue, 23 Sep 2025 22:19:21 GMT  
		Size: 74.1 MB (74120162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d448719fcb750ea5962c567ce67cbcdedd6e55483c11d24fbf12cdddcaa19af`  
		Last Modified: Tue, 23 Sep 2025 22:18:54 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:b1e2ac214fd510b9d1972f6592ee63a6bf48d72c740b95c94be62c4046f0e82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ae8b671e7f3cd884e66f4febdf54bdc305cad3513eb58e34481b996ea37495`

```dockerfile
```

-	Layers:
	-	`sha256:1e3aadf64fcc24887095d034e3774fd82ba7deb61ce29779a96c212edce10a40`  
		Last Modified: Wed, 24 Sep 2025 01:51:25 GMT  
		Size: 38.2 KB (38187 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:474587b8de305c21a62a084e8a3b7a37f0f935ef58ce71f2f4f60912fcede9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195522724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd301a344f01717795bfe590b0a3a79adeafdc75192c7bcd0fab562c4a403a95`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV LANG=C.UTF-8
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_VERSION=3.4.6
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Tue, 16 Sep 2025 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 16 Sep 2025 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:03:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 16 Sep 2025 05:03:19 GMT
CMD ["irb"]
# Wed, 24 Sep 2025 15:00:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Sep 2025 15:00:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
ENV RAILS_ENV=production
# Wed, 24 Sep 2025 15:00:28 GMT
WORKDIR /usr/src/redmine
# Wed, 24 Sep 2025 15:00:28 GMT
ENV HOME=/home/redmine
# Wed, 24 Sep 2025 15:00:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 24 Sep 2025 15:00:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 24 Sep 2025 15:00:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 24 Sep 2025 15:00:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 24 Sep 2025 15:00:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 24 Sep 2025 15:00:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 15:00:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 15:00:28 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 24 Sep 2025 15:00:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e1c50668d374fdca212bb850a7162e63fefcd3ff38b92cc13f63d7b78a39b`  
		Last Modified: Tue, 16 Sep 2025 17:07:10 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a4835974407bc0241f939e4477f5f37b187366ad894a9a514397ea38f462d3`  
		Last Modified: Tue, 16 Sep 2025 17:07:07 GMT  
		Size: 41.9 MB (41926761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd9429e9cf13a39b507e2517331b5635961f47c76155da3161ddadafa4922d8`  
		Last Modified: Tue, 16 Sep 2025 17:07:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c89deb5d1ed52dafed909eee6fc91f8a4fc900c82a60ddac1a2374c68365ed`  
		Last Modified: Wed, 24 Sep 2025 20:34:24 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8476e8f225212b12a529c5489f707f790388fe84e23529c6b6734a4592e99c9`  
		Last Modified: Wed, 24 Sep 2025 20:34:35 GMT  
		Size: 75.0 MB (75019742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04269212fca7a27048c394501eebc5585ecd25b7a89089a6ff510d646176a10e`  
		Last Modified: Wed, 24 Sep 2025 20:34:25 GMT  
		Size: 922.1 KB (922117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aa0a513600389d3cfa898af586883626aabf67de8001507f2f233a787dd3b4`  
		Last Modified: Wed, 24 Sep 2025 20:34:25 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2b6549364a40a67e7bdde0706dc32ce015a301ba98bf3ad9d962d2cb6e909a`  
		Last Modified: Wed, 24 Sep 2025 20:34:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22609c5e6202e9398a625a527e0ad43b13a02bbc5553ddf7511306618d8d06`  
		Last Modified: Wed, 24 Sep 2025 20:34:26 GMT  
		Size: 4.1 MB (4140828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2bff1c5ad1c73ef5d29c97154192443d050e600df5f7425ae2765f34d5fa4c`  
		Last Modified: Wed, 24 Sep 2025 20:34:35 GMT  
		Size: 69.4 MB (69378674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec25f286633d9f6a39c2253872915d56d20d85711fd3f52534300edf52271ca4`  
		Last Modified: Wed, 24 Sep 2025 20:34:26 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:a48357cd94d1da053128fa6f2ad611fed30cb8c746fa300108373bbfd83ae9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f8bedb0e80d6668a7f2ecf34f2f191f335810323aeb87d328e69073557d96a`

```dockerfile
```

-	Layers:
	-	`sha256:a2a909f379ee89f683288d83364182dbd9f2626e5da5ae7366ed8dd78b680b2f`  
		Last Modified: Wed, 24 Sep 2025 22:52:29 GMT  
		Size: 38.0 KB (38027 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; 386

```console
$ docker pull redmine@sha256:5cb0a727fb9efe96bcaf165cd33148de1a8d584c34d47f63c59955247cfce517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193032379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80959db6d6a9bb2472a8abedde4745e2a2b26cea77113f612b05831b083974b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Tue, 23 Sep 2025 19:31:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_ENV=production
# Tue, 23 Sep 2025 19:31:28 GMT
WORKDIR /usr/src/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
ENV HOME=/home/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_VERSION=6.0.7
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 Sep 2025 19:31:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 23 Sep 2025 19:31:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12b7eb52fa449c9b0aba432b977e6b0695fd9ec6ced94b5ae2d0917d747934e`  
		Last Modified: Thu, 24 Jul 2025 18:29:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221c1aaa8074b3e6c17171630b3cd5d659ad539494c2e15a3a24766d7159e80c`  
		Last Modified: Thu, 24 Jul 2025 18:29:49 GMT  
		Size: 32.0 MB (31978271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eca6b1e23b2530f3d6e9be64a8b96278ba90e83cf48cba3ef556a16ffc22aa`  
		Last Modified: Thu, 24 Jul 2025 18:29:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7150ea0f0c7946fe345630c0e366aae5627eaa907980814d8ed4a649dd4790cb`  
		Last Modified: Tue, 23 Sep 2025 21:54:58 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f4d414348356ea398523c6ab1ba1a1e1a2be0b5d44262a6310a13bb40715af`  
		Last Modified: Tue, 23 Sep 2025 22:51:25 GMT  
		Size: 76.1 MB (76129841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e594df47240ac202b7a4c45bac0eb289d654aa260e33dc3f62bfb95c19b504`  
		Last Modified: Tue, 23 Sep 2025 21:55:02 GMT  
		Size: 939.1 KB (939051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257210261890ba9460bb4b1730dd4d1e2b08dc061e4622140017027c04af533`  
		Last Modified: Tue, 23 Sep 2025 21:55:08 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee7aad810f191e2b2b951c7f5379c701205965a2e1e786c665f1804c5f0772e`  
		Last Modified: Tue, 23 Sep 2025 21:55:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124b20e761aed8f2bcfb21868a6aa09a77be77fc9c24b6eecfe1e2a69e9d6b66`  
		Last Modified: Tue, 23 Sep 2025 22:51:12 GMT  
		Size: 4.1 MB (4069757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dba3fe6118c681455cdee55e119f823794e045396adcab0d21de7301d5a222d`  
		Last Modified: Tue, 23 Sep 2025 22:51:27 GMT  
		Size: 76.3 MB (76296598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4ce9735a4be63547ef9c00352b9b9a5e311174d3c50b7f58ae8a91e88e31fd`  
		Last Modified: Tue, 23 Sep 2025 21:55:15 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:b7c9ad4d538d5dc31bc5acd109cfeb9a234d88aef2695c98eb584b8b4785efbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45e299be9f0496d01e343042024b31aebb633cad27af0d36986a57670e120fc`

```dockerfile
```

-	Layers:
	-	`sha256:4cabb91a06ced4b6f9a260d2fed737097ee24fa692820f2a162185ee7939c858`  
		Last Modified: Tue, 23 Sep 2025 22:50:59 GMT  
		Size: 37.9 KB (37948 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:64d39a34edc0fc4bb62284c7b7705dd788357f3160c23c76d9b644adf510acac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197734037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe38ae7f27c61046feeca125445b81d03fffd799bbc49ce49317ffd01d510e13`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Tue, 23 Sep 2025 19:31:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_ENV=production
# Tue, 23 Sep 2025 19:31:28 GMT
WORKDIR /usr/src/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
ENV HOME=/home/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_VERSION=6.0.7
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 Sep 2025 19:31:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 23 Sep 2025 19:31:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897bcad2380e05e6ccb43d1c1224d66ccbf31e39c5f494a35ffd42393b648798`  
		Last Modified: Wed, 16 Jul 2025 00:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52155cbf6e208386f6f5ab022c61b2787741d2cda534bbbfaa6fcfb7193058d4`  
		Last Modified: Thu, 24 Jul 2025 21:54:13 GMT  
		Size: 33.5 MB (33483243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac33a1359538c744e6ee0e1e9f1e5e83e4f173b979f34ee371c080a1627bea54`  
		Last Modified: Thu, 24 Jul 2025 19:01:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c1eaf7b242a70306211165ca128623a3509e82ebef4280f7198a7cb26d98be`  
		Last Modified: Tue, 23 Sep 2025 23:18:09 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd6c8d33afe33e3488dd1c5c6e1adbc21d24646e39630cac9d75875413a3b7`  
		Last Modified: Tue, 23 Sep 2025 23:18:03 GMT  
		Size: 77.5 MB (77463454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588d0b1053ab7d67c5d079bbb9e7f57ed106415e8970099bbc63d8749e9eac19`  
		Last Modified: Tue, 23 Sep 2025 23:18:09 GMT  
		Size: 927.6 KB (927582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9d30d050aa34a9fe799a9e7b28071d285dbfb52eeb6f9e3071d807478b5c6`  
		Last Modified: Tue, 23 Sep 2025 23:18:08 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fa2b508712e9468e17f41cd3c7a050fecfd78af9c1834e048ff325f6622841`  
		Last Modified: Tue, 23 Sep 2025 23:18:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e7477a998f4b2471db068df989fce8c2dab96294733c8b89639c75a3998465`  
		Last Modified: Tue, 23 Sep 2025 23:18:09 GMT  
		Size: 4.1 MB (4069895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdb38332e6ff0df40295f08274abbcc1e07107c620f230aa5f6c9c0c3edece3`  
		Last Modified: Tue, 23 Sep 2025 23:18:14 GMT  
		Size: 78.1 MB (78058900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299e8acbc1e0c2df3f66014dc0ea8516b89817d77c8ad4b2d497912d73979921`  
		Last Modified: Tue, 23 Sep 2025 23:18:09 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:b835ce991e87247608eb48471ce3be1a9d00922c82790a79474e1500a494623c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c4cfc6beb998d07367d99908c798bea89a2c73d9adf5eed3c2a8fe7b3a7412`

```dockerfile
```

-	Layers:
	-	`sha256:c05b67543049442576884dba34bd8d71c6f6b06a3a28296b989c8b992a8d3f02`  
		Last Modified: Wed, 24 Sep 2025 01:51:31 GMT  
		Size: 38.1 KB (38087 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:ea8be7be6a1a3004486c3ff400f9b0ec005900aacbfeafc145da1e7cbd2b6c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191980816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2b507217c13107d7b396db89c8c53e0da228058c6d3f0678ee7acc1d0782f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Sun, 21 Sep 2025 14:39:20 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:39:20 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_VERSION=6.0.7
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Sun, 21 Sep 2025 14:39:20 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Sun, 21 Sep 2025 14:39:20 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:39:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:39:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:39:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:39:20 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:39:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3905288231d9db3a0fab057825d486ad746db59697d750f674f00bfeee979f9e`  
		Last Modified: Fri, 18 Jul 2025 01:30:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f8a218f941e8f339d4b366b40dd1beb052449325260e342be2a8eac783b50`  
		Last Modified: Thu, 24 Jul 2025 19:52:23 GMT  
		Size: 31.8 MB (31771158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70ca7f3fc9114d11cadb7a27959f03e1f0327a2c4f7ae2d4bf8f622f7669f9f`  
		Last Modified: Thu, 24 Jul 2025 19:52:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7bf8178196c5666501cce1ca98a2e58bf388fd450db239cb47c3a5f4963149`  
		Last Modified: Tue, 23 Sep 2025 02:26:56 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3490a77886c3666116ba293b5a80989dd52dbca8493f70cbfea74d073e1caa9f`  
		Last Modified: Tue, 23 Sep 2025 02:27:12 GMT  
		Size: 72.3 MB (72283343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146424d1a879546da4ad0acdef62b5a66a77f89aa1399911cd5e6690b21d541`  
		Last Modified: Tue, 23 Sep 2025 02:26:57 GMT  
		Size: 913.9 KB (913925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399f2fb76e5ca3a1e20d6fe83b7d57fb0d9744d1c7197062b5d62d9a184f6f86`  
		Last Modified: Tue, 23 Sep 2025 02:26:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ba3f253d3863c98bb6a31f4333bd7443a698c7846d2576978a00b93625f1fd`  
		Last Modified: Tue, 23 Sep 2025 02:26:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26105c3033a32f77ed3adb0a74428adcc0927c7db4acd5a8f68d9ed391386fce`  
		Last Modified: Tue, 23 Sep 2025 02:26:55 GMT  
		Size: 4.1 MB (4069934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e2a68faa98b0e6d55dc0d8075c6d64f1dcef5ab1d1583f027486a0403dcff`  
		Last Modified: Tue, 23 Sep 2025 02:27:00 GMT  
		Size: 79.4 MB (79425803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5369f338654dcf4979c0d22601b560e74236fb5bb9203141bf79bdfe7d50edb2`  
		Last Modified: Tue, 23 Sep 2025 02:26:54 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:6002f0b5f219ae9678804f5f9c0bd90180c4bf7c6310261b411790517b519547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eeb449951c6a91adfec1464a883b8dec589e43af73d371f9fa0a0b896d0b1bd`

```dockerfile
```

-	Layers:
	-	`sha256:3a63a387bdd58e17b9a61041957adecf4e5b5628bba521627b7aa689a0234cd4`  
		Last Modified: Tue, 23 Sep 2025 04:49:51 GMT  
		Size: 38.1 KB (38088 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; s390x

```console
$ docker pull redmine@sha256:618472beb8442a39bca4b11876509a6b23b7a07372c44d93cad58e6c061ddf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193673635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171125f2237c656b1e81c94df580bee872b1cea3e362184db826797af0be1cea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_VERSION=3.3.9
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Thu, 24 Jul 2025 11:34:09 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:34:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:34:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:34:09 GMT
CMD ["irb"]
# Tue, 23 Sep 2025 19:31:28 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_ENV=production
# Tue, 23 Sep 2025 19:31:28 GMT
WORKDIR /usr/src/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
ENV HOME=/home/redmine
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_VERSION=6.0.7
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.7.tar.gz
# Tue, 23 Sep 2025 19:31:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=8824560a07673dc7b59f1ca0bf9d7cd854c6c4c97d0fe555a5dbeba332b8dfe8
# Tue, 23 Sep 2025 19:31:28 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 23 Sep 2025 19:31:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 Sep 2025 19:31:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Sep 2025 19:31:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:28 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 23 Sep 2025 19:31:28 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b165588f00306099ed574634bb65ed4b9211498ade906a1602cb03e077aa2e4`  
		Last Modified: Wed, 16 Jul 2025 04:41:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be42f89d9caa3bd043bf99687a891c112e45683b83a72b13f1bd1aa688072413`  
		Last Modified: Thu, 24 Jul 2025 19:51:51 GMT  
		Size: 33.3 MB (33270320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4861d5d86889f08573cbf3a1565450c7be782596e326ea404fc5e6bed9bdfa12`  
		Last Modified: Thu, 24 Jul 2025 18:45:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cb375a3fced5f9efb322e32254e3e918c5e2abd52a71ce99a7ab51a7960efe`  
		Last Modified: Wed, 24 Sep 2025 01:15:51 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b8276c216b4e785ca7159b8e4421c266116b331f456b2152a2174370712837`  
		Last Modified: Wed, 24 Sep 2025 01:16:00 GMT  
		Size: 74.4 MB (74364907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870520b25960fac4b7ad220d65989fd9c646673e76588f108bfba9d8ac3fc8b`  
		Last Modified: Wed, 24 Sep 2025 01:15:52 GMT  
		Size: 943.2 KB (943153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4236f96e911a1423208b09e5816372874fbcfa6e812ab74b2619d37b4f1d0c13`  
		Last Modified: Wed, 24 Sep 2025 01:15:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292b31c56acef737fd76ebb5a054c49b1f7b5ccaf08cf46121068fdb693c77ac`  
		Last Modified: Wed, 24 Sep 2025 01:15:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30941c0a28300a1e9a76df05dbbb4d4e28ee3bec62789fda0213aabf8373d6a3`  
		Last Modified: Wed, 24 Sep 2025 01:15:52 GMT  
		Size: 4.1 MB (4069882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85148885c5fe88271a378188f7e5fbc3e6f5c614672a12f15a1b2a674d3a450e`  
		Last Modified: Wed, 24 Sep 2025 01:15:58 GMT  
		Size: 77.4 MB (77376555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b6d9550fcc2f90c137bd2b5ce735d80fd5487bd734bced7ce6d4cb28c55b70`  
		Last Modified: Wed, 24 Sep 2025 01:15:52 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:3d413c049295c33a114dda79593961e86def1ec461c0e2cf0839f7b78cae96b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66364623a2e461f075e44a477ee005b28e89bffdfdb3e6bdb2629abf1280fc4`

```dockerfile
```

-	Layers:
	-	`sha256:968a65a3a022bcd4d3f20b48cfb95c8f511eb1083b1e17ebd75db7df3e5103ab`  
		Last Modified: Wed, 24 Sep 2025 04:50:37 GMT  
		Size: 38.0 KB (38009 bytes)  
		MIME: application/vnd.in-toto+json
