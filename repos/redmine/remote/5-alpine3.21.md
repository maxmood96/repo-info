## `redmine:5-alpine3.21`

```console
$ docker pull redmine@sha256:cc69a967a7ecc734b410506fb1b370432948f88fa563323e689a9387c3f211de
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

### `redmine:5-alpine3.21` - linux; amd64

```console
$ docker pull redmine@sha256:34dcb50960962801d6e1cf504c6f55e220992c1d1eb735acbf152aef4cd82da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185408578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c95e4bb560c3851a535a108be943493bc94083b0c0731ebc3a533551b21b44`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
CMD ["irb"]
# Wed, 24 Sep 2025 10:59:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_ENV=production
# Wed, 24 Sep 2025 10:59:56 GMT
WORKDIR /usr/src/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
ENV HOME=/home/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 24 Sep 2025 10:59:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:59:56 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 24 Sep 2025 10:59:56 GMT
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
	-	`sha256:6172d1d629f40620f00391d37a59b509102f276749fea2ef15d5f571754c5611`  
		Last Modified: Thu, 24 Jul 2025 18:46:02 GMT  
		Size: 33.8 MB (33801398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd3bffeaa790a083b73c4c9e7f5d5f92987665be2005d75cdaf8fcb38faeea9`  
		Last Modified: Thu, 24 Jul 2025 18:45:57 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643a965e5a1bfaba6dfc44a5e6c353ee6ca4b60dc61e5b9df5a8978bb1d2461f`  
		Last Modified: Wed, 24 Sep 2025 20:41:59 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446820baff633e2006c8b8f94d9d51b4c20a700fb3a5b8bc4a1824fb9eb44afd`  
		Last Modified: Wed, 24 Sep 2025 20:42:04 GMT  
		Size: 72.4 MB (72375687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07da22e6aac0d703d305f7ec6aaeb284ff5a7c28b33630542a64830397b006b`  
		Last Modified: Wed, 24 Sep 2025 20:42:00 GMT  
		Size: 966.8 KB (966810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af54e7a2d43fc99ef9b1ba81293f98cefcd9c0d229dd255b493458b5c667c626`  
		Last Modified: Wed, 24 Sep 2025 20:42:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5558e5be90ae745162904a2abc69df52f04efb025d4a0d47118900370dd10015`  
		Last Modified: Wed, 24 Sep 2025 20:42:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245d2126fdba43da258239583797d0f6351c4658a240d3b4bb54743dcbf036af`  
		Last Modified: Wed, 24 Sep 2025 20:42:01 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66187145947fe0a20d99aa6881ab9da540db3e8022d6d8ac1459ed703de2e764`  
		Last Modified: Wed, 24 Sep 2025 20:41:58 GMT  
		Size: 3.3 MB (3252443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da993cd0aa94e111516311698a5ec10f556b75def4f9ad3f5ad3c4572c9dc6c`  
		Last Modified: Wed, 24 Sep 2025 20:42:04 GMT  
		Size: 71.4 MB (71370649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377ddf180ddb942889fb17562e082c925553f98fd909b699381bde1a8e49b4fa`  
		Last Modified: Wed, 24 Sep 2025 20:41:58 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:182e0630f53822899b3155d0156f55695b57f0d61e942db7bf40a2c7f7c4bda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100efd8a6be109912af2375523f56090f565b30f3dc578a2f751010b717ede1d`

```dockerfile
```

-	Layers:
	-	`sha256:71995e3ec1c119422d38ef7c1692657772bd42f4ea22144b063eac1056c16c14`  
		Last Modified: Wed, 24 Sep 2025 22:50:43 GMT  
		Size: 39.8 KB (39800 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; arm variant v6

```console
$ docker pull redmine@sha256:abed20326c9786fecbfe0f7bd0e3fd10e5eada1180c8fed305b199a37a1cf586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177139808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684ab41353d2925a828d80b5cd249ad279302ce2cbb8dd9a6ec5b7ecc4035483`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
CMD ["irb"]
# Wed, 24 Sep 2025 10:59:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_ENV=production
# Wed, 24 Sep 2025 10:59:56 GMT
WORKDIR /usr/src/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
ENV HOME=/home/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 24 Sep 2025 10:59:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:59:56 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 24 Sep 2025 10:59:56 GMT
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
	-	`sha256:dacc81117a9a8424d9fd77d55f7dee1a6a17b35ff92326f1748a5233c3a031db`  
		Last Modified: Thu, 24 Jul 2025 19:50:39 GMT  
		Size: 30.0 MB (30046187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c922ce2777c189ed8dd5b24e1c30f0f94da829ef1888e7b1ee2eb11faa24ac17`  
		Last Modified: Thu, 24 Jul 2025 19:23:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6060c183aa1b043bf51e31789dfac4756ffd11bc68ec7abd9e7adb242faf30`  
		Last Modified: Wed, 24 Sep 2025 20:38:01 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2ec16f011b19058c98af01d681046035016e139cf89788d6f9def5615048ba`  
		Last Modified: Wed, 24 Sep 2025 20:38:09 GMT  
		Size: 69.0 MB (68965954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4481c65775cdcf6fd630cf930ae0475b3a43fea1e2873edce28a2ba737831cce`  
		Last Modified: Wed, 24 Sep 2025 20:38:01 GMT  
		Size: 934.7 KB (934730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441486ce415d6c49c164343472f965b0f13c10d5f94b24c91d879f8c28ace26d`  
		Last Modified: Wed, 24 Sep 2025 20:38:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb19a3c945e67d272a1ef4c5a02b0c1251c882d11930b8dae66f60f353ba5db`  
		Last Modified: Wed, 24 Sep 2025 20:38:01 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b219857adac32ab63aa1a81a4240af9ac10a365b153438d00bd29409ebb7591`  
		Last Modified: Wed, 24 Sep 2025 20:38:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55290e87611a66dd55393285b34969c9226634d13316496e9797aecaa77ca16`  
		Last Modified: Wed, 24 Sep 2025 20:38:04 GMT  
		Size: 3.3 MB (3252455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f94a34f9aa69ebaf9532a9f5091ff8635e4ef6a06b68688b80423a649a2c92`  
		Last Modified: Wed, 24 Sep 2025 22:52:21 GMT  
		Size: 70.6 MB (70572645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936ba5ea6269f57a035ea5ca2cc492abe0d9179a24678457d28bb2711c2aa177`  
		Last Modified: Wed, 24 Sep 2025 20:38:04 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:0f946710b84ce2df66ef8b06b1a864e306fd15e94ba2d8df41cf330afa35d60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 KB (39951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004632820672afb0f7d26b966edbb4633e3f0440e28c935f41321f66551b1084`

```dockerfile
```

-	Layers:
	-	`sha256:621080fb360c2a5ceafe8532c688dc24b7d1142016743ec864f7674c704ef5ef`  
		Last Modified: Wed, 24 Sep 2025 22:51:34 GMT  
		Size: 40.0 KB (39951 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; arm variant v7

```console
$ docker pull redmine@sha256:cdb0a58462b2b0566f051287f2804758744c83def074cc480943dba6a70cb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172962935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91323e043571831b777194fb9656bc1284868e5cda4aa105b23f4ce82bae335`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
CMD ["irb"]
# Wed, 24 Sep 2025 10:59:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_ENV=production
# Wed, 24 Sep 2025 10:59:56 GMT
WORKDIR /usr/src/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
ENV HOME=/home/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 24 Sep 2025 10:59:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:59:56 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 24 Sep 2025 10:59:56 GMT
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
	-	`sha256:06ca15b336b87002e8a140dfaab86a6ccabfc9645040c659b82e264a116eaace`  
		Last Modified: Thu, 24 Jul 2025 19:01:13 GMT  
		Size: 29.9 MB (29906728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f48e937ddb2d38d581f5e79912055776ca8712fd9ecbe5426f155caab29b8c`  
		Last Modified: Thu, 24 Jul 2025 19:01:11 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9605f77cb35a1c54eedb2ed2c5e85ca406a5545d681109d657a75b60418c924c`  
		Last Modified: Wed, 24 Sep 2025 20:40:03 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ab3f2fcca887021550d23ccfa3eae8cbc505e6da9cea662b31af8410367a9`  
		Last Modified: Wed, 24 Sep 2025 20:40:18 GMT  
		Size: 66.1 MB (66140942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1850113630c129f4addcbb159470129740a2bb68fe9298b3b2edb2e32194d3b0`  
		Last Modified: Wed, 24 Sep 2025 20:40:03 GMT  
		Size: 934.7 KB (934723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98eb45b373e73303a1506380a76bd8cc7b1620628e8710144391203a362f93c`  
		Last Modified: Wed, 24 Sep 2025 20:40:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45f01cd697d30ccf670efb715bd4ae52bd2356df000044f66277a71e0a3d535`  
		Last Modified: Wed, 24 Sep 2025 20:40:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83a6fd040c55efe0d57566e7054564926d78c30bc73221b77813737ec9f270e`  
		Last Modified: Wed, 24 Sep 2025 20:40:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8274823e0d46072f9661d55d494929ffe4cc32a8b09bb266072a91c779a847`  
		Last Modified: Wed, 24 Sep 2025 20:40:07 GMT  
		Size: 3.3 MB (3252456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29048d5b4aebc8b294d59b661bc0bf17b57a80512d7df88d71de216bdde3ea11`  
		Last Modified: Wed, 24 Sep 2025 20:40:13 GMT  
		Size: 69.6 MB (69627192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f52284bc5928151dc08bd5a6302e01d3416b8239f2c45f4a86aa47abbe0a63`  
		Last Modified: Wed, 24 Sep 2025 20:40:07 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:7643240d6f8c017e2416bf0e32d9ca362d56b278be6fdd4f0dc4e7fd57aa2a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 KB (39952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90fb78c8c12b6224a0dd5ff1d43a87bb3e9fad4e605cf83d13838fcd855719e`

```dockerfile
```

-	Layers:
	-	`sha256:48a3e66a1b189109d4cc5cef53fb999837631a4c6f02939658f94bdd835475c6`  
		Last Modified: Wed, 24 Sep 2025 22:51:37 GMT  
		Size: 40.0 KB (39952 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:954f899a42fc1c4be3f35c7ee185d0aedcf5701b9b2b5829460d13295720c6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185325399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb828c5418383dc002b37a71f966382df1383d1948b4f1cbdbd08d17b521fd72`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
CMD ["irb"]
# Wed, 24 Sep 2025 10:59:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_ENV=production
# Wed, 24 Sep 2025 10:59:56 GMT
WORKDIR /usr/src/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
ENV HOME=/home/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 24 Sep 2025 10:59:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:59:56 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 24 Sep 2025 10:59:56 GMT
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
	-	`sha256:410c154fbc9e12cd9d897559f9a934096cfb699f60f51d1de5b9111ae25c0208`  
		Last Modified: Thu, 24 Jul 2025 18:49:41 GMT  
		Size: 33.7 MB (33746191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8199f7009e45c8e148a328e6883ae7d296c54893949bad526249a2a48b5f29b`  
		Last Modified: Thu, 24 Jul 2025 18:49:34 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337bc0910d1683a8f7f415d5d5b8d1d5f04c9e0ba16afb77599a589ec1e52452`  
		Last Modified: Wed, 24 Sep 2025 20:37:15 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5628659f6e6e1b919bd3b6cd4aa7e139703a7ff12d7ed7e591a35495e9a5daa`  
		Last Modified: Wed, 24 Sep 2025 20:37:32 GMT  
		Size: 72.0 MB (72048966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b894b6a3a3d3d32a8021ebecb5107cad54d86af66843552b5b5f814ae28199`  
		Last Modified: Wed, 24 Sep 2025 20:37:15 GMT  
		Size: 922.2 KB (922194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b2ade65755bce3c82a0b5eddbb83a33877b95db5480b7c5486dd4faa784386`  
		Last Modified: Wed, 24 Sep 2025 20:37:15 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4b4683763d06f4c80d83d2de3d5e14574ccc9d6ab2bb1ffe3b25ab07d66e48`  
		Last Modified: Wed, 24 Sep 2025 20:37:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1b54816df2539395a235f83042089307b23a8f13489e0d83969710f6ee35aa`  
		Last Modified: Wed, 24 Sep 2025 20:37:16 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96350ce4fd0f028edcc1929ecad940638f3d222fd3635c5cf76f297d6621f61`  
		Last Modified: Wed, 24 Sep 2025 20:37:16 GMT  
		Size: 3.3 MB (3252450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4df6f66748b6acdc41e3cfddb0f904df84884b364657316e4fb5c18ff98495`  
		Last Modified: Wed, 24 Sep 2025 20:37:22 GMT  
		Size: 71.4 MB (71364640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4cfcb799dfd6c955251fca06549997cbe753be8d5b2c1aebb38b160b039891`  
		Last Modified: Wed, 24 Sep 2025 20:37:16 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:474d442a8820f9236e812378628fffab5e052dc7bcba3cfcfadee01eb75e415b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 KB (39984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682f2c5e85d03697adbdd8114f1e2d2b2cbe4540b954c2576a52826b4762262d`

```dockerfile
```

-	Layers:
	-	`sha256:7d20d44459e4ac2531dd0ffa591fcbcfa607575f4c56d3ecc0f3da4a091861cd`  
		Last Modified: Wed, 24 Sep 2025 22:51:42 GMT  
		Size: 40.0 KB (39984 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; 386

```console
$ docker pull redmine@sha256:ee1a33cd7d629394542fdfc36a8d5bb3cc5c202f7058d10c1d7965330e4e47f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182022254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d4b731480491fd40c7ba3a5b5213f600516c390a1f4f328bae7e5dd60a7913`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
CMD ["irb"]
# Wed, 24 Sep 2025 10:59:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_ENV=production
# Wed, 24 Sep 2025 10:59:56 GMT
WORKDIR /usr/src/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
ENV HOME=/home/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 24 Sep 2025 10:59:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:59:56 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 24 Sep 2025 10:59:56 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512ed26d6f15c8965d33177673d3258df3825f4580edc6a03b47ea26ef3c3c8c`  
		Last Modified: Thu, 24 Jul 2025 18:29:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f818aa12ac4755c135fba7032c2097de3c53a632d97188a70de34fecd57164`  
		Last Modified: Thu, 24 Jul 2025 18:29:41 GMT  
		Size: 29.9 MB (29919580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c7b3d0c1b92289c0a9953c8c0a012f8eb6b2e3bb3aae7255933e600adce31d`  
		Last Modified: Thu, 24 Jul 2025 18:29:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffef55db75be1ce719083484fc907052eec3cb8949ad99badd5f89f3ebfc087`  
		Last Modified: Wed, 24 Sep 2025 20:37:11 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345cca32338c54545779dbb41fd39c2d78137c51403b7bf9e4b8b392e522284`  
		Last Modified: Wed, 24 Sep 2025 20:37:17 GMT  
		Size: 73.0 MB (73043213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5cf4b98d3eb164aec973f1b8422178d824a3b2ea8b1f83f17c6a18852a69d9`  
		Last Modified: Wed, 24 Sep 2025 20:37:11 GMT  
		Size: 939.2 KB (939250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1afd61f217a592d238b06187a00c17330e9a86f13e0d815686d862a078da346`  
		Last Modified: Wed, 24 Sep 2025 20:37:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256390f7b1d993c50f6f2908f370b247c4c41aaf1bed977a76392bdf6f04b658`  
		Last Modified: Wed, 24 Sep 2025 20:37:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b564403aa60551ab40c941fcde105b9ce41afb451be7d62485b06393871071`  
		Last Modified: Wed, 24 Sep 2025 20:37:11 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe6fed93d9aad1e29608d4184386c3f49214d70571c049ecea2cdd21ca29022`  
		Last Modified: Wed, 24 Sep 2025 20:37:12 GMT  
		Size: 3.3 MB (3252433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838cb68d74c6e71c5196c0f341fd54daa4111f68155ebbb727671b7e81a1c43b`  
		Last Modified: Wed, 24 Sep 2025 20:37:17 GMT  
		Size: 71.4 MB (71403027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4889e12a06f904401d04edaca066c31a38641834f13fb1825138c70fddf82405`  
		Last Modified: Wed, 24 Sep 2025 20:37:12 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:b22931cde9114abcd7013b0cae9804ef05521eec620eacf1e756455eac91e8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55e41514e5262a9b4954ab579529cd8fef960b2c699670cadb29c21bb5d725e`

```dockerfile
```

-	Layers:
	-	`sha256:26d2349c2db37d2590ac73f317bb6f98679d4eb197208994ad4576918aaf4179`  
		Last Modified: Wed, 24 Sep 2025 22:51:45 GMT  
		Size: 39.8 KB (39763 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; ppc64le

```console
$ docker pull redmine@sha256:0c9ec3a35d49c878aa1928139f75acc2a2927d7c673e6a43e4c45cfa64d0bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.4 MB (186369733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457d8c31871ee8034d4ca5dd58bf527cec5bb85679424cd48f4bfd24615750fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
CMD ["irb"]
# Wed, 24 Sep 2025 10:59:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_ENV=production
# Wed, 24 Sep 2025 10:59:56 GMT
WORKDIR /usr/src/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
ENV HOME=/home/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 24 Sep 2025 10:59:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:59:56 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 24 Sep 2025 10:59:56 GMT
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
	-	`sha256:8005f94f83889fd112af90e684c1cbb346bcdd4601df83e2e875621c5055826e`  
		Last Modified: Thu, 24 Jul 2025 22:11:27 GMT  
		Size: 31.4 MB (31387472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbe92e981b9736974a34524c72afa810835f8e477b94350d49b82188d324cac`  
		Last Modified: Thu, 24 Jul 2025 18:59:31 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2534fb31ebce5393c5190f9bfe665ec17c772c7ff3c07168c0dc43c658cda796`  
		Last Modified: Wed, 24 Sep 2025 21:29:58 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b0008d9c7511c8274001044ea40fa0fd4cb7b9ce16862142956115789c5f7f`  
		Last Modified: Wed, 24 Sep 2025 21:30:03 GMT  
		Size: 74.1 MB (74088413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0ebb2ed9e4cfd7c329b02dbf9744cbd5778f0f9d1b4ae659218a34abdf157d`  
		Last Modified: Wed, 24 Sep 2025 21:29:58 GMT  
		Size: 927.7 KB (927738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959afe4150d4f3ffa128478f59ff8a06dcc083284701cb754570e9fc5a5477cd`  
		Last Modified: Wed, 24 Sep 2025 21:29:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e407684ce18341401918682bece683172cec50ff51fa4b5bcf924a3fd1ce27`  
		Last Modified: Wed, 24 Sep 2025 21:29:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec92a3a57c17351cb9fceebd79c4b4498b1386fcdbd08c96318ac93967ca3e98`  
		Last Modified: Wed, 24 Sep 2025 21:29:58 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8964b4b7073dc6325a378a736c785995ad001b0c77f659b6c7befbf129fc616`  
		Last Modified: Wed, 24 Sep 2025 21:30:00 GMT  
		Size: 3.3 MB (3252462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edac23f623ba011b28ee49a2b3e552e5a9e4183c475b392357eb3659dc152785`  
		Last Modified: Wed, 24 Sep 2025 21:30:19 GMT  
		Size: 73.1 MB (73140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4197f5c3d1d1757f747ff4ef28045f4a9e65744b3019c4c7c3b2a3501e428d5d`  
		Last Modified: Wed, 24 Sep 2025 21:29:58 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:7a4c32163f32b185fa8fe08ec73b7df8a8df6418c5b701208384e9b7decc4243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 KB (39852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354a287ad7cc74cf6d21e36ca29864b6ddf70b7ba2319dbc5dd8e42d99091b68`

```dockerfile
```

-	Layers:
	-	`sha256:a801d9e1aab4f86647921935d585b2e2c352100bf86d8e071098f69a27c5abc9`  
		Last Modified: Wed, 24 Sep 2025 22:51:49 GMT  
		Size: 39.9 KB (39852 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; riscv64

```console
$ docker pull redmine@sha256:336073f1456a422c8b52149fab746dcbd60f9c02f8220d224788f39cb85c69e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183135067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855394aaf22eaa768c78a7c71f4e0b00edbe46f79b5c84d6556adcb611d9631f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
CMD ["irb"]
# Wed, 24 Sep 2025 10:59:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_ENV=production
# Wed, 24 Sep 2025 10:59:56 GMT
WORKDIR /usr/src/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
ENV HOME=/home/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 24 Sep 2025 10:59:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:59:56 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 24 Sep 2025 10:59:56 GMT
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
	-	`sha256:b3507f60b5910767a7f2fed904d55b121435bb78f6ca06334b520007807bc0ec`  
		Last Modified: Thu, 24 Jul 2025 23:23:21 GMT  
		Size: 29.8 MB (29798305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a5bedb866ec6e8b8157a77edbe90835f9a6f754deb8704c006397710963f5`  
		Last Modified: Thu, 24 Jul 2025 23:23:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf65a0a17ea4a047a8ad79c1bb1ca9b37b98bac406d1187d6ef990b54fa5bff8`  
		Last Modified: Thu, 25 Sep 2025 09:22:10 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed722f3ea2a1e22b7a9cff531ffe36e777e30e6e9cdafdeed9086561389d82b0`  
		Last Modified: Thu, 25 Sep 2025 09:22:17 GMT  
		Size: 71.1 MB (71149546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5762a96b9ace7c7751c85bcdb630b86a97a29e260a514e42e11710e59be1a696`  
		Last Modified: Thu, 25 Sep 2025 09:22:12 GMT  
		Size: 915.2 KB (915191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae17977e4de30a481a8337e0090b6136582cbd8c5557b4aa63304693173bc7a`  
		Last Modified: Thu, 25 Sep 2025 09:22:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6d0ee70afdff673334d545d4a79c11565f1d9a0c107e618d8144e2f3cdf673`  
		Last Modified: Thu, 25 Sep 2025 09:22:14 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1174e8aa247030de92361387447aaadec7373cd773d47e0f241471b71c0af9cc`  
		Last Modified: Thu, 25 Sep 2025 09:22:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b5b6f8bcc2c8fd3d2c430e3cb959ff70f6134819d76273b45937026298de4a`  
		Last Modified: Thu, 25 Sep 2025 09:22:12 GMT  
		Size: 3.3 MB (3252478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4ff5c16f818a906d533724de2833701967e70cf42e317ed5bdf9e27ff97782`  
		Last Modified: Thu, 25 Sep 2025 09:22:16 GMT  
		Size: 74.7 MB (74666435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff3c2dcf03454be224e7a8925812fc397b9f728b4c2a4993c3cbd50e309ccaa`  
		Last Modified: Thu, 25 Sep 2025 09:22:10 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:0990ade286628e4083a3bf879476784d1cec039ccb7fe5056f3e1e1d142daa60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 KB (39851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3de44811544a070434da49de4c60885b3f144560801e62dc78826857c60a29`

```dockerfile
```

-	Layers:
	-	`sha256:45a79087c4f5fd055b0a6dff200ae314b4eeb95f0a9f029111e8ff66fbcb560c`  
		Last Modified: Thu, 25 Sep 2025 10:49:45 GMT  
		Size: 39.9 KB (39851 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; s390x

```console
$ docker pull redmine@sha256:e1897aac0d31febc48ad73fad2ded9b2ba39bf4411ad137e48dae0d18849b5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184578282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2552098b16ecb23568cc7965929109526057b543a39e901f38cc1b0c409e7a34`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV LANG=C.UTF-8
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 24 Jul 2025 11:03:09 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 24 Jul 2025 11:03:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jul 2025 11:03:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 24 Jul 2025 11:03:09 GMT
CMD ["irb"]
# Wed, 24 Sep 2025 10:59:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_ENV=production
# Wed, 24 Sep 2025 10:59:56 GMT
WORKDIR /usr/src/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
ENV HOME=/home/redmine
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_VERSION=5.1.10
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Wed, 24 Sep 2025 10:59:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Wed, 24 Sep 2025 10:59:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 24 Sep 2025 10:59:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 24 Sep 2025 10:59:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 24 Sep 2025 10:59:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 10:59:56 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 24 Sep 2025 10:59:56 GMT
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
	-	`sha256:a4bd08e4cfff326289f5e869cfa412ee53188189d2c0b4eccd701125d33712ce`  
		Last Modified: Thu, 24 Jul 2025 22:11:40 GMT  
		Size: 31.2 MB (31228570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a784fceb557b98d0b4247c55b2234550338a1a0caac3e1181c97c5b8a259d27`  
		Last Modified: Thu, 24 Jul 2025 18:59:30 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593d2b11cb4357ab701b31c2b52a757330a8b74232faa1bdacbc953ee0f5b620`  
		Last Modified: Wed, 24 Sep 2025 21:33:53 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c165dcdd46076a6160a106a945e1861e94006747333a9c290db78140316e504`  
		Last Modified: Wed, 24 Sep 2025 21:33:58 GMT  
		Size: 73.1 MB (73092738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeec64a9006ece4aead5f92255310395a294a92a0fd6d1d5ce2af5d38842c9b8`  
		Last Modified: Wed, 24 Sep 2025 21:33:53 GMT  
		Size: 943.1 KB (943136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bfd135a71c816d29973d43134e5a4b615ab31c7098de08e28c014e0ba63f7c`  
		Last Modified: Wed, 24 Sep 2025 21:33:53 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6396c4dfbe1a70e9140713556dff387392860204d7b84d9f3c9234007f0cf15c`  
		Last Modified: Wed, 24 Sep 2025 21:33:53 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c309e520fd151f554802012687e035174ee6b5ca5a8cd4111e5faaefb564e51`  
		Last Modified: Wed, 24 Sep 2025 21:33:53 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d990f9dda4b74917de96e787d432f5138556b94aac412829a3a7f9fd834ae1`  
		Last Modified: Wed, 24 Sep 2025 21:33:53 GMT  
		Size: 3.3 MB (3252452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ae63f3c05f6033d4c48709838985659c5a6b1714968b393609e0c3cf170704`  
		Last Modified: Wed, 24 Sep 2025 21:33:58 GMT  
		Size: 72.6 MB (72595266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9e1f44c9d8bc9942c603c69f9d630e634ac5a908d695637fe8451261f3a44b`  
		Last Modified: Wed, 24 Sep 2025 21:33:53 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:91b60235cb79c53bf4ddf6abb2e04f4ebd8df24923501fd3510cf9e0697513ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32dc0922b5b12ee70f0006f95862443617c3532f47a811d485a2e2a21dc2d9`

```dockerfile
```

-	Layers:
	-	`sha256:cc97c36dbbdabb0fd893d3a5e66892d280b0eb0df198771ab8733e63db845e64`  
		Last Modified: Wed, 24 Sep 2025 22:51:55 GMT  
		Size: 39.8 KB (39802 bytes)  
		MIME: application/vnd.in-toto+json
