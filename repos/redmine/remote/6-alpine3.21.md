## `redmine:6-alpine3.21`

```console
$ docker pull redmine@sha256:6f2995430e17073299333c1432a6fc12f87881ec1e8e84742ecb891bb4af75cc
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

### `redmine:6-alpine3.21` - linux; amd64

```console
$ docker pull redmine@sha256:0b5a68531799cef3b596f68cce61cb015a62c84fc0a0c20f3a64d8722e317c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189673850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429568566cb25c38a14bfbcd379e96e57b1a501fb33b17fab6d0e6595e2559bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV LANG=C.UTF-8
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe242d09b130806773822323154a3392545deebda43e141b48a8e5733150b2d`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2141123c1e920a49fb9e65545608d61acd44f4293342dbaaecf2a2c285372fe`  
		Last Modified: Wed, 08 Oct 2025 18:16:30 GMT  
		Size: 41.6 MB (41573294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1998cbdeb24dcc0e216bc621338df024581bb86a0b2590b31bfe423c0da8de03`  
		Last Modified: Wed, 08 Oct 2025 18:16:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3a33126b1e516f30923605d47a77309c578913dffe835935872f4fe405b2e7`  
		Last Modified: Wed, 08 Oct 2025 19:13:05 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ead638e53dc08b19715f59754c4c3c3fc773024069a26ae7d2cd54d9482a780`  
		Last Modified: Wed, 08 Oct 2025 19:12:42 GMT  
		Size: 72.7 MB (72708921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73674997a77cb9b5f483875318e71206767c72e13511c03e36c0f3ca5ee8665`  
		Last Modified: Wed, 08 Oct 2025 19:13:05 GMT  
		Size: 967.0 KB (966983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f315ddd0c915e9ca4e1c0c166d72d2c7a936442165039d2b5423d71f41fa2ca2`  
		Last Modified: Wed, 08 Oct 2025 19:13:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a70efa3229c6009d69ab49b983267c57a72ffba7ea0a6c88983806317bcc53`  
		Last Modified: Wed, 08 Oct 2025 19:13:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79cd52b7e6c73db6870bcfcf5472cc35a8bb1325172187ebf4105a347a8831`  
		Last Modified: Wed, 08 Oct 2025 19:13:06 GMT  
		Size: 4.1 MB (4140819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e27d55d078c26613787fd35664e5335105a726b28b3b0e471e409c0f9eb656`  
		Last Modified: Wed, 08 Oct 2025 19:13:10 GMT  
		Size: 66.6 MB (66642411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732e797ae048a21aadec66f3e1d0b92b4c87fe9628c20f91dfd77fd270226c14`  
		Last Modified: Wed, 08 Oct 2025 19:13:06 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:f0b4abb9780382335da9356856ba5b6ae3910c4b1d4f919378310797ae261cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a5b5abe9d2ec558b1a79cd11db423d672bb2983c4162e7bc35091db57a5f5d`

```dockerfile
```

-	Layers:
	-	`sha256:739d003404feb10fa00e857b2022bbea78783f7709a014ab61dd9c52094b168b`  
		Last Modified: Wed, 08 Oct 2025 22:51:02 GMT  
		Size: 36.7 KB (36722 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.21` - linux; arm variant v7

```console
$ docker pull redmine@sha256:1db53d098afb90467de545055b02e2edee74736ae4de527145d752653b05f882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193123176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8461fae0d1f3b7faab059cc2ae41e1575fbed3d71bc5a6edc3129396c7bf1650`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV LANG=C.UTF-8
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
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
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75eb70768e4be1484eeeed4971711d79fd3edba8b7eb2e0cb5e211885d4422b6`  
		Last Modified: Wed, 08 Oct 2025 18:15:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fd584d6c5203908ea003b4f6201da1c64102b0e77e7bd721811f49ce28467f`  
		Last Modified: Wed, 08 Oct 2025 18:15:09 GMT  
		Size: 36.6 MB (36633040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf13ce76c735d73113a242a4a6ab9f0fdfaed58ff6828f2108502e2def3e8e9`  
		Last Modified: Wed, 08 Oct 2025 18:15:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742970c802e428adc2cf9f8b7f7acbdeb6dc30e0d1458c41fb6481f0f3b6666b`  
		Last Modified: Wed, 08 Oct 2025 19:17:07 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2b73432610789adc6779ebff54237844c51517377dbb7999e83d1a351981f5`  
		Last Modified: Wed, 08 Oct 2025 19:17:13 GMT  
		Size: 66.4 MB (66436243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cd00ef5562655819e8df225f9011a2c45e19d3fd1bbc30edc7f4316b3a7bc2`  
		Last Modified: Wed, 08 Oct 2025 19:17:06 GMT  
		Size: 934.8 KB (934841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e93ff9ff3ce22e7b32a2c6bf73d29034e0c59566bd844ae02319f59702fd26d`  
		Last Modified: Wed, 08 Oct 2025 19:17:06 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c8b5e707e34d08f079a300a661bf0ce732b50bb7b53c38578b35744ad50f76`  
		Last Modified: Wed, 08 Oct 2025 19:17:06 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f74bbb46caf1b086ebfb0232b7c5cc8778ffcd6d50ac82d6d891c605c21f4a`  
		Last Modified: Wed, 08 Oct 2025 19:17:07 GMT  
		Size: 4.1 MB (4140850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0f53c347e9c3d6273959528edee43b23967a031c7d81638b63820cb73dbaa2`  
		Last Modified: Wed, 08 Oct 2025 19:17:29 GMT  
		Size: 81.9 MB (81877478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aedf45c72a88c23fdade5750b768e4abf7682b9b947db0c9903d72194bfcfe`  
		Last Modified: Wed, 08 Oct 2025 19:17:06 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:85e8f472fc0ade5760d42d85dddf97751075c5e4c969b4c5db8ffb4b764d98bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614f5ccfcee127da050a979212b09ec2b8c404edeb50eee7c39c5b85fd20054b`

```dockerfile
```

-	Layers:
	-	`sha256:498f349b89309c2a0414870645e0d2572cf70c1fee7cceca808cdfed4fb42248`  
		Last Modified: Wed, 08 Oct 2025 22:51:05 GMT  
		Size: 36.9 KB (36867 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:e9f4a1acabf5e42c72dea35d05a0e4e6df5338dfb662059f1de5606057bfd4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189665710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cb53f9d1deb04bb6e409411f78b80f1ec9c48318bbedc8a25c256a1b5b8c0d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV LANG=C.UTF-8
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
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
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba332a47491c0fd69a2abfee4d69835999fc957686af2bc7cc83d7fa78d3aa2`  
		Last Modified: Wed, 08 Oct 2025 18:16:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0ee6d202b66e3179d82a03d329b3cb59cc1188cfc2a693ed4a5129fb242d4b`  
		Last Modified: Wed, 08 Oct 2025 18:16:16 GMT  
		Size: 41.7 MB (41740984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c214d0493d914ca56a761a5a982d62c4193bc83ec207ef45a6588db218054f2`  
		Last Modified: Wed, 08 Oct 2025 18:16:10 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dae2df37edd016796277a44441d935e738b6ff106a6a3d93d5ff364ffa4a7e0`  
		Last Modified: Wed, 08 Oct 2025 19:25:56 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f71e0a5fc4e86090e0f3f37f27bc1972adcc69656a2e4baedfa4692dad8d24`  
		Last Modified: Wed, 08 Oct 2025 22:51:33 GMT  
		Size: 72.4 MB (72382851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ac91deed587e82216f002ae41dfd8dee2f5c5b3e5f79f6c23db54360250b58`  
		Last Modified: Wed, 08 Oct 2025 19:26:01 GMT  
		Size: 922.3 KB (922261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4703a7acbcfc68f9c748db46ec366fab148656c90ffb086863c379c0141d0b8e`  
		Last Modified: Wed, 08 Oct 2025 19:26:09 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7090d6690c14bbfa36616dbb75189f7756ce1b221080ec325d3c91c2cd5906f3`  
		Last Modified: Wed, 08 Oct 2025 19:26:12 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd820675624e32e93103ea17db57cc0cf978e4b1b1dd599f03198d7117de638a`  
		Last Modified: Wed, 08 Oct 2025 22:51:30 GMT  
		Size: 4.1 MB (4140848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd82be7e6c3b5a7435d671d7439104dfe6125b7f837eae90f4f7e382c4232b2`  
		Last Modified: Wed, 08 Oct 2025 22:51:35 GMT  
		Size: 66.5 MB (66487981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4621536b2e154cbf1a57179bbedf3a3224610025b5bffbcde6b7ceb9d351a692`  
		Last Modified: Wed, 08 Oct 2025 19:26:19 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:3aeead8f56840416e4b103aaa0ed4ba326c25f73dcb5c3bc6bc62006e89e485f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da499e31cab0171203bb69003b1b83b5ebf4e0e1aadbcfd1a6057aca15c3f03e`

```dockerfile
```

-	Layers:
	-	`sha256:0ae051953e66fb1d0811175816b48762d70fd161d1d897a5eb53a725f2c42b00`  
		Last Modified: Wed, 08 Oct 2025 22:51:08 GMT  
		Size: 36.9 KB (36900 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.21` - linux; 386

```console
$ docker pull redmine@sha256:dc88a5df7a57bad4f69d4a39debc3bef608964f3c2ce32aebe42c0ab2ac539ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206901083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5dd814fb416fa681684cf806fb903902e518f809354397a33da207f9a6f8c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV LANG=C.UTF-8
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
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
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad95dd346ba58c7046850c6f88c4d3f17530e1b48b6277493540ae4b9a63c3a4`  
		Last Modified: Wed, 08 Oct 2025 18:15:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f03ff7584f59a87f8774e31a410ae11903de396370693f72faf3d3f01d1995`  
		Last Modified: Wed, 08 Oct 2025 18:15:09 GMT  
		Size: 36.9 MB (36933938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0db024807b84cdffa1bf3259445ef72f0c8c9621ff78fcb95c863d797e9f1fb`  
		Last Modified: Wed, 08 Oct 2025 18:15:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9b75c764a1c7a08250a2518f2e856150885a181aab3113d9e52c9e9c42e79a`  
		Last Modified: Wed, 08 Oct 2025 19:21:04 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1229f00371d3cc5ea2748d7a342004e10ff77dfc488bbae242fae67e4b1c836`  
		Last Modified: Wed, 08 Oct 2025 22:51:39 GMT  
		Size: 73.4 MB (73381367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793f850b7ef0fee98829991891528ab171c2636fea28a343571ac0706c46fcac`  
		Last Modified: Wed, 08 Oct 2025 19:21:08 GMT  
		Size: 939.4 KB (939354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694407ee12ba8f5bbda01d8900e4f5ab4bf4a3facc061f0823e79d448fa41e7b`  
		Last Modified: Wed, 08 Oct 2025 19:21:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee29191ea2ff4ced076b9c532743e2f7c1af8710ff0c507e5f6393f75030571`  
		Last Modified: Wed, 08 Oct 2025 19:21:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa74a2070084aaa942bdc23d6e6b2a7d93f9834ea38b47933e0e4c9bb01b2ba`  
		Last Modified: Wed, 08 Oct 2025 22:51:33 GMT  
		Size: 4.1 MB (4140905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698fe56f9a67e51774019ac19e402a66cf94949e8eeeb8212e08175b66d7ab67`  
		Last Modified: Wed, 08 Oct 2025 22:51:44 GMT  
		Size: 88.0 MB (88040941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1c4e10aa202f1f4ac6549a588589992d0cfd07993ad0870702b4cc9780b338`  
		Last Modified: Wed, 08 Oct 2025 19:21:26 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:9719e0ddc579fdd1d76f07fbe1ef6d99150b15d470240d9b1b19face61d9f5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba3905772b583670e4d035f6ad3560c9174c5e65f12811680ed0022dd645b48`

```dockerfile
```

-	Layers:
	-	`sha256:53b2358acbf3a6c866cbd427d28ff3a741f8df4b047a11303214461c191c2ce5`  
		Last Modified: Wed, 08 Oct 2025 22:51:11 GMT  
		Size: 36.7 KB (36680 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.21` - linux; ppc64le

```console
$ docker pull redmine@sha256:fd89d2de84eabdf31f3d48d383715f5f488d5f525b8ef1b4403c02ad546bf396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224546232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d0ada164f1dc2593ec3c53af9c3dc6da611ac956d517f20705ce3de6f96622`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV LANG=C.UTF-8
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
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
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b484e5ebf56bd3da254810f1b17477f7f356ce2c0b43571d549dbb2d0246387`  
		Last Modified: Wed, 08 Oct 2025 18:50:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80105bcaf5cd469ffe5fb85685ff3af21efddcc674cf0ae547d66c90bbb0e239`  
		Last Modified: Wed, 08 Oct 2025 18:50:34 GMT  
		Size: 38.6 MB (38639623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7698ef970acb60c166d06658d1c2ea503d7150e07762c623a20a2935c8f2a56`  
		Last Modified: Wed, 08 Oct 2025 18:50:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b6b137613301e97fa40ff2d0f54708b48799f8af73a5612a2f717515ad63d6`  
		Last Modified: Wed, 08 Oct 2025 19:31:11 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34377b1150b09e3ef01a808f03d807bd42bfd02b266cbf9ab8190d07c07737b`  
		Last Modified: Wed, 08 Oct 2025 19:30:43 GMT  
		Size: 74.5 MB (74451105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29381f13a22bdc49774b9430dc9a15c82fa15d6f69709c882aceab55aa7be753`  
		Last Modified: Wed, 08 Oct 2025 19:31:08 GMT  
		Size: 927.8 KB (927819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21abed96bd1ad7881a7b4203dcb3e1be866153a8dba9dbcd414ea09b4705084`  
		Last Modified: Wed, 08 Oct 2025 19:31:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3913205571734c8363e854ed693224ac9ec27f937c31434b24fd95e830c6c4df`  
		Last Modified: Wed, 08 Oct 2025 19:31:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b0c590beba1ac0b70b80baf88c628e6b46c41c3df9959edfd1649caaa69ef0`  
		Last Modified: Wed, 08 Oct 2025 19:31:09 GMT  
		Size: 4.1 MB (4140892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c735f4a634b0b0db24008f266415ada341e0a9850f69cb34202a0ca5f19b29b0`  
		Last Modified: Wed, 08 Oct 2025 19:31:21 GMT  
		Size: 102.8 MB (102813815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a915009266faa548c2d51f7a1673f0a81b283e0ee7a1f7ecef4cd1913c35b70a`  
		Last Modified: Wed, 08 Oct 2025 19:31:08 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:584f9cdefe44fe87d65cdd3ae58fd1a05fa67eb9125332708f63b03b8fface32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb79bd3d865bfcc6d9b80ec0f5817868f06527b3ede3b48096cbde792ccb4f1`

```dockerfile
```

-	Layers:
	-	`sha256:b48c7510fced538338ed5d0b96c2c5dcfc8572e02eabcd7007c90887ba1f251a`  
		Last Modified: Wed, 08 Oct 2025 22:51:14 GMT  
		Size: 36.8 KB (36777 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.21` - linux; riscv64

```console
$ docker pull redmine@sha256:4892ead4dda2cf17f11c5424a2f049ff74e67992965b40e0134a4c153723649e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218971760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b5e289befc394d75166b7ca8da77203f1a3b188543426a7ffaa22a6c26e7ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da813de376f5d6d96d6c3a3e5402faa60697eced9496ab2deaef64c5a3d46cee`  
		Last Modified: Wed, 17 Sep 2025 10:07:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f619869feb22afab53ea8468beb3a081d5b688c56184af176d1799b9690b57`  
		Last Modified: Wed, 17 Sep 2025 10:07:59 GMT  
		Size: 34.9 MB (34900926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971a5207a3077c3901cd2926098f7830942529dcb9e4ee334ff38b8c584c4c7d`  
		Last Modified: Wed, 17 Sep 2025 10:07:43 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d330b01158c42a3c5113c3ff960b5a5140fe9f26212d0678da77c15507743d`  
		Last Modified: Tue, 30 Sep 2025 00:46:11 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adca41794b76f5898fad8b5602f19bb5798a316bab00434415163bc4dbff21d`  
		Last Modified: Tue, 30 Sep 2025 00:46:15 GMT  
		Size: 71.5 MB (71468387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c6388789b1f6c3bcb3f29e7e16fdd5054ec5995d5aa12135dc4347a8c1517`  
		Last Modified: Tue, 30 Sep 2025 00:46:12 GMT  
		Size: 915.2 KB (915178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6222214915d759f0362080a1c1c57e6935f248e9ff6c61abb5cc463d5dc59f0`  
		Last Modified: Tue, 30 Sep 2025 00:46:11 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855792868311990c748cba677b8c644cb0af30802ad91e202d45d5af23e244cd`  
		Last Modified: Tue, 30 Sep 2025 00:46:11 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6964e17299716edeae64c1b7b95064d8465337b29c8ad4e6d5e92e31a57e6d`  
		Last Modified: Tue, 30 Sep 2025 00:46:12 GMT  
		Size: 4.1 MB (4140853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2455e89fd99ae970fc51efd501b346e74bd40a46b62cab96d900baac2be480a5`  
		Last Modified: Tue, 30 Sep 2025 20:34:50 GMT  
		Size: 104.2 MB (104193478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288d5d1e6a0c92d9cab3e13c07b112c8e7373d7e4b45aff1f79319c9f458335b`  
		Last Modified: Tue, 30 Sep 2025 00:46:11 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:8f7bbc841dee84cbce8d1cacfbffa93665b95119c0a397ebe4a1ea1d9c3245da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01985456e24dea87ca7d96ccd011f1a008334175a5f91c167cd4c878bdba4a7`

```dockerfile
```

-	Layers:
	-	`sha256:858bc82006940d84ba65b2e786e3aef218cb58069a644be4e99aaaef33f55f08`  
		Last Modified: Tue, 30 Sep 2025 04:49:54 GMT  
		Size: 36.8 KB (36778 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.21` - linux; s390x

```console
$ docker pull redmine@sha256:906e335388954aaed851063af068acd99386e33cc68ec805c02534235e3b975f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222556654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345b39febda7997b7bc5d006cf54e302511d770bb8e83a254a70e5433c5f342c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV LANG=C.UTF-8
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 25 Sep 2025 22:23:05 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 25 Sep 2025 22:23:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 22:23:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 25 Sep 2025 22:23:05 GMT
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
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d970581b474557cf5b6140c7450cc25b6224fab51c3e7e923e6c3ffb0c63ff1a`  
		Last Modified: Wed, 08 Oct 2025 18:32:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b05380f58c00b3833ff411d082e1e100c29ff270e55b89ce27c547be48bc51`  
		Last Modified: Wed, 08 Oct 2025 18:32:30 GMT  
		Size: 38.3 MB (38328046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7d5b128ba0c969f09da440dc04bf93b4ad5e05aefddfa81b177512d954d376`  
		Last Modified: Wed, 08 Oct 2025 18:32:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75261fbd54398340e84b343271bd452b44e0ae6f52250000efdb5201dbb66a80`  
		Last Modified: Wed, 08 Oct 2025 19:33:16 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ab8cb26748ea11d24e6b3772664b1caaebfdc4a48a5b06f129f6da5eb6458`  
		Last Modified: Wed, 08 Oct 2025 19:33:21 GMT  
		Size: 73.5 MB (73456688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05885b6db5ba964a77ab1d3b05b21daf6926647f5f09d5bc2407fac2b17e4ec1`  
		Last Modified: Wed, 08 Oct 2025 19:33:16 GMT  
		Size: 943.2 KB (943159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e44dd896f5acb89438a9cc03ba4dc3460224ac8b94af86ee5a1f159b8c995f`  
		Last Modified: Wed, 08 Oct 2025 19:33:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c7e61b28f929db26dc76e05111c7496a0b152dcf3893dba5724ebb58ff889e`  
		Last Modified: Wed, 08 Oct 2025 19:33:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd4ffad68480e18e82b9461da080c46e160f140dabbad1a47845439b4e0976e`  
		Last Modified: Wed, 08 Oct 2025 19:33:17 GMT  
		Size: 4.1 MB (4140835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efc6118e459d248a549c85a75ada7867158a5c8f322b9727594b5a29715ebf2`  
		Last Modified: Wed, 08 Oct 2025 19:33:26 GMT  
		Size: 102.2 MB (102221977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852717c6a1dd54453eddf7aa5326ecc3737b831e708b5bc81cdf155145447bef`  
		Last Modified: Wed, 08 Oct 2025 19:33:17 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:be5231cfc9f86fbf894f5c2b9d39cd13167a8e9f2f5f3c04389b1ff090e2a2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf94b7d64fb9778e18d9a7ca6f770a43010d87a06a8854e6ecdaefec68d298d`

```dockerfile
```

-	Layers:
	-	`sha256:f89b056bd77de8277890cf1426f4cdcc359b9b103ccd4f116cc5be3ee9c8fda7`  
		Last Modified: Wed, 08 Oct 2025 22:51:19 GMT  
		Size: 36.7 KB (36724 bytes)  
		MIME: application/vnd.in-toto+json
