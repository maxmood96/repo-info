## `redmine:6-alpine`

```console
$ docker pull redmine@sha256:cc3a0ab7a8fa43fc8fce27768ae40348c110b399816f1ca7a13f95e0b940510f
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

### `redmine:6-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:c80cb377af9d534bb4a4bcddd5e722d16bda21146ec43332761eda7abd353e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196264575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddd7221f7b4b24f03edf4c5a36045820e4282768c884200c684fdeeb23fca9c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
# Mon, 08 Sep 2025 20:04:45 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV RAILS_ENV=production
# Mon, 08 Sep 2025 20:04:45 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Sep 2025 20:04:45 GMT
ENV HOME=/home/redmine
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_VERSION=6.0.6
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Mon, 08 Sep 2025 20:04:45 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Sep 2025 20:04:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:45 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Sep 2025 20:04:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384b7de5c8f2fb3d8c37d62c25fa66614128499fdef0eae1f9ce06fc7bf85af2`  
		Last Modified: Thu, 24 Jul 2025 18:29:47 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d2cc9f9b4b0dcf7965bcdfd11f0a0d10cb7109cd005052729953b2b4fe12c`  
		Last Modified: Thu, 24 Jul 2025 18:29:55 GMT  
		Size: 35.6 MB (35639389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccc537e8a51e033b821956a72dca3eecbe12f50e8a15843d1423cb39522b30a`  
		Last Modified: Thu, 24 Jul 2025 18:29:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfeac1a1213bd0c1715c19edabbd869edd3390bafbe83945e01b2da69b9eef91`  
		Last Modified: Mon, 08 Sep 2025 22:51:15 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d73046a1eae90eb916d19e64dfdb52d7e7c60e7d6adb56e365bd3b587fa9e4d`  
		Last Modified: Mon, 08 Sep 2025 22:51:20 GMT  
		Size: 75.4 MB (75389000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb0688a0fe9d590e3702add99816e09a7453200d5a1d7112461dcec22d3a7f6`  
		Last Modified: Mon, 08 Sep 2025 22:51:15 GMT  
		Size: 965.9 KB (965876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4a5843bdabe94929a0237fbcbaed81433c0816c579358819be20b93a5ab392`  
		Last Modified: Mon, 08 Sep 2025 22:51:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaffe94540c86f82ed672b8a10a3a268151ad7658a92c772fc87981cd2fa0c2`  
		Last Modified: Mon, 08 Sep 2025 22:51:15 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf7414d1cc869326d549a3171567f13dabf0c4789f693fa0791f852e64c2c02`  
		Last Modified: Mon, 08 Sep 2025 22:51:16 GMT  
		Size: 4.1 MB (4067250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd5dc854ce030eb67a43b05bb3569a48fa85c4a29d7666665202c60b2429fa3`  
		Last Modified: Mon, 08 Sep 2025 22:51:19 GMT  
		Size: 76.4 MB (76399524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccf1c77f0b719eb967e5bc6c550215bba9fe9031f11992574b5c6db9142ad7b`  
		Last Modified: Mon, 08 Sep 2025 22:51:16 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:dd3a1169e2fbf2b1ad5fbeb15c4c1cb2987fa814f2c173653ba3e9a38ba8f482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefd742cab812b14d297a186400bbc383ccdd57f95f5b4c2cc85d996ad1bc67f`

```dockerfile
```

-	Layers:
	-	`sha256:411702645ab0956246fcfb9616f3006dcb022a3cd6b974c65c3a45acb698f3c2`  
		Last Modified: Mon, 08 Sep 2025 22:50:49 GMT  
		Size: 38.0 KB (38010 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:2d8b7d2177a5c84797b18d7dbad034d6b13c9960e631c21c32b051afee3077f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187979033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faef586ebfbb133d74352e6bad9ce2a3cfe47a1652d7980fdcaa4e58829ba7dd`
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
# Mon, 08 Sep 2025 20:04:45 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV RAILS_ENV=production
# Mon, 08 Sep 2025 20:04:45 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Sep 2025 20:04:45 GMT
ENV HOME=/home/redmine
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_VERSION=6.0.6
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Mon, 08 Sep 2025 20:04:45 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Sep 2025 20:04:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:45 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Sep 2025 20:04:45 GMT
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
	-	`sha256:5b38d9d8d44a070b0b5353626978e39c0285fa93b77902bb3966372f703c3713`  
		Last Modified: Tue, 09 Sep 2025 02:54:15 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de16394f1ddd9a5e7e276c3a733a465f7ffe7c92b883b4bf3454aa4e7ab68aee`  
		Last Modified: Tue, 09 Sep 2025 03:14:36 GMT  
		Size: 72.1 MB (72148226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483ae8cc784ee6439381531d40dce532349271385a9d03ae73675f467793a3f4`  
		Last Modified: Tue, 09 Sep 2025 02:54:19 GMT  
		Size: 933.8 KB (933827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1339b07483df79b07c153b72fb274dcbb6797c6dea25ee907893b3171ffe98`  
		Last Modified: Tue, 09 Sep 2025 02:54:24 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3fbb420230ca2917af82a31fa610792fbfbea8e5d886db6b974126b0fb0e33`  
		Last Modified: Tue, 09 Sep 2025 02:54:27 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365311e69d8494f12c005afb1959a4b05593167919fe5f451c86fc264013fcd1`  
		Last Modified: Tue, 09 Sep 2025 03:14:29 GMT  
		Size: 4.1 MB (4067239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b804bc61d5dbb505d4d0f1fc4a20893720e68be66d4f37b02ae3f3feae7f6856`  
		Last Modified: Tue, 09 Sep 2025 04:51:54 GMT  
		Size: 75.2 MB (75224707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f30f960ae9cbbd403d8555f00e4f81401d6162a2357ffa485c175dc790814a`  
		Last Modified: Tue, 09 Sep 2025 02:54:30 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:6ecae1a2be8fd5cf4895ce28a7332e24da799c2db7fcd841a43b18efca404976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b56233275b89043ac884fef83aa566a6cfc068ca05b808ae6ffdf51fc8cad8d`

```dockerfile
```

-	Layers:
	-	`sha256:783eafe6efe8ab397a80078518443a6acd46389ba8b0c387aab6c1c31fe442a3`  
		Last Modified: Tue, 09 Sep 2025 04:51:03 GMT  
		Size: 38.2 KB (38186 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:ce90801372502e94ded5f78ef7e1645e8289c02e973af3f3512489a615c05fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183226476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9e71b2eec0fc5d8c9103feba67ce9bae25eac3e3b765fc5c6956769fea4391`
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
# Mon, 08 Sep 2025 20:04:45 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV RAILS_ENV=production
# Mon, 08 Sep 2025 20:04:45 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Sep 2025 20:04:45 GMT
ENV HOME=/home/redmine
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_VERSION=6.0.6
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Mon, 08 Sep 2025 20:04:45 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Sep 2025 20:04:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:45 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Sep 2025 20:04:45 GMT
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
	-	`sha256:89567894422ddabe1f2b89a715d24194e7fd03b7dcf01f75a06323612b4f0822`  
		Last Modified: Tue, 09 Sep 2025 04:35:14 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78447e63af37bf32d58c067be43669be393eb96f3fbd21d322039c345543cc2f`  
		Last Modified: Tue, 09 Sep 2025 04:49:34 GMT  
		Size: 68.9 MB (68938106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4dd6553d15aa21f98735a99347166e33025a63f4e7c1dcd80fe21c7499f312`  
		Last Modified: Tue, 09 Sep 2025 04:35:14 GMT  
		Size: 933.8 KB (933786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc7a7d5ecd4fbd8c720f598d0e3373a88d72c219f1be3aa961d7f6a52a49a87`  
		Last Modified: Tue, 09 Sep 2025 04:35:14 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3affb5726e02d1f3d00d60fed84606f9e183fc5f64561d51280ccf6dd8d33e04`  
		Last Modified: Tue, 09 Sep 2025 04:35:14 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc6b839835cb3189b5e34a334f56b6b10d071df737179bd921030613607e892`  
		Last Modified: Tue, 09 Sep 2025 04:49:26 GMT  
		Size: 4.1 MB (4067227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0bfd81ea6dad45c61bbd0df890e2489ebd3d775a80c9d6974a5ac7bdadf876`  
		Last Modified: Tue, 09 Sep 2025 04:49:25 GMT  
		Size: 74.1 MB (74102170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935d38496bb8c7b4e153f451623f70969a8009b0413c08e9f205b4ab9397cd10`  
		Last Modified: Tue, 09 Sep 2025 04:35:14 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:851d6d2da841b12716fb775db1a67d5909aea11ccbde33a4d67a74b9d23718b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59578f1e12ad7f9fe41375e942c0c24168e8269e8d43ebf70bffd6907e4d3d99`

```dockerfile
```

-	Layers:
	-	`sha256:2aacce775af1d3c43cfc8c17b6a0a8535c56f685d086bdef45e3a55395aa2987`  
		Last Modified: Tue, 09 Sep 2025 04:51:06 GMT  
		Size: 38.2 KB (38187 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:54efab6510a7f3955a83db3333726603086c07bd5fe429c5ddfd70fe12c27182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196401539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f6dd6389c95943dc4e136dca27ced39d0745fcda0d2f9d3fa6d0f56afb4e5b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
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
# Mon, 08 Sep 2025 20:04:45 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV RAILS_ENV=production
# Mon, 08 Sep 2025 20:04:45 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Sep 2025 20:04:45 GMT
ENV HOME=/home/redmine
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_VERSION=6.0.6
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Mon, 08 Sep 2025 20:04:45 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Sep 2025 20:04:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:45 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Sep 2025 20:04:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c09257109ac898fca88b26ba8b5083a10c26c1561d2fdfa48f428f3c19c121`  
		Last Modified: Thu, 24 Jul 2025 19:12:09 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f101a1cb65b95a0ef2947118cfcb4f5b4f57d43a52fdbdec65dfc5ac77c5ac`  
		Last Modified: Thu, 24 Jul 2025 19:12:12 GMT  
		Size: 35.6 MB (35566308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13799c5ed6b81b70be277ee62a00784098d8d512d76b7c554fd881010e1f54d2`  
		Last Modified: Thu, 24 Jul 2025 19:12:09 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296b0d1faa310122d468dc933235e58cc3e646c726bda29b5151dcb21b25f969`  
		Last Modified: Tue, 09 Sep 2025 02:28:12 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a8a447fb9aeb9bdb965b7e2cb1daba7faadbb7b3d66fa526b6822b28e2c7d9`  
		Last Modified: Tue, 09 Sep 2025 04:51:49 GMT  
		Size: 75.0 MB (75010412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d57d3b96938dd3e51f2ecbf3f8ad8810349b31a2ce0bb241fd2c756105deb58`  
		Last Modified: Tue, 09 Sep 2025 02:28:13 GMT  
		Size: 921.6 KB (921627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b23992d8570e2a9d3555684a8836bf614c03f64a72c03c43881e92f8003fcc6`  
		Last Modified: Tue, 09 Sep 2025 02:28:13 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e77447f6ec5a182552defb118ad76453096dd884b0dd686074fb84d6e139823`  
		Last Modified: Tue, 09 Sep 2025 02:28:11 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f3a95d84bc61ea6cb8c6bf9839f98492eea831a8328f2dbe18f86e8c1c96bc`  
		Last Modified: Tue, 09 Sep 2025 04:51:45 GMT  
		Size: 4.1 MB (4067232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f874e7d529cd5165a74b5d5ffc8d85705dcd188517eddb527df4d220ba2c5f`  
		Last Modified: Tue, 09 Sep 2025 04:51:48 GMT  
		Size: 76.7 MB (76701360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad326b053f3d613aa4d42e9733c948e71fd351d11214c828640195b4be35ec39`  
		Last Modified: Tue, 09 Sep 2025 02:28:12 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:1ebd6075b781c37b97d4944c2caa1e55a9d4e22673d4e9182136ad8d9b64c854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf73626203074c032715fc946dafa182f5f64c64fd53a14f2b5d987c56e165d2`

```dockerfile
```

-	Layers:
	-	`sha256:d8480d89f84e02990906821caf319beb7826631987746c0ee4ce9aed285e895d`  
		Last Modified: Tue, 09 Sep 2025 04:51:10 GMT  
		Size: 38.2 KB (38237 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; 386

```console
$ docker pull redmine@sha256:2b8af89de405942e8d4d10a7df59895eefc02d2694e600b047424eff0adcda42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193002911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8605c53986bba51008bfef022209674d3742a813ee46e0c9c975b67d5382d312`
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
# Mon, 08 Sep 2025 20:04:45 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV RAILS_ENV=production
# Mon, 08 Sep 2025 20:04:45 GMT
WORKDIR /usr/src/redmine
# Mon, 08 Sep 2025 20:04:45 GMT
ENV HOME=/home/redmine
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_VERSION=6.0.6
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Mon, 08 Sep 2025 20:04:45 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Mon, 08 Sep 2025 20:04:45 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 08 Sep 2025 20:04:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 08 Sep 2025 20:04:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 08 Sep 2025 20:04:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:45 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 08 Sep 2025 20:04:45 GMT
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
	-	`sha256:5b386176e89666f54377802a80056799ba2c52118321a87d9fbc76e8dd306e50`  
		Last Modified: Mon, 08 Sep 2025 22:29:48 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f43c2b023eeeb5b30338db7b61cc04df5f86f0c71e25901d5946eb01692b71`  
		Last Modified: Mon, 08 Sep 2025 22:51:22 GMT  
		Size: 76.1 MB (76120075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00b4db62f05d57488a70692bc60f49138ba1fc4561bc9af0e7ed124c4a28f40`  
		Last Modified: Mon, 08 Sep 2025 22:29:52 GMT  
		Size: 938.1 KB (938132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7260bf5e6d95c340ae1985be3b64a68f6686aef0c4418a7c3821ef83f82230ce`  
		Last Modified: Mon, 08 Sep 2025 22:29:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8889d0f199727ceee4819e0b128260e6a6569599f23e017bcf325adc564f7137`  
		Last Modified: Mon, 08 Sep 2025 22:29:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da864150f971ed9aa1b977bf560a00866e5684ca2f14484872a812079a7ffa2`  
		Last Modified: Mon, 08 Sep 2025 22:51:16 GMT  
		Size: 4.1 MB (4067284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec499ff904d13c61f6212248d19e079fe2c45387018c63de515793605f6f7cd7`  
		Last Modified: Mon, 08 Sep 2025 22:51:21 GMT  
		Size: 76.3 MB (76280290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c652b2ab6cc8216b49d99ac5a17a1e895caa8338112b933a2278444384da326`  
		Last Modified: Mon, 08 Sep 2025 22:30:05 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:7701e161b60c613a72fdae62f386d1ec3791a191d97c2e0f4d9ed648c38dd973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878f084de034c5d6ff50773a5867e0e3f1b6bbb56432797709710db5c461b291`

```dockerfile
```

-	Layers:
	-	`sha256:7a8228e61aed228b4a18580e777f800377f5b9d796740b806a3a32d4fbcde03f`  
		Last Modified: Mon, 08 Sep 2025 22:50:59 GMT  
		Size: 37.9 KB (37948 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:afd1479224d731c73650506903f3a39bca396e85df013efa9f1f76946ae0c5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197959819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4794b5413a05d5780cce3e48fe2f82ccb3c6ec084544c991da27b83935342904`
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
# Tue, 19 Aug 2025 06:37:23 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV GOSU_VERSION=1.17
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV RAILS_ENV=production
# Tue, 19 Aug 2025 06:37:23 GMT
WORKDIR /usr/src/redmine
# Tue, 19 Aug 2025 06:37:23 GMT
ENV HOME=/home/redmine
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV REDMINE_VERSION=6.0.6
# Tue, 19 Aug 2025 06:37:23 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Tue, 19 Aug 2025 06:37:23 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Tue, 19 Aug 2025 06:37:23 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 19 Aug 2025 06:37:23 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 06:37:23 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 19 Aug 2025 06:37:23 GMT
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
	-	`sha256:2b0446d9f510c3f80e3b8bf3ee7e66ec52353304b6ad527fd36a71154e658249`  
		Last Modified: Tue, 19 Aug 2025 17:21:03 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505c7b8d30ef29a2ff16081db7bea3cbd8178a0d0ecaa9ffb9cd0e45e5f1677`  
		Last Modified: Tue, 19 Aug 2025 17:21:21 GMT  
		Size: 77.5 MB (77458993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437247382240c1737626fb4c08344f8ca846a3300599276863a83a192567914c`  
		Last Modified: Tue, 19 Aug 2025 17:21:04 GMT  
		Size: 1.1 MB (1087121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9de93a574482f903946ac010bb8616e43a2922ef0f963a5eb78d2605e7620e`  
		Last Modified: Tue, 19 Aug 2025 17:21:04 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a1ae5e929c7471fa50b0623d676e50afd01f4ce1d97041d96af89976f2fe59`  
		Last Modified: Tue, 19 Aug 2025 17:21:04 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b26458f533ca936314ee32dc983ecc47b2c5b3cc1c94f447a005a6301ac0af6`  
		Last Modified: Tue, 19 Aug 2025 17:21:04 GMT  
		Size: 4.1 MB (4067226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf58b0a4cd8ac5a3d424e8044bfd9fedd5a5652dfd5ff38ae339eab23f56b31`  
		Last Modified: Tue, 19 Aug 2025 17:21:12 GMT  
		Size: 78.1 MB (78132275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831a95dad5e18ebf493a650f195ff4d6531eae07ee703cdf93b957acea12fe6`  
		Last Modified: Tue, 19 Aug 2025 17:21:04 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:50f4cf46c4b172ac372ca8c87e74be58d7ca7fc4b15f5256fe2549042dcbeb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b327c8cd37731d68404a827e5f06767354c259dd9a82b222d8d4d82322f2600`

```dockerfile
```

-	Layers:
	-	`sha256:f40f7d4dfc2e6007cdbaa60dc65c14f768071d2e56dcbd792a86d88829d1759a`  
		Last Modified: Tue, 19 Aug 2025 19:52:39 GMT  
		Size: 38.1 KB (38094 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:2cbf0f69f5b1922ccb2c07507b46a700f75ea1cafe06b91ccd1a35a4dbef4c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192281819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d58fbe7409c950f90207eeb8b6c8f54cfc5c32d45b505ba054777742234330`
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
# Tue, 19 Aug 2025 06:37:23 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV GOSU_VERSION=1.17
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV RAILS_ENV=production
# Tue, 19 Aug 2025 06:37:23 GMT
WORKDIR /usr/src/redmine
# Tue, 19 Aug 2025 06:37:23 GMT
ENV HOME=/home/redmine
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV REDMINE_VERSION=6.0.6
# Tue, 19 Aug 2025 06:37:23 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Tue, 19 Aug 2025 06:37:23 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Tue, 19 Aug 2025 06:37:23 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 19 Aug 2025 06:37:23 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 06:37:23 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 19 Aug 2025 06:37:23 GMT
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
	-	`sha256:4c5d411d539656ab7d6d4f6dc493071dc9659b8461bf83a2c91933674a672c3e`  
		Last Modified: Fri, 22 Aug 2025 13:06:52 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc78beccba1525eadb5d73eeeae8cf9c4495667967b4ba52219d18a02c97463c`  
		Last Modified: Fri, 22 Aug 2025 13:50:17 GMT  
		Size: 72.3 MB (72274637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb63016e256324b2205d751314fa307ec5b103623bfaa5b7931582554c7724f`  
		Last Modified: Fri, 22 Aug 2025 13:06:53 GMT  
		Size: 1.1 MB (1136857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ab2971079b88b1ff539dbb76d0de1832038fcbe232c1bdb0f4e022d4fca956`  
		Last Modified: Fri, 22 Aug 2025 13:06:52 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ed8757a563d34a833b09497af770dabd27632b098b58fd48f116ef42cb59b0`  
		Last Modified: Fri, 22 Aug 2025 13:06:52 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2206074f0621e105dd9ad681d62ba5b75936a7329785cd2bef43d3d8a71b7af`  
		Last Modified: Fri, 22 Aug 2025 13:11:28 GMT  
		Size: 4.1 MB (4067368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb662b803f2df6e6899696f838d2b8ab4ab1ab32cc6f71491b27cc7e9c5bd16`  
		Last Modified: Fri, 22 Aug 2025 13:50:15 GMT  
		Size: 79.5 MB (79515145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b8ba9b89c8fa6695935e5893dd7b91b23390ce0b30f906e6ad9fae972e9ae6`  
		Last Modified: Fri, 22 Aug 2025 13:06:51 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:7e76c331696ef6491005005d995449e5a86c1f04690935bfd19916b346f2f285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922b08e160429f188392732ac216f839d2d0daa11dd098782b00d584cc597e45`

```dockerfile
```

-	Layers:
	-	`sha256:0b8629ac1ca1b29d93009cf4d7738cf1338ed892217060028c07021aa5c01096`  
		Last Modified: Fri, 22 Aug 2025 13:49:56 GMT  
		Size: 38.1 KB (38094 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:e3591402f7fb75caa3bbef18b21b3bbcc5f9b8fe32e45477f7054cc860a7d0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193950233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b5f70c3682a9b663f8ffa0dd2430821a552794e52d89ff066d99237e2affc1`
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
# Tue, 19 Aug 2025 06:37:23 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV GOSU_VERSION=1.17
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV RAILS_ENV=production
# Tue, 19 Aug 2025 06:37:23 GMT
WORKDIR /usr/src/redmine
# Tue, 19 Aug 2025 06:37:23 GMT
ENV HOME=/home/redmine
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV REDMINE_VERSION=6.0.6
# Tue, 19 Aug 2025 06:37:23 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Tue, 19 Aug 2025 06:37:23 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Tue, 19 Aug 2025 06:37:23 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 19 Aug 2025 06:37:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 19 Aug 2025 06:37:23 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 06:37:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Aug 2025 06:37:23 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 19 Aug 2025 06:37:23 GMT
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
	-	`sha256:6c2741239b1e50db2c0850b4f2cb46fa16952b103da74127bcbb01fbd2fec7f6`  
		Last Modified: Tue, 19 Aug 2025 17:16:10 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16df1fa81210ee4a46dae4add67f8a964e544afa35916a6bd2ee3988b8f42b2d`  
		Last Modified: Tue, 19 Aug 2025 17:16:18 GMT  
		Size: 74.4 MB (74366647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1649a373d413b23c5610cb12b88a45e2bb1e4766b8efc7880c68b3195b15c22f`  
		Last Modified: Tue, 19 Aug 2025 17:16:10 GMT  
		Size: 1.1 MB (1131837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737910c6c1d49fe28780d683cfa97e0882578445aae0d156003b3c9391f5044c`  
		Last Modified: Tue, 19 Aug 2025 17:16:10 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9e3b65b89186e0992a510d7cf958abe1231c85ea33e7ba541acd0b84fa9b2`  
		Last Modified: Tue, 19 Aug 2025 17:16:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac1ca0989eb74618a37ec1e5c4591d10aae57658aca5e9fdac287c6d6c86a30`  
		Last Modified: Tue, 19 Aug 2025 17:16:11 GMT  
		Size: 4.1 MB (4067217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d4a8d55bc7bbcf2ee944b6e0ccd3e7ffa8cd63a7866fc92ff99e4e94cadc39`  
		Last Modified: Tue, 19 Aug 2025 17:16:23 GMT  
		Size: 77.5 MB (77465389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba17909baf3c91727de936399b3947ebe9d03a73271023c1252c82e94025ae0c`  
		Last Modified: Tue, 19 Aug 2025 17:16:11 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:c41f6d78358431a62eb87a6dd96e7934daad3d2dd999661590d0bfcb2450f1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f130ffbd1666f905c7f90fc48f10e64872a90f68b2007de8777e263620db9e`

```dockerfile
```

-	Layers:
	-	`sha256:6feb952345234dbad53d196d6ebe52955a4181f3f42f5d1c3fd11c2700cd1aa7`  
		Last Modified: Tue, 19 Aug 2025 19:52:45 GMT  
		Size: 38.0 KB (38016 bytes)  
		MIME: application/vnd.in-toto+json
