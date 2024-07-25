## `redmine:5-alpine`

```console
$ docker pull redmine@sha256:9bc84861354a7a33b7c5be07d2381b1beb6593bbb42302bd1c91a8d60f07bf01
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

### `redmine:5-alpine` - linux; amd64

```console
$ docker pull redmine@sha256:b6c6d27f99bf5a96fef68e8032cc491e91790d4c6544e90e18d7b10b3b3f4a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186678141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abc2ee6460828066b5d948997826e39a73fe592fdcb7059c703b9af4da3e677`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["irb"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588a5e7d3c16ac9bf230ac4f89ed437ab1bc231e179af1fbe155ac7461910ab`  
		Last Modified: Mon, 22 Jul 2024 23:07:25 GMT  
		Size: 6.7 MB (6684065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1f183cd43b2e89e830b2978c43e87a235076c98b97a8547ff0b4ece8ddd5ed`  
		Last Modified: Mon, 22 Jul 2024 23:07:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f821ce720af011c0a4807872b134941e5758bf63708cc2d1ad0f82df89081cd0`  
		Last Modified: Mon, 22 Jul 2024 23:07:45 GMT  
		Size: 32.1 MB (32104726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6243234203bf3c086d33434bc0c7f983352cf72b78d08c1fe6f1d7eadc5d41dc`  
		Last Modified: Mon, 22 Jul 2024 23:07:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae84d89b3871f1afbba540683fe06e8515723eb43446f488422fd336bbc7ca6`  
		Last Modified: Tue, 23 Jul 2024 00:10:57 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170b27fa94248eca087593208a59f827423282645e2916d2f7e7b4375de085c6`  
		Last Modified: Tue, 23 Jul 2024 00:10:59 GMT  
		Size: 69.0 MB (69049981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d207dccdaf3430424e94bea62e709ef727f16a93b0e6ef55c5c3ba7330f8e3`  
		Last Modified: Tue, 23 Jul 2024 00:10:57 GMT  
		Size: 1.2 MB (1195630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a198e7e9abd6aceb2693b8c206d6745fa7a3ca58640016fd4ee37ae1d8d39384`  
		Last Modified: Tue, 23 Jul 2024 00:10:57 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cf4f2d9ccb15bab406322392a60ee68d67dab81c6f6d8f905eef20264d82e3`  
		Last Modified: Tue, 23 Jul 2024 00:10:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e467429660db181d341b5b53dec831bdafae70a4a2d18ec5773bbad05f2e04a1`  
		Last Modified: Tue, 23 Jul 2024 00:10:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3d7cb87d728d7e7da20ba1c0fe5d8e5c9b08be9148a07d39af3b8ba016d453`  
		Last Modified: Tue, 23 Jul 2024 00:10:58 GMT  
		Size: 3.2 MB (3244084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353b0c352ca25f22a6660333dcac7920e0464409af1370068503f405d999dfd8`  
		Last Modified: Tue, 23 Jul 2024 00:10:59 GMT  
		Size: 70.8 MB (70773060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0b3de8820cd5a0aac0af22ebe17c56916ec63869ea938ad277a053a02b340f`  
		Last Modified: Tue, 23 Jul 2024 00:10:58 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:af1ef13c06dc59409facccb26ea0563de15a7570551916ab5f756bda964eebde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933f74f064feb853c37a78992d78aa4c8f82d89197eb40b6f484a30d61f8dbfc`

```dockerfile
```

-	Layers:
	-	`sha256:8e70a2ebe96d23494bc8404358fafff52b80f55f9354179b0845a958fb141116`  
		Last Modified: Tue, 23 Jul 2024 00:10:57 GMT  
		Size: 43.4 KB (43395 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:460d4e20650fad69bb92aae0a8b52637f879c00758b28b0145ff11b2abd1c371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178542936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa50634b5b8e65a18471ba7790312513adac9d1827310dd5766d8f09035b7d80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["irb"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74719713a7016efb7fdc63183937d47b6d650a97cffb2e1ed7542e6fb958c3f`  
		Last Modified: Tue, 23 Jul 2024 11:28:40 GMT  
		Size: 6.5 MB (6531387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79209c4b64b5e0afa4365889a46c51fa5e6b4558024ed1c8e748038406253be9`  
		Last Modified: Tue, 23 Jul 2024 11:28:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42364cf3a652d1d21ad457915ee8bdc1daff879958a572946089c3b3dafdf012`  
		Last Modified: Tue, 23 Jul 2024 11:40:51 GMT  
		Size: 28.2 MB (28244032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bc0bfbe17f592aa8d0b25f310bcc267c75b971c688170150a499a32f7868ac`  
		Last Modified: Tue, 23 Jul 2024 11:40:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c2317aa9fccb9c0fcabdc00363d4820b1063dc47b7b34a58047070dd31f1e`  
		Last Modified: Tue, 23 Jul 2024 13:17:05 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40496d19500ddfd9403656e3433d4ee40350c3c2e1204d49ca8d152fd141fcc6`  
		Last Modified: Tue, 23 Jul 2024 13:17:07 GMT  
		Size: 65.9 MB (65873464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf67d3b6e923004acc009d8c2009abd1c75369cf425a60e595ff76e583cb38b`  
		Last Modified: Tue, 23 Jul 2024 13:17:05 GMT  
		Size: 1.2 MB (1162316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d9b316b7142dee6da78529d77ead927944e1597cff120be158cffc2a03086c`  
		Last Modified: Tue, 23 Jul 2024 13:17:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22c399b6d06f3c16d4e90991fc0432d51938cb73fdeda8200f82de483aa3802`  
		Last Modified: Tue, 23 Jul 2024 13:17:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1d6912d294112046211a30a2b40f7146764c811d5cfe1e02c113fcf21112d`  
		Last Modified: Tue, 23 Jul 2024 13:17:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6038b7d84e4282963bc563c4e970b01c9950d6c3464f5a2828429ce585ee53`  
		Last Modified: Tue, 23 Jul 2024 13:17:07 GMT  
		Size: 3.2 MB (3244063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1237b0ee46da03a2c130176159f727b4ceb2dea3e7d08f051f4d1830aacbe26`  
		Last Modified: Tue, 23 Jul 2024 13:17:09 GMT  
		Size: 70.1 MB (70118779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28074f4c8070e5bdcdd21d8d6f46f8757353f22a8ec6e8f9045e9811b1b98cde`  
		Last Modified: Tue, 23 Jul 2024 13:17:07 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:5c192ece04619d609b74c62374f1bf70c75007ed31e436f00905ccd72c25170d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb65ba69e36095f966232e7f61d85a72abdd4c091b6fcab6fc52f42666b03741`

```dockerfile
```

-	Layers:
	-	`sha256:2897aff67168a68fb247b58217132b7dbb7d5961802d0cd7827c54135be2cb91`  
		Last Modified: Tue, 23 Jul 2024 13:17:04 GMT  
		Size: 43.6 KB (43641 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:d1bafa0193738013d8a79ffc99545099bf54020b6d660abf16bb7f569d25b570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174400677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69b7acac37233ebc13860a0cfc67339003478c534ef65b400fa884eca323ab1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["irb"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3509e54445049a7962a250a257fa21917ea8425572c136dafeebee8d6e82ce`  
		Last Modified: Wed, 24 Jul 2024 13:39:21 GMT  
		Size: 6.4 MB (6375823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36c58d18afe84e95f7526f9436ac5e9bde0ef8ff682d8667f4c220e039f44d`  
		Last Modified: Wed, 24 Jul 2024 13:39:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88f542dddeb297c8c4ef5efc47f18eb1cb30c4f1fdf6744aafbda51fd2b2206`  
		Last Modified: Wed, 24 Jul 2024 14:10:46 GMT  
		Size: 28.1 MB (28118214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8db65b3a11d0a1387a50cbf901e65a2e46d345f1a21f485f2aaf0344388f731`  
		Last Modified: Wed, 24 Jul 2024 14:10:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1476c32ca36ce2d2115618b670c1deca77fe96937965265cd283d0e59f5c51`  
		Last Modified: Wed, 24 Jul 2024 19:30:53 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48baa76a72f20bf7d2286185ad8b13d03b18e7554b0ab0eb76942fa625a01905`  
		Last Modified: Wed, 24 Jul 2024 19:30:56 GMT  
		Size: 63.3 MB (63297671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4e4861deeaf145bb699fe2837e49573f3ccd7e047f43458d5e6950f54b3c85`  
		Last Modified: Wed, 24 Jul 2024 19:30:54 GMT  
		Size: 1.2 MB (1162363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3720ac54df9763546b1acfd275d01583b73f1061e832a8c61a54aa03c0bead64`  
		Last Modified: Wed, 24 Jul 2024 19:30:53 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c1b8d605c83662d0224e694689287532f97096340d91180ce62bbcc23a5618`  
		Last Modified: Wed, 24 Jul 2024 19:30:54 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ab3e22f9752f79c9c258983a1948d8dd504d8f6b460e38ca855473c3dfecf0`  
		Last Modified: Wed, 24 Jul 2024 19:30:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf40ce69c409d95fca575a74becdd3497dbcdadacbbcef85ef74eff8db85fa`  
		Last Modified: Wed, 24 Jul 2024 19:30:56 GMT  
		Size: 3.2 MB (3244047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ded621a693f37fa7e279bbe9e95ee091f7d67003a28ec72b7031b3ddf0d3ad1`  
		Last Modified: Wed, 24 Jul 2024 19:30:58 GMT  
		Size: 69.1 MB (69103890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f73e7601f6d7c030befa2aff581ffa6080f411a8f2f93d730a01ad5e9fdd72`  
		Last Modified: Wed, 24 Jul 2024 19:30:55 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:fed584bfd39063b886da5fb3f412847b71b591c00d109b39851eaf0483769c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c16e7782cbfda3429d315498b54a6d25601588cc42a384e6448922486b1ee1`

```dockerfile
```

-	Layers:
	-	`sha256:dc31e873c70f1ff536d4b7eebd6855ff88f16a30406321235e2ecf430b64337f`  
		Last Modified: Wed, 24 Jul 2024 19:30:53 GMT  
		Size: 43.6 KB (43638 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:54ca9389a267bc9f0976d08d071c30a7d131561e0d71c4c294725a0901bd4b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187778419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557ad6dd74d0fd7fd95a9b598dbc8f6bf5e1aa4b66a4e380d5c6e2a9dcace344`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["irb"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ac6f38e95a15a08cafcfb1eac4bb79d1f2f4acaced374937a71640947f6887`  
		Last Modified: Wed, 24 Jul 2024 07:30:35 GMT  
		Size: 6.8 MB (6750611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5360b8813ee58f07a2a5551b87e7773a27723cd931d213844edd09894f725c9`  
		Last Modified: Wed, 24 Jul 2024 07:30:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114ae518c0f71a25a9236a8285e1a76503415b55a40c2d06e6f7ef1eef5f061c`  
		Last Modified: Wed, 24 Jul 2024 07:59:54 GMT  
		Size: 32.2 MB (32169350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2301eef040d7d723d21c40a0570f46dfe1247efc1912dfbf76cc520d87e8fc69`  
		Last Modified: Wed, 24 Jul 2024 07:59:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df46efa70dc596cea93ddde799f021a695857d18a58eca765efdf289c659386`  
		Last Modified: Wed, 24 Jul 2024 16:08:39 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ea74fa18f502136679b050d7cdada421a2831d70269968b2e27725bee2ac6d`  
		Last Modified: Wed, 24 Jul 2024 16:08:42 GMT  
		Size: 69.5 MB (69533807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cbd878822acef78f73d53adec52edaa4b36d1a24a87beed7a77d8669a9ff32`  
		Last Modified: Wed, 24 Jul 2024 16:08:39 GMT  
		Size: 1.1 MB (1121358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f18d588afc0f5432ce89d80beefff4a5cb180d2cd60ca94fb0161a3b19d302`  
		Last Modified: Wed, 24 Jul 2024 16:08:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5a0fbb3acea4e83fa76a270544a12cc205aa8b2dbe579447223a3fa16b1510`  
		Last Modified: Wed, 24 Jul 2024 16:08:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf884cdea86d4655f0661b3cc14b7ae4a2bb5fd2ae37cd391dd443703f0e2aa`  
		Last Modified: Wed, 24 Jul 2024 16:08:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f590e78a2049e189324640bd1b89b85235597bdd55644c0306fa83fe4729331`  
		Last Modified: Wed, 24 Jul 2024 16:08:41 GMT  
		Size: 3.2 MB (3243982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0d19240ed574dd22dc06a5664c5c67b651b16bbe7876751c6ec4d6c64181b`  
		Last Modified: Wed, 24 Jul 2024 16:08:43 GMT  
		Size: 70.9 MB (70868669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0abb0494a2e8ef1e0f8829aec2e92a66fae1903040faa0d4db1b54e91ef31aa`  
		Last Modified: Wed, 24 Jul 2024 16:08:41 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:e908a318eba593f968b035296b62b778deb8bcd89ca193bdee4db0cc0ab61dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 KB (43888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee8a5d26f80c69ae4122cbbd1a740eea3dc69015210ff67ac97d8437297b790`

```dockerfile
```

-	Layers:
	-	`sha256:eddf017a4dad1a36fda322b9d3fbf69f93539cf10cb9163912e4649f1f78917c`  
		Last Modified: Wed, 24 Jul 2024 16:08:39 GMT  
		Size: 43.9 KB (43888 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; 386

```console
$ docker pull redmine@sha256:d165c3f88866fc6680208caae951e8c5d238d51f7dd370e4437189b0aa59ad09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183271079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723bdc77ea32cd4822542cd0b8b5350191bd5cb16d19eef43f534e9b18dc3365`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["irb"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd5cda8dd6d0d6ca9f9abdfa88c357b46498c24f90d7edd982042adf2961ed6`  
		Last Modified: Mon, 22 Jul 2024 22:11:13 GMT  
		Size: 6.7 MB (6749330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d695373f2c9d78cb9feca90de9d1384bad5409c6a610adff46fe2034eec565`  
		Last Modified: Mon, 22 Jul 2024 22:11:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67227c717fe5c6344a256acfcd587d919b9fe84ff488e5108afe35e060a3067c`  
		Last Modified: Mon, 22 Jul 2024 22:11:13 GMT  
		Size: 28.1 MB (28099039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5dff6a579024e44417117b78a616e219c7f324aa22809c7e46a8acaca0d138`  
		Last Modified: Mon, 22 Jul 2024 22:11:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3962b280d544149125b0dca7a1b2c565fbc2bba0682b184b88a39e602b9e5862`  
		Last Modified: Mon, 22 Jul 2024 23:11:31 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739f06f2cb6c42e1f3682daff84b37c3a0d6d806384b722f335a2b7953576d1`  
		Last Modified: Mon, 22 Jul 2024 23:11:34 GMT  
		Size: 69.6 MB (69619855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa66a1d99263e5ddd4eb51da4d9605149ecdcfb6c73e23110f3f762562d29447`  
		Last Modified: Mon, 22 Jul 2024 23:11:31 GMT  
		Size: 1.2 MB (1170727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95df33b1f427faff6e7f69f52811f6e87372df04fa14e2a77e5b794b87254d39`  
		Last Modified: Mon, 22 Jul 2024 23:11:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4248167bdcf356dc1d03a5b1a88023dfc90614d985c4556845c29448fbfe80`  
		Last Modified: Mon, 22 Jul 2024 23:11:32 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ae1d7e28a67c28b1fae21f515d7db349043e0f39b7e53b54e236ec6a49c82c`  
		Last Modified: Mon, 22 Jul 2024 23:11:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1854fec43de091b1dfd59e934176b2df5b7cc089aac59bf6c089b99af6ebd449`  
		Last Modified: Mon, 22 Jul 2024 23:11:33 GMT  
		Size: 3.2 MB (3244053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8bbf4cdadb2360290988a5557acecf030b0eeffab3e38f0f9adf2c68472ced`  
		Last Modified: Mon, 22 Jul 2024 23:11:36 GMT  
		Size: 70.9 MB (70916303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e74f7c45c3938e425dbaf1dc6ea8646c19ce8addf6b18c3e29938cb5040880`  
		Last Modified: Mon, 22 Jul 2024 23:11:16 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:2004c72e9e5558aec40c40cc7346f19ba9cbd4ccc429d7da828aca65b332a0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 KB (43331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14acbbfa1bd5bf528a8c842a67e0a085ba6811847e1b6b6932e013d8bae19277`

```dockerfile
```

-	Layers:
	-	`sha256:0f26ed3676e5351f0945314d9c53cfbb6083920cb33e6c42c59d40e851999998`  
		Last Modified: Mon, 22 Jul 2024 23:11:31 GMT  
		Size: 43.3 KB (43331 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:fa267d244ab5b3ef8741afe7cf7d3e13e6dfb8b5cc3b299849ccc88f7c478912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189865508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c08000fb3d0701c396f255fd6ec93dc48356a0ed6771063310793912fe314ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["irb"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61cd6291894b95f52f0b001d66e3a69d75a15b3b303a4da7d7910741b946209`  
		Last Modified: Tue, 09 Jul 2024 19:20:49 GMT  
		Size: 6.9 MB (6911703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85adda175aa350d4c5a350928142664e4b9f0905956b472c82f922bfbbf5bdc5`  
		Last Modified: Tue, 09 Jul 2024 19:20:48 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bcfbf2547240588d7b271633db436f7f5e2640fef6a88f06b4eaa51b021b5f`  
		Last Modified: Tue, 09 Jul 2024 19:57:47 GMT  
		Size: 31.7 MB (31681404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b098ff54d22667ded7222d8030f57aae85bedc66c76ed4c8dcbad07998c8514e`  
		Last Modified: Tue, 09 Jul 2024 19:57:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbcdbb00965540fbb66cf820668c10038dfd96b08b028cf853ffbb9e3cf1fb4`  
		Last Modified: Tue, 09 Jul 2024 23:33:14 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c857f5d4134d4129d0995a0ad78e2bbe582680591a2b7c34796138f05abca2`  
		Last Modified: Tue, 09 Jul 2024 23:33:16 GMT  
		Size: 70.6 MB (70627254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071e6663152691adfcdf0f84a5bce255677112af39a48bd3c219d74ae971ba78`  
		Last Modified: Tue, 09 Jul 2024 23:33:14 GMT  
		Size: 1.1 MB (1111966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ab8ddb195c78ddc08ad1f24cc88c751b77c1cf5fb9c284a441c529b19955d9`  
		Last Modified: Tue, 09 Jul 2024 23:33:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603b2d85e54f354cf349d6e5be270015c0a810c00be6d4947140325f2117fdf8`  
		Last Modified: Tue, 09 Jul 2024 23:33:15 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0256437895125afe20e798580ce1e584671964f54b72a5130be7f2f6930fead9`  
		Last Modified: Tue, 09 Jul 2024 23:33:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176add2ce06c115ae626cff1a327aae10d2b484f5db511424f3356e5d08b6e8a`  
		Last Modified: Tue, 09 Jul 2024 23:33:16 GMT  
		Size: 3.2 MB (3244057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e965f453e089318feeeae9a893f3450819e35dc1e3617615971ee41818157063`  
		Last Modified: Tue, 09 Jul 2024 23:33:18 GMT  
		Size: 72.7 MB (72713716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b790d8eb9e535b5bfda0ab2ac8750fde0e76fc30d4b213f7c6938aabfe734d3`  
		Last Modified: Tue, 09 Jul 2024 23:33:16 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:edb0b361fd2f24fd0aee25fe1a2d75912b994f598d8a7d9bc1bd5e4bf031b427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 KB (43535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac259774ee6fa235b614d1782c2ab5b919a1303b6960432f0f6c186b29b68e1b`

```dockerfile
```

-	Layers:
	-	`sha256:8b92d9ddd3ed4ede44d7d0d181c673bc1d79818b066e7efe341df8e8e0037621`  
		Last Modified: Tue, 09 Jul 2024 23:33:14 GMT  
		Size: 43.5 KB (43535 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; riscv64

```console
$ docker pull redmine@sha256:301610a64a95da67731ef330ff8cab548dc3d745bba3d7728eab5809df8eb681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185617273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3487efb85993e0760f9281b3ac6512aed9bb284ad8c2d28bcdb0962cc893fa9b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["irb"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87e29fd243609335bf73872cef8f77f3eb64caf689902a9427d41d4da91c898`  
		Last Modified: Wed, 24 Jul 2024 08:02:55 GMT  
		Size: 6.9 MB (6946869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de4ec38553454ed5a050b280f5687716a5f1a696120fca981e6b84215d26ab9`  
		Last Modified: Wed, 24 Jul 2024 08:02:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d4fd3afe685050881b256320c0baf94598fecb7fe38c015b343ef36b1da862`  
		Last Modified: Wed, 24 Jul 2024 10:31:11 GMT  
		Size: 27.3 MB (27330690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3d84e9e7e84856b10cb697f508156e6e9b78749fd7cb1dd8d86dfa1754315e`  
		Last Modified: Wed, 24 Jul 2024 10:31:07 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f282001ce09b860b8d7aa60bba83a8d277cd7786f6b791b540f55127d915b406`  
		Last Modified: Wed, 24 Jul 2024 15:19:22 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a7c614737eef73315aed5cdafeacf639e98d012a8f7b4f1f17e107973f1ee4`  
		Last Modified: Wed, 24 Jul 2024 15:19:31 GMT  
		Size: 69.4 MB (69371943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d9aef8a8affe642507e36ca301073a6772c5f213be1fd88f32f2ac4be48c1a`  
		Last Modified: Wed, 24 Jul 2024 15:19:22 GMT  
		Size: 1.2 MB (1163818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54646484093a789fe6276f744737cae9f2e08c8becaac16f47071a4455efbb1b`  
		Last Modified: Wed, 24 Jul 2024 15:19:22 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1adc77784963521f3f0c84f295994c080694dae3f95b259de1064fc59c2fe2b`  
		Last Modified: Wed, 24 Jul 2024 15:19:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48bd86e3b7927c67cda94842ba29a46db353dd65d0bdcecc911c29d62f31e60`  
		Last Modified: Wed, 24 Jul 2024 15:19:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca7a812316b0f2da7b9b95dcf98096c025d28a20edc4fafc265f755188c3b2e`  
		Last Modified: Wed, 24 Jul 2024 15:19:24 GMT  
		Size: 3.2 MB (3244185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd5cf4d853749701505b03fcac7ecd4298a39b2d72532de193b2a0c2be28c53`  
		Last Modified: Wed, 24 Jul 2024 15:19:35 GMT  
		Size: 74.2 MB (74185389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2a65599442d1c7d973fb38a8561fb6fa1409cd1402b84f6c818140e791dd02`  
		Last Modified: Wed, 24 Jul 2024 15:19:24 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:2e394b2d0acfb3852ff6eeb0ea582b43967dbf1711bcdcfbf4adaf3770940c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 KB (43535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5e5cc0f63a71c79ef5fdc013292d22af1c2a3b60aeefbadd479fca9b1cc7f5`

```dockerfile
```

-	Layers:
	-	`sha256:41c7c3edeb2850685f21734b6bc04431b0a908304102c81b1a6627a28e5d1217`  
		Last Modified: Wed, 24 Jul 2024 15:19:21 GMT  
		Size: 43.5 KB (43535 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine` - linux; s390x

```console
$ docker pull redmine@sha256:6c401a0187dcfa84889bf2a000799e0e3d4b0bd153fbe6484e4fefeef6b2aa09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186868380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de04a92fe64331ada8d69df8aa4654f8fcb81a2d08054dd476bd7a8ed2fbc32d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV LANG=C.UTF-8
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_VERSION=3.2.4
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Jun 2024 22:07:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["irb"]
# Tue, 18 Jun 2024 22:07:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV RAILS_ENV=production
# Tue, 18 Jun 2024 22:07:17 GMT
WORKDIR /usr/src/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
ENV HOME=/home/redmine
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_VERSION=5.1.3
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.3.tar.gz
# Tue, 18 Jun 2024 22:07:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=8a22320fd9c940e6598f3ad5fb7a3933195c86068eee994ba6fcdc22c5cecb59
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 18 Jun 2024 22:07:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 18 Jun 2024 22:07:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 18 Jun 2024 22:07:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Jun 2024 22:07:17 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 18 Jun 2024 22:07:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb90b363d3063b00efe8bcb62ebde1f83f67edb6fa04f00f54ce11a82740fd9`  
		Last Modified: Wed, 24 Jul 2024 09:29:39 GMT  
		Size: 7.1 MB (7061663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1ed03d3da7763ee9ea2e6a7afbb48c6359f7960fb8116bcc5659ed9972f614`  
		Last Modified: Wed, 24 Jul 2024 09:29:38 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf313c5bbd0ee348ef6d5996b5dd2c9057ecdaed7308c1e8cc817a901b20636`  
		Last Modified: Wed, 24 Jul 2024 10:25:18 GMT  
		Size: 29.3 MB (29261638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae31725ab8dea92d8964da23271fe6e8a760a22a11982866bb00dc174d33c4`  
		Last Modified: Wed, 24 Jul 2024 10:25:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3308aeee0d512f7bfe80f796188b68a574be04c3a139c0e257a18ce8ca6bbd`  
		Last Modified: Wed, 24 Jul 2024 17:00:14 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6badd309278058aaaa52b31aa55901b3a83c8f1bfd8374a553d71038645b920b`  
		Last Modified: Wed, 24 Jul 2024 17:00:15 GMT  
		Size: 70.7 MB (70719368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cf664bff64602bb4e7de49b51df268610c7533a372c991859f2ed8a8932136`  
		Last Modified: Wed, 24 Jul 2024 17:00:14 GMT  
		Size: 1.2 MB (1160536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d498d06353ea4d44d38af8808982544dd8aa52f810e8df9614a84b15e88ad44`  
		Last Modified: Wed, 24 Jul 2024 17:00:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c38b14613303cedbb0dcbdcb4256bee461e51b81de904091c81b06a7826be5`  
		Last Modified: Wed, 24 Jul 2024 17:00:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6390bdef8037587676301e9f2841fec128202e8dbfc7d98d336eb183a62a18`  
		Last Modified: Wed, 24 Jul 2024 17:00:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337f0fdbdd1122e2c5f30c69e050de8914236c5b3cfe9cb77371b1bfdb48d320`  
		Last Modified: Wed, 24 Jul 2024 17:00:15 GMT  
		Size: 3.2 MB (3244039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c467017e5b1e39cbf0dfe702107b481f2d7230f9952b99cf7c295eb5304d6bc`  
		Last Modified: Wed, 24 Jul 2024 17:00:17 GMT  
		Size: 72.0 MB (71956365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562989effb39c30676e071fa2ebd4eda75ddb67808b68b6dbcc6e391a6f949cf`  
		Last Modified: Wed, 24 Jul 2024 17:00:16 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:aa5c99a1284818ac8dfc83a63b028efba65a164fbefda02682d208fe6d2530cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 KB (43455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2da39e61c73e1954cb848197cd3ff9f0d3835e89ada9bd525602582720acd20`

```dockerfile
```

-	Layers:
	-	`sha256:823ea0580e973a0ebc44214144d610c3086575f2531be0ebf96fa61b98550fc6`  
		Last Modified: Wed, 24 Jul 2024 17:00:14 GMT  
		Size: 43.5 KB (43455 bytes)  
		MIME: application/vnd.in-toto+json
