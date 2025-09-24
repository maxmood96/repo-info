## `redmine:alpine3.21`

```console
$ docker pull redmine@sha256:cd66df05f63ff2f4ab1c3bdf7e9c22aa145f8dc191a687b369180add49fba8fe
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
$ docker pull redmine@sha256:2f33dfddc64ac7f48d982a96f3831b6b1c92fb05a052397b39e7f30f8327ff77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 MB (190773787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a29d0a6644ffe9b62b94f85a5eb3d5a7ef7a7dac95c35464ebc28690954fd0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072e3e4ea5c913a8dae03862632bcceaa9122bb0351a8b1562e276de1cc1ed0`  
		Last Modified: Thu, 24 Jul 2025 18:45:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203353491163f797e096e74e92c164a8132e0412753837bbfe30abd3c336c296`  
		Last Modified: Thu, 24 Jul 2025 18:46:10 GMT  
		Size: 35.6 MB (35615628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6debf1a7124e3a62068eca8fe54dd40cce6ab977d7091f99a086fbcee3403de0`  
		Last Modified: Thu, 24 Jul 2025 18:46:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42236121bf60c6a300807a5f09822b74f64f609520d72e355fdc5fa7a5369e3`  
		Last Modified: Tue, 23 Sep 2025 23:21:54 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5233300fb93bfddb10b4a24c56c0500cf2329552325ae34077bea75927c69ab5`  
		Last Modified: Tue, 23 Sep 2025 23:22:00 GMT  
		Size: 72.7 MB (72688180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2cc5c93c77272841f10517b411d88b1f78fa3d75343a2241c54118949b2341`  
		Last Modified: Tue, 23 Sep 2025 23:21:54 GMT  
		Size: 966.8 KB (966788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d76620738da29a51ffd925cf70b311b4cd6ccae17a96f32543e7e3a843c6e75`  
		Last Modified: Tue, 23 Sep 2025 23:21:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5399e0262d279f630156aa5e8e75d71af5ed9b4b98950775145250eb31a7ffea`  
		Last Modified: Tue, 23 Sep 2025 23:21:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee73e9927c3bcc0c0ced5615047d185633052352d730380b5346aa08e371cc03`  
		Last Modified: Tue, 23 Sep 2025 23:21:57 GMT  
		Size: 4.1 MB (4069871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5004a23a6de64a4d9c36ca469b314957199425e7feda0dc4fc8da5e1aa071ab`  
		Last Modified: Tue, 23 Sep 2025 23:22:00 GMT  
		Size: 73.8 MB (73791897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd3dfb06a975eab3a0124952d1ae08ef372d5685fbf3d4e45929afe9f2e3cf2`  
		Last Modified: Tue, 23 Sep 2025 23:21:56 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:852a433862d5776dbe75d03b732d06a7165b5711a851d6e85de9a2a09f9b9270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5bc7dff9bacfdb1241f8f181cb8587fbc4e1bce56b443653b802d73ecaaec1`

```dockerfile
```

-	Layers:
	-	`sha256:89cbd068e6c856a53dca3519734252f159a31959996f3b868aced2dd3b07e5ca`  
		Last Modified: Wed, 24 Sep 2025 01:51:35 GMT  
		Size: 36.8 KB (36786 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm variant v6

```console
$ docker pull redmine@sha256:63845d749d4ff79fb3c1772ccae63c8c5cee42ad14143009232346f3c78569e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182677808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470844ebf4f1e36be223dd3b58dcd8371cca5aeb117f9733f2e4c2b924630d5a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd2aade873422152cd38c54790f33c3043c235216377097742a4ec943cea10`  
		Last Modified: Wed, 16 Jul 2025 03:14:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4d3b39d485fe37d5d05f0240313ddfdcc1f39833a914ef28acde83dd2d9085`  
		Last Modified: Thu, 24 Jul 2025 19:52:09 GMT  
		Size: 32.1 MB (32071821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bda74ee7a6784522652a758995e54717ecca24ed5692b58b4c4c1b65b35df8`  
		Last Modified: Thu, 24 Jul 2025 18:45:55 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6558423d44e3b4ec8c972dcffac6405d046ca92265d422eade593e0d28812ea`  
		Last Modified: Tue, 23 Sep 2025 22:08:15 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f0b46795b597855b9fcd7ec65761d3233ab417ab12abfdf23ac2a8401d206d`  
		Last Modified: Tue, 23 Sep 2025 22:08:30 GMT  
		Size: 69.3 MB (69259991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a755ffa84b083f3f8d72e3972c849852211266dda597d9a1e048994fe533e90f`  
		Last Modified: Tue, 23 Sep 2025 22:08:15 GMT  
		Size: 934.7 KB (934717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4c82a823bdc65dd9bcf1a76bab8b4d55f9fe0f30e27d88bd615bf28f3c35d6`  
		Last Modified: Tue, 23 Sep 2025 22:08:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce007ec2b56388f78a466c26575896ad0f5dff927a15dad7132882ab3150212`  
		Last Modified: Tue, 23 Sep 2025 22:08:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8210bb8b7c1afc032017ce10e3283ec543bc5f07b0dc30be00181805520d75bb`  
		Last Modified: Tue, 23 Sep 2025 22:08:16 GMT  
		Size: 4.1 MB (4069902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de3ca78faa51f4cb5b54d33ea877c72da15c4490a43a27288defb557d768e2f`  
		Last Modified: Tue, 23 Sep 2025 22:08:24 GMT  
		Size: 73.0 MB (72973713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be784e64d0c2ec36bc06030e3bd0d08d024f914f5f73177370563257ad96eee`  
		Last Modified: Tue, 23 Sep 2025 22:08:15 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:319932f8d923cd7e91fa602c8967edb950482ab4b4e553c079531ce6c946a4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed16e8ec1b89a508c8b64ae9df2dc088ad3e049371b76ec211afa85c76e1d1bd`

```dockerfile
```

-	Layers:
	-	`sha256:8639402775a2a9f1d9bda5b48cd22859e9f2048f29831292b20dd4bde6b7d27c`  
		Last Modified: Tue, 23 Sep 2025 22:51:06 GMT  
		Size: 36.9 KB (36931 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm variant v7

```console
$ docker pull redmine@sha256:ed0fe81fe27312fd2354be86471c1a56cfb5767fc766df0c46ee95f9fce4e03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178460791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e849423651288fd740288c62dcb69a10c36245ec4f5a0598feee82cd6ee67c3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770f1267e885ebdd245469ced631a975128a2c04584309a18a73b137ebc67293`  
		Last Modified: Wed, 16 Jul 2025 03:21:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a012e992f71f58404b2fdf681c56e004d9232fb46f6c13da8fffc3b6197f3031`  
		Last Modified: Thu, 24 Jul 2025 18:44:28 GMT  
		Size: 31.9 MB (31940083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ca87e750f691d8434671a63c5d33fc91364fc16d93f947291a4b06152de84b`  
		Last Modified: Thu, 24 Jul 2025 18:44:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a430f2847aa9cbf2e573c29a3c080ac299bb936eebbd048e3ac70f75342cf52`  
		Last Modified: Tue, 23 Sep 2025 22:18:59 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aa7cda568746acaf7edf27d7a945bb8e91aead93ec3c599b14d92e6b981c37`  
		Last Modified: Tue, 23 Sep 2025 22:19:05 GMT  
		Size: 66.4 MB (66399686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca860bc0ed6990f580290580bb8340ec041f1b2f8f6a8f772042b4d7c8f398a0`  
		Last Modified: Tue, 23 Sep 2025 22:18:59 GMT  
		Size: 934.7 KB (934707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdefc3b3a32271facf0f90a1a7b3aa14d809c1de77b5f388790d3220d616af6`  
		Last Modified: Tue, 23 Sep 2025 22:18:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc73ffc37c5d98418e7bd9a76a383d71b1398abf5496a6732329243c45972b7`  
		Last Modified: Tue, 23 Sep 2025 22:19:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9b24b423e7a6d9f136c8544d9d8e50a65c4db33228f108aa25d9ee8fa5a08e`  
		Last Modified: Tue, 23 Sep 2025 22:19:00 GMT  
		Size: 4.1 MB (4069997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441bc6815c64ff50f399182dc10d219648e99b74627dff51fca1fa23c231ed6b`  
		Last Modified: Tue, 23 Sep 2025 22:19:07 GMT  
		Size: 72.0 MB (72015596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973974012050cab3f793142b067900a677bbfc7cd9a89e0607446ba77f347901`  
		Last Modified: Tue, 23 Sep 2025 22:19:01 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:e5fc4191370b87769badfb83d5984f332802c96f580a8dc099472b5969ca4d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866dd3333aa9934e3bdcf0713e35199bd78d1f5bd6dcb43d3297e6aa296d8c49`

```dockerfile
```

-	Layers:
	-	`sha256:d88e8eb536887486c938c6b2bdc68ed9cbbdde525cae356c0069547553e356ac`  
		Last Modified: Wed, 24 Sep 2025 01:51:39 GMT  
		Size: 36.9 KB (36931 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:d4244d535b152eff45203f5e846a4415a2377bfee9afb9b727ed0e5d3c8918ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190671687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56922a0b8c636fa5c50ec9e5f67a921cba41164fd5404d2c8bfb4bccde3e6d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88a67af6e61884f81e8aedb5d643f2b423edf30698d9d9bc7288cda191cbf86`  
		Last Modified: Thu, 24 Jul 2025 18:37:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d27753b78f787827728c2071fe55f26c6bcc73df36f87f22aa332e586477f5`  
		Last Modified: Thu, 24 Jul 2025 18:37:34 GMT  
		Size: 35.5 MB (35538489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9681ddb3a23aa1504e2a6638408b60fdf418de7eb55437715a86b576d27e87d1`  
		Last Modified: Thu, 24 Jul 2025 18:37:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d79db507ff5421950d35746776888ff56807de609334ae02d901b81b5b1fca6`  
		Last Modified: Tue, 23 Sep 2025 22:14:30 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683e5343d253d75142a9579833e844f9617df3fce6fd3a04d6d12de9104c7ab3`  
		Last Modified: Tue, 23 Sep 2025 22:14:35 GMT  
		Size: 72.4 MB (72360845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02cefd47ed301dc6a01b3c5442f5910289d1a949805da1f86428a0f35d30a7a`  
		Last Modified: Tue, 23 Sep 2025 21:32:52 GMT  
		Size: 922.2 KB (922182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0661b708ea3d50a71ec401f8f93eeeea0045b3e5f3118b2fb65b73f75a239e91`  
		Last Modified: Tue, 23 Sep 2025 21:32:52 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9696cfd217ab4038cf805fe87fd1e5b0c7f18853857cfc78ef2da9981056ead2`  
		Last Modified: Tue, 23 Sep 2025 21:32:52 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889c459de421e3740f4f1ed11f08d39d780f0a5a5b623cbbbae72c0e0bb6967f`  
		Last Modified: Tue, 23 Sep 2025 21:32:52 GMT  
		Size: 4.1 MB (4069895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62669fabce25a6ccca60caad9544f19e15dc7f26597f30641fe0118b3ec48a02`  
		Last Modified: Tue, 23 Sep 2025 21:32:19 GMT  
		Size: 73.8 MB (73789489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc87cf0671a81f4190e71a2d6bf599822538798035aa61cdab6ede745d02c408`  
		Last Modified: Tue, 23 Sep 2025 21:32:52 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:cb9284d493cea5da02ed84b688e3e830df11e31361d1a45a2eb6b303957b3c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce2c8e4e77707e56a412db89d9cba8f1210f4c63644f5404aa11f0c981f8b09`

```dockerfile
```

-	Layers:
	-	`sha256:071a7d34643de02efd0fd6ba0fd8f9860ef6a672b8e6ec2c8a02483ce4e74071`  
		Last Modified: Tue, 23 Sep 2025 22:51:11 GMT  
		Size: 37.0 KB (36965 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; 386

```console
$ docker pull redmine@sha256:b2fab0cad98834e06377e48942d73d43bd0d1edc6b7cc844055559a34af10ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187652571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38778343ae1a7af45a180bfe5da8905dfbce2a13e8bddcabc3eafe12d15b7c75`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3748b85f9c1210995838145e6f8169922d062f6375fb07ce372c3a05ab89fde4`  
		Last Modified: Thu, 24 Jul 2025 18:30:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e01c4485ee7ec68e4f000ce7a4758a03345860b3e84cb29c0db67ce607ddc5`  
		Last Modified: Thu, 24 Jul 2025 18:30:07 GMT  
		Size: 32.0 MB (31957554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afba70ebeaafeafd7f195c817c2fbee88a9e478ce37161dff65bad07561d93a2`  
		Last Modified: Thu, 24 Jul 2025 18:30:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e6965c72b808b36f49959f139545c60dd5b7cf9d33924d7294e4eb59b58238`  
		Last Modified: Tue, 23 Sep 2025 21:47:50 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8dd763659914453db91484239e59f502a8e9b4132ee916256712b3b1a47c2b`  
		Last Modified: Tue, 23 Sep 2025 21:48:06 GMT  
		Size: 73.4 MB (73366494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a73108591f1d7d521921b8b36e5a4d8b303cb87eacdaa58e858f9d69c0b02c4`  
		Last Modified: Tue, 23 Sep 2025 21:47:50 GMT  
		Size: 939.2 KB (939238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2531878ab4d34dd4197f73214d142e47c0ca72ac212385160fc480e30b513dc`  
		Last Modified: Tue, 23 Sep 2025 21:47:50 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81a6d9a6805d95b226c55266650d27eb80893fc09868e3e32e757a5c437f05c`  
		Last Modified: Tue, 23 Sep 2025 21:47:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5201d267855687399c072c5274cc28881bd85da85cd7348c15cdbe3e4035e8cb`  
		Last Modified: Tue, 23 Sep 2025 21:47:51 GMT  
		Size: 4.1 MB (4069898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5804f4ed74e2f71789b724b367c50cdd17dab82bf69e12aae382e4bb7e809582`  
		Last Modified: Tue, 23 Sep 2025 21:47:27 GMT  
		Size: 73.9 MB (73854809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c3407a0d1c4bbcdb7ba40756ea188e421b09c3a24984dcf6a53e51a2082e3c`  
		Last Modified: Tue, 23 Sep 2025 21:47:50 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:e55a9850a19a1f616f3d7bf4e92cacd0b834510e0979484e40de7c33ee1d6d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0502777b384d664227ce2a6b718b7e83dfc9956385ffd81e6fa79baf9bb0f1`

```dockerfile
```

-	Layers:
	-	`sha256:7e01d8430f6ee2f9efbe47af0efffc37a3819b41311a4418b2b0ee8cffb84744`  
		Last Modified: Tue, 23 Sep 2025 22:51:14 GMT  
		Size: 36.7 KB (36744 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; ppc64le

```console
$ docker pull redmine@sha256:36cc21f155c99b3c4be6fa0750b8c6610c9dcf1f99cffc59482a5d2c1b6b89d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192002726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1662aae0a303859abfee27d10fb09893bb1bec61eabf29504b7552760439bb4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f46416c566ecc9d89cb5bee95fc09aa21f865554af8f4134eb062779a2f237`  
		Last Modified: Wed, 16 Jul 2025 00:59:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f34485f0a02542f6d3f0071e2b20b14784febfa7e6900cda5a89c870d097b3e`  
		Last Modified: Thu, 24 Jul 2025 18:37:09 GMT  
		Size: 33.5 MB (33453818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cc80e746f49edd232e415595c252265c3fce90bcc1aaeeccbd81827f3b4a2d`  
		Last Modified: Thu, 24 Jul 2025 18:37:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c8703057795c3db9258439bca3114d329df94f8240b1faadc93ac15cd7f70e`  
		Last Modified: Tue, 23 Sep 2025 23:22:57 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a0beef9df8f8c2f85f2febb9f4ca27218b0ac535969954580b8e1729024852`  
		Last Modified: Tue, 23 Sep 2025 23:23:02 GMT  
		Size: 74.4 MB (74412268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7059372069716d681cb229e8fa0a3c3e749331bf6a60285c0535409ad8a1e128`  
		Last Modified: Tue, 23 Sep 2025 23:22:53 GMT  
		Size: 927.7 KB (927715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952d5e029d60b187ac7f7df99891d6def0f55571d2886bd37402595a1563b258`  
		Last Modified: Tue, 23 Sep 2025 23:22:53 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fd86567595c1d81406b79b81bd20e5703bb329b2fe23d1b56ac2c702f2da2e`  
		Last Modified: Tue, 23 Sep 2025 23:22:53 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20da0aa853125972a4f8f0adf791ae5805ffb3473fc08709660805c9cb2168ea`  
		Last Modified: Tue, 23 Sep 2025 23:22:54 GMT  
		Size: 4.1 MB (4069891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a2cd957960978a9d3a6b5020e2205d1044746854a38d6f2e05c40892d7dba0`  
		Last Modified: Tue, 23 Sep 2025 23:22:59 GMT  
		Size: 75.6 MB (75566056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbf6ec5e7e224fae9f6d75931ba9f6ec8850502d9ce8fc26675f0fbe7d7bd8c`  
		Last Modified: Tue, 23 Sep 2025 23:22:53 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:f8721b0ab08975f7831d3f381cdafa198063b98f2f877f7e484a49acd9eaac40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2cca90a46e0ef25422c204efe5b65df0eab170c9eb7b45baaac014ec83ab79`

```dockerfile
```

-	Layers:
	-	`sha256:df1883352ed752a48607f9d7af248e0d5169411c9c4b36559672a85e6625b709`  
		Last Modified: Wed, 24 Sep 2025 01:51:46 GMT  
		Size: 36.8 KB (36840 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; riscv64

```console
$ docker pull redmine@sha256:49e18dade03bfcb24a297e9ceed7c6cdbd67055d91bc4a2c2c1bbe14ebd0caf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188680964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39710bad6683b57f018c42374ee03b5007da7d803789d298c42c5c2e18725928`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c4be3fb7c48ca84ee50be475d7d4a527212bb75b64469ee7eb6e6f0a98941f`  
		Last Modified: Fri, 18 Jul 2025 03:36:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af990bad08aaf772d4ffcb9f06a602319d08aef90e9237bbb8ee4e99946120f`  
		Last Modified: Thu, 24 Jul 2025 21:22:31 GMT  
		Size: 31.7 MB (31746901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590aa49d68bcc0b2b953b8aeb5192dc3617a732a168b59d588c9d1d2ecffdace`  
		Last Modified: Thu, 24 Jul 2025 21:22:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598f300a0267f059e27772110b4c1780006c2a98b756acd2490d11a4b516f573`  
		Last Modified: Tue, 23 Sep 2025 03:31:58 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4aa886188321d90c756c0e3dc29d9d37afb9b9da7473dcf1d56f017f2d852f`  
		Last Modified: Tue, 23 Sep 2025 03:32:03 GMT  
		Size: 71.5 MB (71468597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32926b748278afb198304ffd77e8fddb2b7113634ca3cc63184bf21e0b9cbfd3`  
		Last Modified: Tue, 23 Sep 2025 03:31:58 GMT  
		Size: 914.1 KB (914123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b85713057c411c22171c0ee24ad29365549f6fa0b357a99b3318e707db54d8c`  
		Last Modified: Tue, 23 Sep 2025 03:31:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725ca9096a3503c6c3a8532d621c501e10350b2b9bda9d69d64784b7a787d26`  
		Last Modified: Tue, 23 Sep 2025 03:31:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c585e23fd0504026bdd52a01630531a11592c04ce5c1f50204e5782659cb8e67`  
		Last Modified: Tue, 23 Sep 2025 03:32:01 GMT  
		Size: 4.1 MB (4069921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1798a74ac0409f653834d4cbf9c9f3a8b81ee0a50f67bbc72ac04befbb7ba886`  
		Last Modified: Tue, 23 Sep 2025 03:32:08 GMT  
		Size: 77.1 MB (77128482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c04e8db4b9dba81d6b490863656127250cea487080a7f84801ca8d8e17c4527`  
		Last Modified: Tue, 23 Sep 2025 03:32:02 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:6bdc8429cd068dbb3b9210a351a4be7576a09aace386fedc620f33b4bbd4b7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a9b164d2f3af7e0b4f7b33c9334407e8b0208e9fd0b42a5a31df8ca42fee6c`

```dockerfile
```

-	Layers:
	-	`sha256:b9ab1543ab60b8941b72f1b552dc4eecf861c90cdd272fa6526c6469c75dfcf0`  
		Last Modified: Tue, 23 Sep 2025 04:49:58 GMT  
		Size: 36.8 KB (36839 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; s390x

```console
$ docker pull redmine@sha256:47a06ed492942754f71be89581b33dd69f4212606f7372fd58bf8bef9a52976e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190129769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1476dfb17396e9f3fe47be69eb7d13d1e4255043b207f1ee60cfd160a94624d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f70e23950b298583307250026bf211e6e69f1f04bf424c27ce5cf1cd1fad65`  
		Last Modified: Wed, 16 Jul 2025 04:44:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc5994e3e7f2ba57e4e98b07425316eb455c49533613b82fe3cf226bce501d7`  
		Last Modified: Thu, 24 Jul 2025 21:56:21 GMT  
		Size: 33.2 MB (33245157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a3915b37178951f6bf6db0323dd06587ba7079824f4956c6845fede9501d0e`  
		Last Modified: Thu, 24 Jul 2025 18:46:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227417db301e7a01a367c43e92c4d580c1bb05c7860db4a907644b433e868464`  
		Last Modified: Mon, 22 Sep 2025 22:43:16 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae2c297f5ea8131693065dcd6eb0ede366904e7eaa314a7d6c70e5fe3de4414`  
		Last Modified: Mon, 22 Sep 2025 22:43:21 GMT  
		Size: 73.4 MB (73438633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495bd2d4486c11e7ece40118fe2a3675f25d15ec502d1a5f92edeab8f5ad4939`  
		Last Modified: Mon, 22 Sep 2025 22:43:16 GMT  
		Size: 942.6 KB (942565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9c0506c1186800103c31963797f2870401b6d7bb5f3ffaa95e7a85d831069a`  
		Last Modified: Mon, 22 Sep 2025 22:43:16 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673a471c125efede177f511654a935756fd22e897aa06604cb382ae6775786c7`  
		Last Modified: Mon, 22 Sep 2025 22:43:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13478ab893b24d96f1e09e27d89b20c9474108496f92fd7dd05ffcff9a2f2d3a`  
		Last Modified: Mon, 22 Sep 2025 22:43:16 GMT  
		Size: 4.1 MB (4069907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937cf0c79756ec73c86dfde1a407276941b69652d1a2b4d1e629291c736fb9ab`  
		Last Modified: Mon, 22 Sep 2025 22:43:37 GMT  
		Size: 75.0 MB (74967556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224de524ff5630ca1cc149c6aae290f052ae41eb8ce1797a623689dd848cc0ea`  
		Last Modified: Mon, 22 Sep 2025 22:43:16 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:44154d30643244ec998dfb321e6b0d9addea54a6c5e367e1643566ed32184735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9470d38f975956aa1f50b23cfc38098ac51b6fe3c073e127785f34939571074e`

```dockerfile
```

-	Layers:
	-	`sha256:1a695af46944d4f9ffc206e521252c40e50b058f9d37607c5785edda88558389`  
		Last Modified: Tue, 23 Sep 2025 01:53:14 GMT  
		Size: 36.8 KB (36786 bytes)  
		MIME: application/vnd.in-toto+json
