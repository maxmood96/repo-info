## `redmine:5-alpine3.21`

```console
$ docker pull redmine@sha256:364b93c67b9bd4d3566687a0eed683f6971631a914d3cd3ad0ab4cfed392f7c6
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
$ docker pull redmine@sha256:133af0d1dfe16e095dd6b92eae1185cdacbc7338b36abcae56df2a34efad32b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185399631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be47754c948cb327e9d02f25db8441a889051f269b0a93259eb42b3ed53b4e6a`
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
# Sun, 21 Sep 2025 14:26:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:26:11 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_VERSION=5.1.10
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:26:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:26:11 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:26:11 GMT
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
	-	`sha256:46b3dcc5f4ff90184bdb3057678b78e725bc8ea21666605ff8bd01d27cff5bf0`  
		Last Modified: Mon, 22 Sep 2025 23:49:27 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3101fc0453345f2aa408fa645a3b2c9f64bbfd1a8e0b7efb12c2daa4cd8a40c`  
		Last Modified: Mon, 22 Sep 2025 23:49:34 GMT  
		Size: 72.4 MB (72375813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d612729c88cee10c2029d1b37a21726e6086326c3a4168b08b6370486a1ec`  
		Last Modified: Mon, 22 Sep 2025 23:49:27 GMT  
		Size: 966.0 KB (965959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99b72382e4ea505a1cdb9199a7fdb3ebbbb466e3920fca76450dffaf6c8e776`  
		Last Modified: Mon, 22 Sep 2025 23:49:27 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d467e2afee388eb5ec97e361021dc22057dd62a038da118f3a28af7a793819`  
		Last Modified: Mon, 22 Sep 2025 23:49:27 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105acb4ddae8afcf272e565ae5e0ff6fa2565283afd3b3812036fdb65c02778a`  
		Last Modified: Mon, 22 Sep 2025 23:49:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3579eb5e89fea513a6116f812c0d2eb2a9e34e701cf5bfe82d47aa44b3fc3ca0`  
		Last Modified: Mon, 22 Sep 2025 23:49:28 GMT  
		Size: 3.3 MB (3252122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9ca2f893d5118b6f12290b8fd73a110120ee763e9c3e7a02463386206c0763`  
		Last Modified: Mon, 22 Sep 2025 23:49:33 GMT  
		Size: 71.4 MB (71362743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05cd2db5c383253ab980d3e4dfc78385b5afd2f46932783cca5fcd3fc157d02`  
		Last Modified: Mon, 22 Sep 2025 23:49:28 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:5e42a778700aaa9597ad1b8261843ec7cc5e38fb9922c86e42aa034678b045d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955610e33fbcd53cd1794a3830643db1b5d31e1851233e5e5084ae03040a9ced`

```dockerfile
```

-	Layers:
	-	`sha256:90441d358919ea0123860abb966d12103ef5704c579420365fb620daf82c24d1`  
		Last Modified: Tue, 23 Sep 2025 01:50:47 GMT  
		Size: 39.6 KB (39638 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; arm variant v6

```console
$ docker pull redmine@sha256:b61aa052dc5ff2440e8a039d92228b192bc59ae160840cfbff50d94fde0a2d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177137427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64e3e8542ee4284c6f2053218cc06fa0a8837b4d57e640bd17a4ce80dee715f`
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
# Sun, 21 Sep 2025 14:26:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:26:11 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_VERSION=5.1.10
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:26:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:26:11 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:26:11 GMT
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
	-	`sha256:badaefae735d0361211f024bd750211fbfddcbcc3256aa59f005ef3bcea75d26`  
		Last Modified: Mon, 22 Sep 2025 22:16:55 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca8893a12ed2e73dd91204f7b37a4bd988a7559f5fe9dd0f04a0e3f7cb20d0e`  
		Last Modified: Mon, 22 Sep 2025 22:17:06 GMT  
		Size: 69.0 MB (68965681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0d8c0933206ca6109b919fb831b4341f66ad811805f58a94d0877121b8152`  
		Last Modified: Mon, 22 Sep 2025 22:16:55 GMT  
		Size: 934.0 KB (934015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b0dfe64c5a85af77d9ec2ce3db4109ba81f9477faf5bc81debd5bc686dbdfd`  
		Last Modified: Mon, 22 Sep 2025 22:16:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deeaaf1ebea3a9265716cfaeaae21e5620e3d16e154c816a4e424dca08b92ed`  
		Last Modified: Mon, 22 Sep 2025 22:16:55 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffc930e03b8e2e8302ff06a5682ffacc1b80e339e87d7f011bc44ce91d88704`  
		Last Modified: Mon, 22 Sep 2025 22:16:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9fb3cd46ebba370da40203b7d6eecd84315e6ee668bc1ae1974c41abc0766`  
		Last Modified: Mon, 22 Sep 2025 22:16:55 GMT  
		Size: 3.3 MB (3252446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa39c6ecd3db0bf3be5699d53528b27c6c1cd453aaf79b2176fdb5d3e6125d4`  
		Last Modified: Mon, 22 Sep 2025 22:17:05 GMT  
		Size: 70.6 MB (70571259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363a0844e8d3062dbdad38c97bba2699bfb04bc473289f5ed9e2f984e2a9a65a`  
		Last Modified: Mon, 22 Sep 2025 22:16:56 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:6783274781af8aefeda3b0afbfdd86aac1370e2c786aece0326f0299adee2361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bd52d8bdd68d9d330d00a371319750380f8a2bbf688e9a59ca6978b01eac7b`

```dockerfile
```

-	Layers:
	-	`sha256:0d520f10f148f49d906748df9a8b1a07fdf4c4b92da4e348de7f45a896a96911`  
		Last Modified: Tue, 23 Sep 2025 01:50:50 GMT  
		Size: 39.8 KB (39788 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; arm variant v7

```console
$ docker pull redmine@sha256:60620f0b62f1ea5aa35280de8676e6d76edd0000902a0676dbfb52df6a8c4343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172959285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26113f3b6b7b027b85ae96627c2bd7bbbe22b8261797d47ec30dd5b0df1b792`
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
# Sun, 21 Sep 2025 14:26:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:26:11 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_VERSION=5.1.10
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:26:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:26:11 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:26:11 GMT
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
	-	`sha256:84864d68bbe32631672cc1f37c818740c1137f767f44860620edcf82dd839c99`  
		Last Modified: Mon, 22 Sep 2025 22:20:56 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d262fa259c0029f4b7c319e7e9ed60ae0b839cb807b8ff43c4c56de1fa616ae`  
		Last Modified: Mon, 22 Sep 2025 22:21:01 GMT  
		Size: 66.1 MB (66141106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d143d5035871621212804cf97470d5fbb24eb790683daa4c1b5c8d03b181113`  
		Last Modified: Mon, 22 Sep 2025 22:20:57 GMT  
		Size: 934.0 KB (934010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fc5c7e7f544ed82d0715f4a069b6884c14d4e71852cc788dd95eec537489ab`  
		Last Modified: Mon, 22 Sep 2025 22:20:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08df51b5d68b5f5affeeb84df74ab26b7a0069814da0fe838229f843b14a24a7`  
		Last Modified: Mon, 22 Sep 2025 22:20:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae63d26972acbcb49dd738f5e71269f700608f368fda9b2cb006a5de3d4870`  
		Last Modified: Mon, 22 Sep 2025 22:20:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ce1b1d076d11774cd8f1b0f2d3dca93d24517a652b1c9322266de12d464591`  
		Last Modified: Mon, 22 Sep 2025 22:20:59 GMT  
		Size: 3.3 MB (3252479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6954de4ec0f79b7dbb99549b295c6ebd9615db10a64abda92c8ba668698800f`  
		Last Modified: Mon, 22 Sep 2025 22:21:04 GMT  
		Size: 69.6 MB (69624065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbf04b08674810f924d3f7815e10b53bf0c4688f5f6f78c0fdc3a11cf3491b5`  
		Last Modified: Mon, 22 Sep 2025 22:21:00 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:b8008fdabd5c008c834fdd8c3ce9836080f2aee906f17ed32c3273ae7fc2a94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382a0f4a38bdb6495297b734bcfdc2f977ca5881693f07b4b4925fb1b10cbe39`

```dockerfile
```

-	Layers:
	-	`sha256:3a205a374644792a05822a39eca614aa83b141abb8dd0fd4f60f0c14aeaf216a`  
		Last Modified: Tue, 23 Sep 2025 01:50:53 GMT  
		Size: 39.8 KB (39788 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:765eb56d010b889723df9b51ed6039c169d3d14bc6c4dc6d103d6bf3cfc70ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185318033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5ae80afd5e6647bc4b3953a0cbad1d2e3654442539d57beaadea9a39acec57`
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
# Sun, 21 Sep 2025 14:26:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:26:11 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_VERSION=5.1.10
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:26:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:26:11 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:26:11 GMT
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
	-	`sha256:2f9840c2ffab2f13f76825e9824fadf9dd00268193d6bb3452fddc41be7a43ef`  
		Last Modified: Mon, 22 Sep 2025 22:24:17 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddcd833c11422dc6357463f7a3b974143884e797e0859b81e8e8bdfb0ed25ba`  
		Last Modified: Mon, 22 Sep 2025 22:24:21 GMT  
		Size: 72.0 MB (72049155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f37626deb84ceb0b027ac1e7789ee4ae8d6219ee8982b85e453564a2eee8d3`  
		Last Modified: Mon, 22 Sep 2025 22:24:17 GMT  
		Size: 921.7 KB (921741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a833e5b86289aebcdec2845b87f48c5d1a20ed4c13ef1e3aceb8be625b298dcc`  
		Last Modified: Mon, 22 Sep 2025 22:24:16 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81eee7963c0e35204dee22be6cfd74e8fcf3150d3996643183d47123a55ca49b`  
		Last Modified: Mon, 22 Sep 2025 22:24:16 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94948078d940600512e102967e87ec5c53b656fc73fd0591502112578ae3a8b4`  
		Last Modified: Mon, 22 Sep 2025 22:24:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b885383f2e5aeb92ca4790b9bce76bb9bfeac354c5e4dba208f79cb85b46f336`  
		Last Modified: Mon, 22 Sep 2025 22:24:17 GMT  
		Size: 3.3 MB (3252457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f3cd280ddc8c6b2288f5154c8b0f7063d4a868b33ebb75dd77f8a2805015e1`  
		Last Modified: Mon, 22 Sep 2025 22:24:20 GMT  
		Size: 71.4 MB (71357529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7e013a286ea0fae4bda7ad0ec5fa0b884d7ba5af37f9fe72feae8677b76cb5`  
		Last Modified: Mon, 22 Sep 2025 22:24:17 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:27aba878296fcecf4292781568f1efe7e483b274e4a9af4751a3fbbbcda35b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b016960bfa48c695fb42d9603b97c2f4b96a9e19a788861d278a2dd8ef6e0f2`

```dockerfile
```

-	Layers:
	-	`sha256:695cc895c834335c85ee7d59f399af9beedee492fce40ba847f98dfd237f68df`  
		Last Modified: Tue, 23 Sep 2025 01:50:57 GMT  
		Size: 39.8 KB (39820 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; 386

```console
$ docker pull redmine@sha256:548aec2c8d25955fb20cd393cb28f78aee0e8b0da3d073bc8aa1720b4f74dd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182012592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdad069cc0ca540b7a3ae97a640477cdeaa77f57654de7d4ee940a149799c291`
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
# Sun, 21 Sep 2025 14:26:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:26:11 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_VERSION=5.1.10
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:26:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:26:11 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:26:11 GMT
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
	-	`sha256:478f1e0934724c293d5744e2b079dd2ac6ea61314f160a2330bcbb8f58a9b10d`  
		Last Modified: Mon, 22 Sep 2025 22:16:54 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c3e9ba9209232274a99a30dd43e1b9ade2046bf36b111b02dc316da8da7ddb`  
		Last Modified: Mon, 22 Sep 2025 22:17:04 GMT  
		Size: 73.0 MB (73043715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec5bd03c119c22f0a19723443ef27390925ba23e55f97f6f13f4c0ddff0c294`  
		Last Modified: Mon, 22 Sep 2025 22:16:54 GMT  
		Size: 938.4 KB (938396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3d7d0257a3598a4d268c848518284e6c8482482a3e0b0d77093fc6a85fa608`  
		Last Modified: Mon, 22 Sep 2025 22:16:54 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e064fe370fcc1f9c5019dfaf9a8e4b06c9d548975b662de17cbe958bfcce4868`  
		Last Modified: Mon, 22 Sep 2025 22:16:53 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996d40a3014691154f0ddab5a2eea0c813c75d7822b5ad946cde46e5288fb31f`  
		Last Modified: Mon, 22 Sep 2025 22:16:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f631302c938a98b86107b3454d368de95894de7d3b89cce2d0c1df3081688c3f`  
		Last Modified: Mon, 22 Sep 2025 22:16:55 GMT  
		Size: 3.3 MB (3252573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d901bdb682068d87a0bc910955f5aa045f0743a136ccfd6d5dbad7b2c97384`  
		Last Modified: Mon, 22 Sep 2025 22:17:00 GMT  
		Size: 71.4 MB (71393580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f164f105983373532ae4a07743648221d65bc682eeeb83862154544ee990833`  
		Last Modified: Mon, 22 Sep 2025 22:16:54 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:fe690e1122d91d9e37aef6e994668066f20e3f0fee8974a545aa852a50b3db9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5800e9b6926f33d48fcacb03a147cd635c17978b7e5b7b59c7967183e3630c15`

```dockerfile
```

-	Layers:
	-	`sha256:b89809075ff904ef74caed4993a0643382e120e3d1b53decbb4d0ef5af34726e`  
		Last Modified: Tue, 23 Sep 2025 01:51:00 GMT  
		Size: 39.6 KB (39599 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; ppc64le

```console
$ docker pull redmine@sha256:fbb44424729daa0389403e05f2759d8e3e81b5009a4f03274603bd364fcbc24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.4 MB (186365240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f570ce907830a1bdc992818e8dfbe91a2df181e25d454a7072a79fc4f441d6ab`
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
# Sun, 21 Sep 2025 14:26:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:26:11 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_VERSION=5.1.10
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:26:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:26:11 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:26:11 GMT
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
	-	`sha256:1d73b5ed8e45d4664f00c3c9a0ab8f9a8679958ae8f7ecb7dcfd4e75176fa025`  
		Last Modified: Tue, 23 Sep 2025 00:16:08 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24462518f6a0a25e5834af4ad7dda4453ceaf9e441414141e43adf546cb5db5f`  
		Last Modified: Tue, 23 Sep 2025 00:16:15 GMT  
		Size: 74.1 MB (74088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7132190c9b0197fb9307ec8a0b1bbd366cd8a0ca898d4c8c6560fb18e365893e`  
		Last Modified: Tue, 23 Sep 2025 00:16:04 GMT  
		Size: 927.0 KB (926986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b121d31a0d00eba1d6a14730def188e9fcb681659c6f2d2545caae6918aaab`  
		Last Modified: Tue, 23 Sep 2025 00:16:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9907db8b7d04ad979f52d86c932995695e10360ac3fec32261466f10a31c4dbb`  
		Last Modified: Tue, 23 Sep 2025 00:16:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bb7e13f1a1fdb2aa0803fcc00dd6f6332e8f9f0c1158551ea819995c2827da`  
		Last Modified: Tue, 23 Sep 2025 00:16:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738c08a4d26f0ef8c88199956c3c8132dcc521f23b69a00c1da778a505880395`  
		Last Modified: Tue, 23 Sep 2025 00:16:06 GMT  
		Size: 3.3 MB (3252530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507efecc7943b7de8ac41760a0716f290feaf94500621aa1dc5a32932fba8232`  
		Last Modified: Tue, 23 Sep 2025 00:16:15 GMT  
		Size: 73.1 MB (73136737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0c9d799cebf284db3f6596a217aef1e1fa738fd57d2f923b9421c1ca2ea73a`  
		Last Modified: Tue, 23 Sep 2025 00:16:05 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:1bd63df91edde1fcbd58ab7f241213376f75cd0e0ccddd4c9561e446425ecb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 KB (39686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34a87511f6af3205944deafa6f57d940d6a49f7332fee8c902843db86c8dd76`

```dockerfile
```

-	Layers:
	-	`sha256:99ca54a26e24119ed5dd7846fd41c567f7fe864c36f9f9efcd697c85bd509b8d`  
		Last Modified: Tue, 23 Sep 2025 01:51:03 GMT  
		Size: 39.7 KB (39686 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; riscv64

```console
$ docker pull redmine@sha256:b06d8edbf57ddb5fc4044a0e88be038864e294abdea9bd5cf2de0022a9786607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183125177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42d54083a0e67c11c338a633eb479c01f923c8deefbf67b7a71cf627ec5a1a3`
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
# Sun, 21 Sep 2025 14:26:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:26:11 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_VERSION=5.1.10
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:26:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:26:11 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:26:11 GMT
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
	-	`sha256:82bebd1e0a12d089f824810f5506a9ad3685202c709c79e160e1a52db6ec0bf8`  
		Last Modified: Tue, 23 Sep 2025 05:39:17 GMT  
		Size: 915.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ca0943840a889a2c7e2f518474f6a0786730bbe3af7564a9b76bf6016f9da2`  
		Last Modified: Tue, 23 Sep 2025 05:39:20 GMT  
		Size: 71.1 MB (71149577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cae2850fc2b8153c46f6f98578e4e95fa13f2e44c8bade96f2c15bd16ca39c`  
		Last Modified: Tue, 23 Sep 2025 05:39:17 GMT  
		Size: 914.1 KB (914140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1933c15e68c9893058416c0fce5a640d26b5fea03a6bcb22ef576399251f03`  
		Last Modified: Tue, 23 Sep 2025 05:39:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f02e7c9662ab341c53d87b21658b3e034f573b3027c19df610e75ffff959d5`  
		Last Modified: Tue, 23 Sep 2025 05:39:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7e119b2b18f9f2c9ad89a16d7117597c6dabc499a878fababddb1124719ccf`  
		Last Modified: Tue, 23 Sep 2025 05:39:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a69a9636c3737f4a1ca9672e4522496f20837cb3aaa8309b762d900ee9fbf1a`  
		Last Modified: Tue, 23 Sep 2025 05:39:18 GMT  
		Size: 3.3 MB (3252493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552a42313fd90090209e78352e7777fb535ee0ad34794185b642b5f037ed323a`  
		Last Modified: Tue, 23 Sep 2025 05:39:21 GMT  
		Size: 74.7 MB (74657543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71631b4785d8d0dc4ca12e0ed4ab545706ce9608857489d11f0b353f83d0cb18`  
		Last Modified: Tue, 23 Sep 2025 05:39:17 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:208a756b8d13824e80c2809ba199f43b901d57caa4e842220473e990228e5904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 KB (39688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd28ecb69eb9737011bbe7c73a57283c127ca10a0a75a5292e77c0da95483a7c`

```dockerfile
```

-	Layers:
	-	`sha256:3e47fcff829efe2623ebb23152de3d817971809db9a5e774b98dba543e90d6f0`  
		Last Modified: Tue, 23 Sep 2025 07:49:39 GMT  
		Size: 39.7 KB (39688 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.21` - linux; s390x

```console
$ docker pull redmine@sha256:7d2bc13e7958e4d75d3950ef73be01ff99f1612fb066aae1d5708ae9a38627f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184565243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dee5b19bd7897bb292169d5e38ce2cff1983b900df96a39638cdaf420e63d84`
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
# Sun, 21 Sep 2025 14:26:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV GOSU_VERSION=1.18
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_ENV=production
# Sun, 21 Sep 2025 14:26:11 GMT
WORKDIR /usr/src/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
ENV HOME=/home/redmine
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_VERSION=5.1.10
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Sun, 21 Sep 2025 14:26:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Sun, 21 Sep 2025 14:26:11 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sun, 21 Sep 2025 14:26:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 21 Sep 2025 14:26:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 21 Sep 2025 14:26:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 21 Sep 2025 14:26:11 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 21 Sep 2025 14:26:11 GMT
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
	-	`sha256:d659c7ed90d353aa38b1b52957204fc5d719081bb368dffb6a00b378a3ac014e`  
		Last Modified: Mon, 22 Sep 2025 22:53:55 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4402de6825c08a2520e5693b38666056d784b0178f633f457719b5e5f0e456`  
		Last Modified: Mon, 22 Sep 2025 22:53:41 GMT  
		Size: 73.1 MB (73092511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13014db6af55ec295771af23529d74fc9d7b0ee897b147df46e20eedefd046b5`  
		Last Modified: Mon, 22 Sep 2025 22:53:55 GMT  
		Size: 942.6 KB (942574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926b0ef9365f5af3ef55ed6ee625ce1379474724f0eee9982d9b5ab5511afdb2`  
		Last Modified: Mon, 22 Sep 2025 22:53:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b92e3ff6ee86f9b107ba347df271f13920642280a3a4a826ed1921088bf172`  
		Last Modified: Mon, 22 Sep 2025 22:53:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011a38818a92499b76a69b06aa5587954fc7a6abff3246e6f6a6aef88552e8ca`  
		Last Modified: Mon, 22 Sep 2025 22:53:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc08bc20967b4961359a0bbb98b26ae8d01b2183e4289c6f7b4c452ef76e1bde`  
		Last Modified: Mon, 22 Sep 2025 22:53:56 GMT  
		Size: 3.3 MB (3252489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d59a199b885aeccddd0c6e4de2dade0e3fd4aa36ab67109290203805309f68`  
		Last Modified: Mon, 22 Sep 2025 22:53:42 GMT  
		Size: 72.6 MB (72582972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f7dbb1649c3b0dcc5c9f9e3f846f29ed6284d9edede91b2d4418559f36ecf`  
		Last Modified: Mon, 22 Sep 2025 22:53:56 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:b529cf1ac4bdd75b11775149d1b19f8d3ab324f05fd1032c6e21b36dcc5d9bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da9139d246f0a2821f5f00cf6cfdadfb027775f10fb3883ac921ed252b323b9`

```dockerfile
```

-	Layers:
	-	`sha256:e71eb61badd06a1bbf71decbaab4793d1ea1920af3a2da28cbe3889a4b1caac1`  
		Last Modified: Tue, 23 Sep 2025 01:51:08 GMT  
		Size: 39.6 KB (39638 bytes)  
		MIME: application/vnd.in-toto+json
