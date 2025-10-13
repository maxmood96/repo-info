## `redmine:6-alpine`

```console
$ docker pull redmine@sha256:84b471f3c86ed0d35000ced90415f72b5d6138299d21c84ec91c1ed049c3ceff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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
$ docker pull redmine@sha256:03884685aeef52e6ae1ec23f2650dbe6cac81259f720f495a5310e3075c13e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190307541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608aa808aa838edfbe51b972a009a26251ff153907a79cdfe56f7f42c6fcc752`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6451b1d524d7c9191c1a3ec5ea1d187c29c51df71efc2acc953edf0855e29a`  
		Last Modified: Wed, 08 Oct 2025 23:19:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a662f20494e53cff5ee6fd1c1f4b7317ec31dd22d39cbb457af58edacdec32`  
		Last Modified: Wed, 08 Oct 2025 23:19:30 GMT  
		Size: 39.3 MB (39312605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45999a133a1a615882cb5ba6fedc2d68bbbd54eac730c7895000c845da4fe1dd`  
		Last Modified: Wed, 08 Oct 2025 23:19:28 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25033f3176418d868716366d1b371ac558af0e0dcc0890271adf073a06b3d40`  
		Last Modified: Thu, 09 Oct 2025 17:26:06 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5857cc09421399d68aac7afbbffb0171a71d97deee50ebde513cc24cffca179`  
		Last Modified: Thu, 09 Oct 2025 17:26:12 GMT  
		Size: 75.4 MB (75403458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15cc2eae58e1dbc430c205f5b22c66b974558626224f78b062edae98d9f4d73`  
		Last Modified: Thu, 09 Oct 2025 17:26:06 GMT  
		Size: 966.7 KB (966703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6098852ffa72fb78310f9bd938ff3b797e59d70175230091e5e57cdf45b233`  
		Last Modified: Thu, 09 Oct 2025 17:26:06 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8e6d4ea48e683138b777d035c2e15a53b9ddf1553afc1893a83b7cdefebee`  
		Last Modified: Thu, 09 Oct 2025 17:26:06 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fcb765a0e4701dfd40f1054e9df4b37f1a052f0382122728964e314c60f0b9`  
		Last Modified: Thu, 09 Oct 2025 17:26:07 GMT  
		Size: 4.1 MB (4140869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f1ee0bb888d32190e5165e1adc20745e3b54eacdf2ddcad4c0431617a9eb4`  
		Last Modified: Thu, 09 Oct 2025 17:26:10 GMT  
		Size: 66.7 MB (66677543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bc4d9d4ff11023e279c4ac7d61c9e934834ec300d85dd7643e2db9628e55b5`  
		Last Modified: Thu, 09 Oct 2025 17:26:07 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:162e2bb11dba19cb11a893804383d0639c1e0c21cb074baed639a9c123dcef4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51acb22dec4ad08828460be72458c4c596f88bf3c4a7f0ccbaae979f03f2ba2`

```dockerfile
```

-	Layers:
	-	`sha256:6000bb41c24329c74df349162688c62535ac9e37432c2b93dffb8fb1b0be35ef`  
		Last Modified: Thu, 09 Oct 2025 19:52:47 GMT  
		Size: 37.9 KB (37946 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:be16b5a67bab798af7c329f5a7d68fa541b40d4af272f35e902db6832c6956e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194353830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f8c31015d9a4b516a416f898739d4ca196fb6abb818412099fffdd2145e923`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3525e083585f6b97f18c72664a1f170f90fefb86fb8e51e93e18154511ff0`  
		Last Modified: Wed, 08 Oct 2025 22:41:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6e7ad44fd00315636e82854d172985670ddd499fb74b2aede25b409e4362d3`  
		Last Modified: Thu, 09 Oct 2025 01:51:25 GMT  
		Size: 34.9 MB (34860808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7d0d5fd78ab43128f5ea4a0c92e7a791681ebbbbb95945ae4dce23761ff730`  
		Last Modified: Wed, 08 Oct 2025 22:41:02 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab6e82836c6ad61fcabf2c118d629627c33d4e9a0dc3753b3773e9cd1d665b`  
		Last Modified: Thu, 09 Oct 2025 18:18:12 GMT  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0559f35ddfb3a59bd29510c0721ae92d30815bb49235233fd4cdee0c0fa53b4b`  
		Last Modified: Thu, 09 Oct 2025 19:53:23 GMT  
		Size: 69.0 MB (68960397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf57eaab2dc4ea143f782cb698f292880044a21773f7b5d3b2cdd68f6308945`  
		Last Modified: Thu, 09 Oct 2025 18:18:13 GMT  
		Size: 934.7 KB (934658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d83af209dd5b8b2d42812521005760d04d90f860c4869d3a6eb9563371f1cbd`  
		Last Modified: Thu, 09 Oct 2025 18:18:12 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9680a7b556ee68625b51f913c8baa260d1f3e016ee37f9de9b5e62ab6e842c7b`  
		Last Modified: Thu, 09 Oct 2025 18:18:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f448827b6becc70caca405e1b71d44cf7529bb9f08b06856955d5ecec3cd55b7`  
		Last Modified: Thu, 09 Oct 2025 19:53:14 GMT  
		Size: 4.1 MB (4140852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885c54af85a6fee7af9cba5a4b95f52c9b653df33c81119d2b167bd40a859fda`  
		Last Modified: Thu, 09 Oct 2025 19:53:19 GMT  
		Size: 82.2 MB (82231648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045b6a4ee4a3778ac97caa8e0cc35be95431adce21ce8372661db3f5f0b90abb`  
		Last Modified: Thu, 09 Oct 2025 18:18:12 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:7f77b7944483369fadc501e757722cbada8e6b6caddc5bc8e8dd9e88e082c96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e455e008efa70ad26de0bda075f9e6fe2e6e603935b5627c994ab05e3052a03f`

```dockerfile
```

-	Layers:
	-	`sha256:704fa66f52ef2edc10125f00c63d17bcca7539fcd6363dd6c73c6291209489db`  
		Last Modified: Thu, 09 Oct 2025 19:52:50 GMT  
		Size: 38.1 KB (38123 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:4e11ecbdb46ddd942e755b95d7b5f70702210de85aae657724cc7c0ab719625f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189934216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5986d785b5587e8ca0746399b83b499996854e80fd0f1775bde531eb6c93ee6f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f91771b6b3d663b68678cfe531282984d785f284d6a3045d051096c99edc5e1`  
		Last Modified: Wed, 08 Oct 2025 22:05:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bc681485953b8e19a36cf5e7d740aed69e73b1e9a337092e63b30b98340dce`  
		Last Modified: Wed, 08 Oct 2025 22:05:08 GMT  
		Size: 39.2 MB (39162641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992aefdef755ed935562cdfc9276c43413748262bb1c230aa1a30a017d622122`  
		Last Modified: Wed, 08 Oct 2025 22:05:04 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3464e2a71f1dc48b91afd273b0874330022ee4768ab6795869176f413b340c58`  
		Last Modified: Thu, 09 Oct 2025 17:27:09 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358809166bada04cd18dbc75b73e995ba12472c806d00b28311d3e1767d5b726`  
		Last Modified: Thu, 09 Oct 2025 17:27:29 GMT  
		Size: 75.0 MB (75045375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4130c110e2937292bfcc403129e6f50a7b76dcc4441b07c52338a85d13a3ba5`  
		Last Modified: Thu, 09 Oct 2025 17:27:10 GMT  
		Size: 922.2 KB (922187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1187a1a44424bf84c43a6c19e95a9b6329c5552f8a1b863c33ab3483357a61`  
		Last Modified: Thu, 09 Oct 2025 17:27:10 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb958cac3a21087ec509ff7ed724ed77d406d376706266b32379bc95c555edef`  
		Last Modified: Thu, 09 Oct 2025 17:27:09 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b8dc8afe13eb7c7656a5052a51aec787169442db15bc4a2ede08f599cf6b88`  
		Last Modified: Thu, 09 Oct 2025 17:27:11 GMT  
		Size: 4.1 MB (4140854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df3680d049fb6548cc12e93724b32a05a21e0982f4152a3dafaf693c73a1d14`  
		Last Modified: Thu, 09 Oct 2025 17:27:14 GMT  
		Size: 66.5 MB (66521179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b8838a9863b366858702952a2038f7f5c991360de374269c2c5f618e1ab890`  
		Last Modified: Thu, 09 Oct 2025 17:27:10 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:f8e503409d9a62c2167dfa4a819f6672031bcb964a017b499fbf75174f7c01ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd270b58a3b9b0855ffff5e808fe674d37be976033eb4cc5a46a5f632fec661`

```dockerfile
```

-	Layers:
	-	`sha256:0588f74b9c709836c9adc97a55167c0d2baf92a710ea2255af3df8a634c34afe`  
		Last Modified: Thu, 09 Oct 2025 19:52:53 GMT  
		Size: 38.2 KB (38172 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; 386

```console
$ docker pull redmine@sha256:c5c04ef304db29bc136eca4a01984bb6f73504d41b4a959fa0ae0cf408365864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207806862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdce349256bea00af22faac7414849c269330678f8c2ddd73aa0eb6d1d38f19`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742d0083d00079d6b0287abd29fc9e26007ebb5e7b5cb8b459a4f0a8f8b0e9ba`  
		Last Modified: Wed, 08 Oct 2025 21:44:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df14df0ed513ad605ffed7fbcdb86590aff03a8cd30351c572e5914016b64a39`  
		Last Modified: Wed, 08 Oct 2025 21:44:25 GMT  
		Size: 34.9 MB (34859955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7f87cb0bb0844cfa1a151d376f8c8fe74d93de723a751a8474b4b73dd778aa`  
		Last Modified: Wed, 08 Oct 2025 21:44:19 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8b2c2738e2ce18c7fd8a4b6b26710e26fc3485c64a774d902056721a3fc74a`  
		Last Modified: Thu, 09 Oct 2025 18:18:30 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06412e2c33983d4174760f6446cc7062279f1c1030ef68acdb098def3ea83545`  
		Last Modified: Thu, 09 Oct 2025 19:53:17 GMT  
		Size: 76.1 MB (76142746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d00ba00899830c3bbdd820bd0b71a338dea585f9ccee3aff2d57c9b7e5f7c`  
		Last Modified: Thu, 09 Oct 2025 18:18:31 GMT  
		Size: 939.2 KB (939209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd54f8368b8456b50c19f1c477ebb45f87382b9ffd04545a7e6572db900666e`  
		Last Modified: Thu, 09 Oct 2025 18:17:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603407f067862c49404c1167150ef356aed40b79b462276febe2950dfd4b773d`  
		Last Modified: Thu, 09 Oct 2025 18:17:16 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d415bc0d3ae712c14e1e1e960174f3597d384f11d86fe63ca7ab5960901bc6`  
		Last Modified: Thu, 09 Oct 2025 19:53:14 GMT  
		Size: 4.1 MB (4140865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1235e829083a2f13406a79f61e6516716c423aabb92aa609d09f7d0e0c95cd3`  
		Last Modified: Thu, 09 Oct 2025 19:53:20 GMT  
		Size: 88.1 MB (88101243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b083f4f3c7d990de80fb702f33b6f41e699e98bed84a46b2106bf12708ce03aa`  
		Last Modified: Thu, 09 Oct 2025 17:44:02 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:8c8e6275e1462045c8978713c2af35cc9fa9de3d85a438d86c246650894b51a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e51d852335fde0d7534c2b68dcbb95ce110a8f3a938658053a10f8a387b6e1`

```dockerfile
```

-	Layers:
	-	`sha256:726610a844b6af0e0c6f8e9c0149cb35fdcde5eddaa7238f8451dd52586e9f5a`  
		Last Modified: Thu, 09 Oct 2025 19:52:56 GMT  
		Size: 37.9 KB (37884 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:8f37037c625e5db3a063a7b4562babb3167aa15a3cc4554a116f5086abec8492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226419388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dce70c9d1c7133d7bc520a1b62238fa20fa3994b3f18376bdbc82145992a65`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05d59a37c7aa56f022ee55db10fe16720630a18748a9add220c24d9a46e00a2`  
		Last Modified: Thu, 09 Oct 2025 04:47:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1e4db1595ce8dac816e2d4cd8bb5b6a2d2082d65e20dbea7e24b2dff172220`  
		Last Modified: Thu, 09 Oct 2025 04:53:21 GMT  
		Size: 36.5 MB (36518192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2341b37203ac59bf7734c80428b28ede848e435033b08ec26d8934e38009900`  
		Last Modified: Thu, 09 Oct 2025 04:53:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c63b22abb6582e610ce34534ba9b798ce609ac1389a43ae93a648074c77e33`  
		Last Modified: Thu, 09 Oct 2025 17:34:30 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61e7a31bdb183f1ba6ec5913a4e7aa22c71b660a49988705dab16fad1d9f906`  
		Last Modified: Thu, 09 Oct 2025 17:34:35 GMT  
		Size: 77.5 MB (77478465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35d8ee0f48a137740ddf63df73627bebe6b2f127604921c04fb31569580cfe`  
		Last Modified: Thu, 09 Oct 2025 17:34:31 GMT  
		Size: 927.7 KB (927714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b115a69dd801b56f4b0050573791a6f5ef574d020fe7e46b222766f405726`  
		Last Modified: Thu, 09 Oct 2025 17:34:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11845cee45c9279ff0ef1e4b7be73bd42ed0cbb1ad55c8e214ac95bcc882c24`  
		Last Modified: Thu, 09 Oct 2025 17:34:31 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c662620c1846feb31b06e4e445a3f9d5dbd3cb11ea54829c3f1a3486b452701`  
		Last Modified: Thu, 09 Oct 2025 17:34:31 GMT  
		Size: 4.1 MB (4140894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b919ce2c73fc5ae9f0a90e34097640b6362c7123616bb0745d18eda1ea6436cd`  
		Last Modified: Thu, 09 Oct 2025 17:34:37 GMT  
		Size: 103.6 MB (103617965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b7c73d770ca4de3d996be6fe53b1575f36cf60f72d00abb8b18ef210ada046`  
		Last Modified: Thu, 09 Oct 2025 17:34:31 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:0eda84f11ee097e160a865af09972f51c53b58bce09b00ca8e926916f79c2617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb4fd11dcddb4dd30db4950f8009dabef53a60d43eb8a4e15db29aeeabf87c2`

```dockerfile
```

-	Layers:
	-	`sha256:6fbff00360c94e01950c1c62259e190f0535c587c4e64a6f094d80ebc0d2656b`  
		Last Modified: Thu, 09 Oct 2025 19:52:59 GMT  
		Size: 38.0 KB (38026 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:4a69ae01d4f4145f09211575393aa0236337a1b41fe5737d84cfe92b52330f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224763742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3dd170c258438260c7ade8ff4af402b5bdfdbfb9fe2a10b2dea7ab6157c40a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
# Thu, 25 Sep 2025 22:23:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RAILS_ENV=production
# Thu, 25 Sep 2025 22:23:05 GMT
WORKDIR /usr/src/redmine
# Thu, 25 Sep 2025 22:23:05 GMT
ENV HOME=/home/redmine
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 25 Sep 2025 22:23:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 25 Sep 2025 22:23:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 25 Sep 2025 22:23:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Sep 2025 22:23:05 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 25 Sep 2025 22:23:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Mon, 13 Oct 2025 01:16:18 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725f7cc38ecd0e8526ceb60091ebec855d3e2a1ece3cd3345c76898da3d32ee8`  
		Last Modified: Wed, 17 Sep 2025 08:00:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8771cc7f331a1be2af7b7e9a43884d2b958a42f3156ae9e68555739bcd6441`  
		Last Modified: Wed, 17 Sep 2025 08:00:52 GMT  
		Size: 37.1 MB (37059129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4783aae8683a591447579ed4030a688cdd3708e928bd62a6d38e5f9ce2665b81`  
		Last Modified: Wed, 17 Sep 2025 08:00:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83620a19997b0415962283f79eee13a5eaef1887f5ab4107ba18f74dff44af0d`  
		Last Modified: Mon, 29 Sep 2025 23:25:15 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f6a24caa4020a7b78d70600104e6943b32888a5915a1abe39c0f2250832d1`  
		Last Modified: Mon, 29 Sep 2025 23:25:21 GMT  
		Size: 72.3 MB (72283708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbe0b8b5c991b0b5b899fabbdd01307ef85d16c9acb7d9b5dd071a53cd1c036`  
		Last Modified: Mon, 29 Sep 2025 23:25:15 GMT  
		Size: 915.0 KB (914989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac74da170ed5a7f05cf635ae93aa11562b88478753ceae8bb3091172b62873f`  
		Last Modified: Mon, 29 Sep 2025 23:25:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c690231d2c88c725fbc64180639a7d7f7fe0935d37f9fc9040420d1304d9497b`  
		Last Modified: Mon, 29 Sep 2025 23:25:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdf79389e51bc074eaf7428f3bfc2ea2d3683fa2bab2070dec9ea8ff4b19d7a`  
		Last Modified: Mon, 29 Sep 2025 23:25:16 GMT  
		Size: 4.1 MB (4140820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b222c62e47b4d92bd7e3d43dd441e3a600554c867ec3deb64ccf9bfcff9cb5`  
		Last Modified: Mon, 29 Sep 2025 23:25:21 GMT  
		Size: 106.8 MB (106848446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c951a70b1769ba7133d8b44c29158059ff9c3b48bce0c21d78c4cd05dd567f`  
		Last Modified: Mon, 29 Sep 2025 23:25:16 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:5a477fea204bdfe37e568e3a5ea10ff33afc6799e609e3fe7b360987b31ae2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea1a8389794011a333d0ac249cd65b7d05f899b07e4c201353f03543c40adb0`

```dockerfile
```

-	Layers:
	-	`sha256:712a9bb9441fc0ef1f4af1327968f3464b15844909f4291ae10071216caea57e`  
		Last Modified: Tue, 30 Sep 2025 01:49:55 GMT  
		Size: 38.0 KB (38026 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:a3990c1492a3025a5abd6f49c565ac8745308344595f73f6b63b71870235543f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221902110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7847bed40ed6b6d66576ae1b2b8635289523579dc7fa273d0f10099071421cd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
# Wed, 08 Oct 2025 23:35:26 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_ENV=production
# Wed, 08 Oct 2025 23:35:26 GMT
WORKDIR /usr/src/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
ENV HOME=/home/redmine
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 08 Oct 2025 23:35:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 08 Oct 2025 23:35:26 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 08 Oct 2025 23:35:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 23:35:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Oct 2025 23:35:26 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 08 Oct 2025 23:35:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff34f11148b98d1e3395053bb36df148948025f86aaa78669db85af430e6b29`  
		Last Modified: Thu, 09 Oct 2025 06:07:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691f23dfa23832594b7d0138b3aa7bdbfe393588d3be7ccf54b8bf0c9c591257`  
		Last Modified: Thu, 09 Oct 2025 06:10:38 GMT  
		Size: 36.3 MB (36316094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbd321e9da76d083ae562106c53638404dd70178e3d67d73c964beaa8dd0890`  
		Last Modified: Thu, 09 Oct 2025 06:10:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f77810106d09a365e8ab9a6e176ef0837e4b84914456850eb0ed12cc50e4515`  
		Last Modified: Thu, 09 Oct 2025 19:53:13 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a866f3a75f6e11522064cc6b673fbd9004a9c42581a777e9b1863b0d58ef7b`  
		Last Modified: Thu, 09 Oct 2025 19:53:28 GMT  
		Size: 74.4 MB (74401510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea601dad52a62a18d1911f4f544760566b00a0874a206e9f9faeb28633ece3c`  
		Last Modified: Thu, 09 Oct 2025 19:53:13 GMT  
		Size: 943.2 KB (943182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1686ce57ef04bd63c60084ff149e90b7068a736874dbe25122af4e62c83dd5e8`  
		Last Modified: Thu, 09 Oct 2025 19:53:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0ea1562dd8c905b8109f1cd81e5ce7985b08bbc2bc52f60c8ed897e2dacd43`  
		Last Modified: Thu, 09 Oct 2025 19:06:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ef85e75a3d435e7d6820389f582d24b83092e2ce09d186656dacdae6563719`  
		Last Modified: Thu, 09 Oct 2025 19:06:01 GMT  
		Size: 4.1 MB (4140857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e96c8d12080d50967f151044d6c6033164e6f788c2fd6f1e144e7aed7597c`  
		Last Modified: Thu, 09 Oct 2025 19:06:20 GMT  
		Size: 102.4 MB (102447306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f827a9d4cc2b80aca43c79c6f8320f738f7a6b1296d41f1b2c0f879720e98d32`  
		Last Modified: Thu, 09 Oct 2025 19:06:02 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:85b988cfbe35f7bf92af9a18cc84e7ff1214aa955bd8b8b3b2adee3e644cb075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cc32c9266a4692373eba71a6eee5f48ddbb0e9ef173b0118e6ccd08007ceae`

```dockerfile
```

-	Layers:
	-	`sha256:4ac95d50921bf7a410a883a41c0253cbeece31e64ed1037f17a7cb324f96d4f7`  
		Last Modified: Thu, 09 Oct 2025 19:53:05 GMT  
		Size: 37.9 KB (37948 bytes)  
		MIME: application/vnd.in-toto+json
