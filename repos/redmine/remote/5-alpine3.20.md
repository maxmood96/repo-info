## `redmine:5-alpine3.20`

```console
$ docker pull redmine@sha256:67f6f513f076c496451bbd0318ec2d325843d56dd9d145c25ac0eff9c35e1745
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

### `redmine:5-alpine3.20` - linux; amd64

```console
$ docker pull redmine@sha256:a7d13984e0507ac6face0f8b8d1e9d6e935995fe6ba1885f65c14fe37785252f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182022054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7477582a9a3109d71278487392d46d630d68e6f0da8e6c2b92139726791e5fd6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV LANG=C.UTF-8
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
CMD ["irb"]
# Tue, 14 Jan 2025 18:28:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_ENV=production
# Tue, 14 Jan 2025 18:28:33 GMT
WORKDIR /usr/src/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
ENV HOME=/home/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_VERSION=5.1.5
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.5.tar.gz
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=2c9739511712fc1381d9584fa005f911a3022e8366d1d6a53fec0f014dac0168
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 14 Jan 2025 18:28:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 18:28:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 14 Jan 2025 18:28:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a719e694db1541edfc3f5c486b7362842c1d62c9b85ace5aed11eb94afb404`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b9a6180912fc00ed6377daab2202e02052d5141738f2b5ed0f46fb6ebb1a0`  
		Last Modified: Tue, 14 Jan 2025 01:37:17 GMT  
		Size: 33.5 MB (33478828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fa30845653c8ed79d3eabef3d777ba6900ce3503fa9449065fc5a201277c73`  
		Last Modified: Tue, 14 Jan 2025 20:39:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835c205c66bc518bbfff65663b64f70886adbc00632b2b4b07833ba26597d8bf`  
		Last Modified: Tue, 14 Jan 2025 20:29:23 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f1c6739e936d2aaa876bf59d9c4e696c571e9f7315bedf3da92b6098f86c8d`  
		Last Modified: Tue, 14 Jan 2025 20:29:45 GMT  
		Size: 70.1 MB (70077830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d813721373b2c0a93cb21a40dd1ec38eb8d985453694e458e133154b7ef6671`  
		Last Modified: Tue, 14 Jan 2025 23:50:51 GMT  
		Size: 1.2 MB (1166458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33940e1682eb1303150d9ff20b1f2b9cf12dda134cbd8bcd1dc93ed3f5d6c676`  
		Last Modified: Tue, 14 Jan 2025 20:29:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b33c37ef3c897510573cf2ab54b96322a3126a050cc4cb65e4519e56e7adc8a`  
		Last Modified: Tue, 14 Jan 2025 23:50:51 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d0c8127adf3fb074e369465d4ad46fcea539a4705992703193135792c44160`  
		Last Modified: Tue, 14 Jan 2025 20:29:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f87a77f8f48baa885e7ce2076d857047600dafb6876e3e6ffd59358a67bbb5`  
		Last Modified: Tue, 14 Jan 2025 23:50:52 GMT  
		Size: 3.3 MB (3250434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54623a59c136c7fb273fcce82606379028e94707731887f22706f1ef863918b2`  
		Last Modified: Tue, 14 Jan 2025 20:29:46 GMT  
		Size: 70.4 MB (70418589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30f6e61354efbf5ff0e2eb19929c4058e02ccfc366f64a494b1a04b2905485f`  
		Last Modified: Tue, 14 Jan 2025 20:29:24 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:df627ed386823351f4ebb153385eb67dd391b414e822aa9221880b577e001cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39fbea213c65fe0b5881beb15d6514f6bd080cbbec209127beb9d07c0b3b292`

```dockerfile
```

-	Layers:
	-	`sha256:cbde1325d9b5cea199b4308d3460bfd2856847ca84156bc5cc6994ef04f0173a`  
		Last Modified: Tue, 14 Jan 2025 23:50:36 GMT  
		Size: 40.1 KB (40115 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:857efad4ed0d80d5ef7447294edb35c2f4888d970bc5588a532e7674b2b39eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174183397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395547026cb38069728823d91638360ce5c47d6fd1f1548bc96aed0dc845452c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV LANG=C.UTF-8
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
CMD ["irb"]
# Tue, 14 Jan 2025 18:28:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_ENV=production
# Tue, 14 Jan 2025 18:28:33 GMT
WORKDIR /usr/src/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
ENV HOME=/home/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_VERSION=5.1.5
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.5.tar.gz
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=2c9739511712fc1381d9584fa005f911a3022e8366d1d6a53fec0f014dac0168
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 14 Jan 2025 18:28:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 18:28:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 14 Jan 2025 18:28:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646063a45551a61d3aff631507ce28db6d552b256afec6162f53389af67e600a`  
		Last Modified: Tue, 14 Jan 2025 01:42:24 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cc6be5dc5a2a9c2be74f6b1255c80513296d79a9ea80e2efa389237e9f6bee`  
		Last Modified: Tue, 14 Jan 2025 01:52:02 GMT  
		Size: 29.8 MB (29828000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9659a935ffbf249164701ccc1a768c2004912517229f38f637161a955ec6543b`  
		Last Modified: Tue, 14 Jan 2025 01:52:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca75dcf124fb918bc923fa41555feb0f1bff5794e12cd2656efaae86d20e051`  
		Last Modified: Tue, 14 Jan 2025 02:26:06 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea87f5579b70428b615bfe64f9aded2f5fd46f2f36d231398b2d70f40c19e604`  
		Last Modified: Tue, 14 Jan 2025 02:26:09 GMT  
		Size: 66.8 MB (66832525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600f2c049109738cce6eadbfc9bc74d1e011ec0175f2d11763e381d4d6cb08f1`  
		Last Modified: Tue, 14 Jan 2025 02:26:07 GMT  
		Size: 1.1 MB (1133486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6654a179a89e65f8a21d429842bd3e5d1cb01c951d0abf9424c32fade4c40772`  
		Last Modified: Tue, 14 Jan 2025 02:26:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7808230ad9fc3590dedb9c8024d059ce3efc7455e484d637371ecbe427138e`  
		Last Modified: Tue, 14 Jan 2025 02:26:07 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e5db91081a64de4b2725fc8faa46889b01761b885775a26ee132e207c1188`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db2146c02f69f8733832dba7b626e98213cb63514ed6f9d2f1033755f2ac9f5`  
		Last Modified: Tue, 14 Jan 2025 02:26:08 GMT  
		Size: 3.3 MB (3250699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f60cc9c2ff42789bd954cf0bbe2fbfe8cd1c58ff520d7147331bd1fee198c4`  
		Last Modified: Tue, 14 Jan 2025 20:37:34 GMT  
		Size: 69.8 MB (69763558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08665420070ac1ef2fae55060e3c673cf2853d274356fa7c91c332b67cae2226`  
		Last Modified: Tue, 14 Jan 2025 20:37:32 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:f73035a6e36004fef042bfdc963b70f94b80d07cf5167ada2be571764bb6b55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bd030850234db16725254c17d97a2d6919fbf5d7348bfd224db0dfbf2a4f5a`

```dockerfile
```

-	Layers:
	-	`sha256:f68744ac33f6d8f0e84c2b34165cb2f2650652899e6066c6e012dc3c2126636a`  
		Last Modified: Tue, 14 Jan 2025 20:37:31 GMT  
		Size: 40.3 KB (40260 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:a48fc8b8794293a33e492ebc21df3b3767708073500bd76edd7ed5772bc25ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170093781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d24b61f7112cc67eff88cbec6a73f83856f8bfe7b6325e8a186b0f24b3d5257`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV LANG=C.UTF-8
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
CMD ["irb"]
# Tue, 14 Jan 2025 18:28:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_ENV=production
# Tue, 14 Jan 2025 18:28:33 GMT
WORKDIR /usr/src/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
ENV HOME=/home/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_VERSION=5.1.5
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.5.tar.gz
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=2c9739511712fc1381d9584fa005f911a3022e8366d1d6a53fec0f014dac0168
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 14 Jan 2025 18:28:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 18:28:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 14 Jan 2025 18:28:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04cd14ba7406c54223a25e09ff76f4ed50955d6c12ebda81a014cf1bcb3461`  
		Last Modified: Tue, 14 Jan 2025 01:47:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075b2b9ba4a5b9af0d50aa856ace66277dacdeb7a4018aa7790e8bde561e593a`  
		Last Modified: Tue, 14 Jan 2025 01:56:47 GMT  
		Size: 29.7 MB (29664552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1331f6e976eff189be48048dc94d765d1bf456ea02fadad9fd8ea0e7bd6aaf`  
		Last Modified: Tue, 14 Jan 2025 01:56:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f767ecf633d9bfde2015f1cb3d01c7c2aee74526cc590cf7f48a7ab7f1954e`  
		Last Modified: Tue, 14 Jan 2025 22:59:13 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0c0a484c1e5b7d13eb01755af33236b3910c6a1aaf7807790ce3b69ff7c00c`  
		Last Modified: Tue, 14 Jan 2025 22:59:16 GMT  
		Size: 64.2 MB (64185651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca7ec28b57cf32b19529bacb7e638b2bbe1282bc0038d9cf349f9b12622c11b`  
		Last Modified: Tue, 14 Jan 2025 22:59:14 GMT  
		Size: 1.1 MB (1133487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048af5e8b164bb62e6ac86d70593f5e77db449bb7253d33e4e83c693b8df67db`  
		Last Modified: Tue, 14 Jan 2025 22:59:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7c9611c1898c0ad55725dd4116d181bd886e300363c83ac1f70f6591a13ff8`  
		Last Modified: Tue, 14 Jan 2025 22:59:14 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded98839e2456618c190f8fba3bf99914a4c1125dfc2fc45eb91552ccaae2cc8`  
		Last Modified: Tue, 14 Jan 2025 22:59:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb7ddac8349624bcca8d1ddee52fb7dbf0aa1de568c762cbc891ded97c94ef`  
		Last Modified: Tue, 14 Jan 2025 22:59:15 GMT  
		Size: 3.3 MB (3250410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805bfd8d90c4a6b88ba3cac55070ab754d7ebd01f56c275a018056a88be27d03`  
		Last Modified: Tue, 14 Jan 2025 22:59:18 GMT  
		Size: 68.8 MB (68760510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3630cde83cf28675f462c0709971a31449dea6e46a4108949833ce643baa8fb1`  
		Last Modified: Tue, 14 Jan 2025 22:59:15 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:19313e43b5a4e70ac7ef76175b546b58c33b525017d2580d759bb2a152e0dee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82dabb80017d2efd81e03c89c9aaa9b76a7b172f31db9d62021e9f2fb006e9b`

```dockerfile
```

-	Layers:
	-	`sha256:4be6bc7901d7c0e1c530c9feee68b3076ea745e2f79e5672be578ff097eddc9f`  
		Last Modified: Tue, 14 Jan 2025 23:50:38 GMT  
		Size: 40.3 KB (40261 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:4e147d46974a4a14bc63bf54d0f05f5ec072e186da517dab73b80fb969449feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182979008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b0b1c87a21863168a2f6bce766ed2dfaac25090e02db07991a78875bdefcba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 14 Dec 2024 00:12:59 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
CMD ["/bin/sh"]
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV LANG=C.UTF-8
# Sat, 14 Dec 2024 00:12:59 GMT
ENV RUBY_VERSION=3.2.6
# Sat, 14 Dec 2024 00:12:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Sat, 14 Dec 2024 00:12:59 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 14 Dec 2024 00:12:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 14 Dec 2024 00:12:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:12:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:12:59 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:12:59 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV REDMINE_VERSION=5.1.5
# Sat, 14 Dec 2024 00:12:59 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.5.tar.gz
# Sat, 14 Dec 2024 00:12:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=2c9739511712fc1381d9584fa005f911a3022e8366d1d6a53fec0f014dac0168
# Sat, 14 Dec 2024 00:12:59 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:12:59 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:12:59 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:12:59 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b061e389e1cfaa1b6c20109d4c4f25f3fbc6449802a6b02e00043572ab4bceb`  
		Last Modified: Tue, 14 Jan 2025 20:51:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a49c475ebe8cbceee636ff80148d84e1cda7f72aa4a2891191ca38c6e465299`  
		Last Modified: Tue, 14 Jan 2025 21:28:08 GMT  
		Size: 33.5 MB (33478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1ed0c73ceca351ad7c2bdd82bbe2711320d3e894af3bc48b3c1fba7e7f48e`  
		Last Modified: Tue, 14 Jan 2025 21:20:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a0cc8e774862c4b23a35d65735bd9ccc2aab019360941b2be766e00670bb65`  
		Last Modified: Tue, 14 Jan 2025 21:17:14 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d229290a390caee24322fe59ec72c4f7e8ce4dfcf5b9ab5b60d58d561212b71`  
		Last Modified: Tue, 14 Jan 2025 18:17:18 GMT  
		Size: 70.6 MB (70558028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa614e36c61958819578bd882c86bb23062d2e3520381bf7505208e984f7d63c`  
		Last Modified: Tue, 14 Jan 2025 18:17:16 GMT  
		Size: 1.1 MB (1093073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c0b107c99dfc1d0a81fcb5c73ab886511081bcdbf1975fd75e0ffcd88e8645`  
		Last Modified: Tue, 14 Jan 2025 18:17:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6c931af8a5b729c0598f374d2a2ace0321514e720381b66ad0f9abde2d98d6`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d4a3466570281f48d71e17a77132c6ff56bced7e186cbe90789ddb37351c3f`  
		Last Modified: Tue, 14 Jan 2025 18:17:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0c3ff80a18d1377a63d837cad3d2159f9f1160808dfbc61fed12ee96d71f8a`  
		Last Modified: Tue, 14 Jan 2025 21:17:21 GMT  
		Size: 3.3 MB (3250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe700a6140a8af9591b2994423b2827ddc79f2a32d164bf2984e8e7a6167aeb`  
		Last Modified: Tue, 14 Jan 2025 21:17:26 GMT  
		Size: 70.5 MB (70504303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5f3d1da398d1e758176e3ac91b1c46bcc01636306e108cbf704e1f6a2c30e2`  
		Last Modified: Tue, 14 Jan 2025 18:17:18 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:8ac7d7827066b4d78aff4fbfe82b504cdb37fa1a8564d9cbe18a81e0bfe9dd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f75a6ac81e39173e5388814f766e32ef414e60cc792d4a3b4c05e6298e4ece7`

```dockerfile
```

-	Layers:
	-	`sha256:d0a5399847716cd806f62f32f60629b554345be17a0ca23f56553482c66f1a6d`  
		Last Modified: Tue, 14 Jan 2025 18:17:16 GMT  
		Size: 40.2 KB (40225 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:72c502c9aea2da4078b82fb44b03dad1944731daaab62dfc9daf8f831c9c684b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178949157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20617661dbb426bb682e711afa7f52938a255ff20a374bf1b48416f48042f54c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV LANG=C.UTF-8
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
CMD ["irb"]
# Tue, 14 Jan 2025 18:28:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_ENV=production
# Tue, 14 Jan 2025 18:28:33 GMT
WORKDIR /usr/src/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
ENV HOME=/home/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_VERSION=5.1.5
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.5.tar.gz
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=2c9739511712fc1381d9584fa005f911a3022e8366d1d6a53fec0f014dac0168
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 14 Jan 2025 18:28:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 18:28:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 14 Jan 2025 18:28:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e189947a713b398fb29def22373261240c5dca0c3934f838baf89fc97a030370`  
		Last Modified: Tue, 14 Jan 2025 01:36:58 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561f5ba489b5283e95aadf5eaabd1acceb6843e66d4e971b670a99dd28904e6f`  
		Last Modified: Tue, 14 Jan 2025 23:50:53 GMT  
		Size: 29.7 MB (29692874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae8aabf1b7219bab922d4debfd0fe04b8b0779872f0f2499ed5f3ad48700a1c`  
		Last Modified: Tue, 14 Jan 2025 23:52:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3fa35730b3574fdedc605c880474a15359a862a35e1234818b48e89aa5951c`  
		Last Modified: Tue, 14 Jan 2025 20:30:09 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48cfd4606818a4f635acf09e16fa297a3aadda88c7b062c564cc8b681a48016`  
		Last Modified: Tue, 14 Jan 2025 20:30:13 GMT  
		Size: 70.8 MB (70817856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ac0f1c5cf1f78f5575dfe3c8898e44113229bd90ed5eda59edc3ce4d7d009c`  
		Last Modified: Tue, 14 Jan 2025 20:30:10 GMT  
		Size: 1.1 MB (1141323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fbfbf0f30c12116a0f502dd6b909e7fbeaa548c7ef95417e3232f2adce9c32`  
		Last Modified: Tue, 14 Jan 2025 20:30:10 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9536cc17e69fb65e136bde60d1892330d0cc458dd248b9a234526f0b65179c4`  
		Last Modified: Tue, 14 Jan 2025 20:30:10 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a1ef6333e959f05cef3e30cb2d4b6896ac962b3d54d0c2fe040cbb3684683`  
		Last Modified: Tue, 14 Jan 2025 20:30:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9198252312ac0834c352d4c8b6140ec40dd11ee4410d6c0beb958286aa972c39`  
		Last Modified: Tue, 14 Jan 2025 20:30:11 GMT  
		Size: 3.3 MB (3250717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de1eb0911d13b97a676165e1d06dbd0073d84d1287196a796fe1755ae7403a0`  
		Last Modified: Tue, 14 Jan 2025 23:50:58 GMT  
		Size: 70.6 MB (70571758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d2dbf8293eda348ae9c21b4f2180a0d471f30e033f33257d3da113b2db561`  
		Last Modified: Tue, 14 Jan 2025 20:28:31 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:c60a4333ba4cf6828f23659e9a7a92a1c904797ffd49b82c8b777e37e1586ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd58219c3e9115134ccfb97be1488bfaa4c024af957e75314fb400a6e64d7c1`

```dockerfile
```

-	Layers:
	-	`sha256:5645f4e2d4ce775c970fec701c05e8aa316f4a2d94d68f09c5e727495922e3ad`  
		Last Modified: Tue, 14 Jan 2025 20:30:09 GMT  
		Size: 40.1 KB (40076 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:ca6f0d2f2327dec473013723af3bd739fd59e36fbae3505d5e382131c05001dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183146655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd05e06e1cdf7a2b5f18424976eaef6bba9da03da234b90b42f27fea0896afc0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV LANG=C.UTF-8
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
CMD ["irb"]
# Tue, 14 Jan 2025 18:28:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_ENV=production
# Tue, 14 Jan 2025 18:28:33 GMT
WORKDIR /usr/src/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
ENV HOME=/home/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_VERSION=5.1.5
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.5.tar.gz
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=2c9739511712fc1381d9584fa005f911a3022e8366d1d6a53fec0f014dac0168
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 14 Jan 2025 18:28:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 18:28:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 14 Jan 2025 18:28:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd611afdfde6a92b771a8c2f4dd7b096a1311acfb8646e981977bf38912787b`  
		Last Modified: Tue, 14 Jan 2025 01:48:43 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b201a935bf33b295fd9333ec90113ccbc5c5de9a265ac6538866d868a24ef`  
		Last Modified: Tue, 14 Jan 2025 20:55:09 GMT  
		Size: 31.1 MB (31123090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59df318c99db4c253e211a04ee35836b0af1a035f5af50e6b21fc6adf9c2c748`  
		Last Modified: Tue, 14 Jan 2025 01:59:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4971ad0e64c370ecaa3cd0acb68f42bca49a5fd25eca93dcc3ef41ce4bd2131b`  
		Last Modified: Tue, 14 Jan 2025 20:58:23 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aab48d407ab7bc6cafa9875cdc703268c8892e555b1dbc31d7c5810430e222`  
		Last Modified: Tue, 14 Jan 2025 20:58:26 GMT  
		Size: 71.8 MB (71775388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed750cabbd868319bfed4376778792f8b48c084b7dc99750ab6bf653b5d8de`  
		Last Modified: Tue, 14 Jan 2025 20:58:23 GMT  
		Size: 1.1 MB (1083693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9b77bdef5d6ce6e9b29bcd44ba26c2d25a5aa8c85f94a66d10faf462bcc778`  
		Last Modified: Tue, 14 Jan 2025 20:58:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150d9fe708d504e03ec9415c45fc2a681e679f980510f67f438837fba3bba89`  
		Last Modified: Tue, 14 Jan 2025 20:58:24 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6643aeb60857a3e65152355d574f0ee8c56ae033b42b161e4b0a7196e94417aa`  
		Last Modified: Tue, 14 Jan 2025 23:50:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddbf9e1ed9a0e9f6d45d06c2863a2f73b9023a13d6fc003694e7439f8025462`  
		Last Modified: Tue, 14 Jan 2025 23:50:57 GMT  
		Size: 3.3 MB (3250707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b49c0f865ce0ac4c4cafc0563b4764e407816144f6b1666a7e11d67ed90bcb`  
		Last Modified: Tue, 14 Jan 2025 20:58:27 GMT  
		Size: 72.3 MB (72335715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19754d1f4d7b132239e450318c5c4efc4ec662ee455e9ce604b2a56a2393039b`  
		Last Modified: Tue, 14 Jan 2025 20:58:25 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:c12803b2d9c87b6912777505ae52fe611d22ff2fdc051a6308b59457b65a64c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27f6952254cf4d040b6d3ec8cfdbc3d9b58615f8b1a7d08dfe98b39c0049e98`

```dockerfile
```

-	Layers:
	-	`sha256:d84647b49428d9037f8757f8a0738de040d477ff8d98eb59a6adadb112dbfb37`  
		Last Modified: Tue, 14 Jan 2025 23:50:42 GMT  
		Size: 40.2 KB (40165 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:6f22099c5d25e7272f3eee5c4909cdef50b6f1a4838e8ddf4289862c65fea955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181698956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecad08bb46036acb5441aecad90c36754ced2415dc6c78c0a322dbd1dfce30aa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 14 Dec 2024 00:12:59 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
CMD ["/bin/sh"]
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV LANG=C.UTF-8
# Sat, 14 Dec 2024 00:12:59 GMT
ENV RUBY_VERSION=3.2.6
# Sat, 14 Dec 2024 00:12:59 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Sat, 14 Dec 2024 00:12:59 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 14 Dec 2024 00:12:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 14 Dec 2024 00:12:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
CMD ["irb"]
# Sat, 14 Dec 2024 00:12:59 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV GOSU_VERSION=1.17
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV RAILS_ENV=production
# Sat, 14 Dec 2024 00:12:59 GMT
WORKDIR /usr/src/redmine
# Sat, 14 Dec 2024 00:12:59 GMT
ENV HOME=/home/redmine
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV REDMINE_VERSION=5.1.5
# Sat, 14 Dec 2024 00:12:59 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.5.tar.gz
# Sat, 14 Dec 2024 00:12:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=2c9739511712fc1381d9584fa005f911a3022e8366d1d6a53fec0f014dac0168
# Sat, 14 Dec 2024 00:12:59 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Sat, 14 Dec 2024 00:12:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 14 Dec 2024 00:12:59 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 14 Dec 2024 00:12:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Dec 2024 00:12:59 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 14 Dec 2024 00:12:59 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb69847f873261cc901364c6e5453bc8ac36796ac8944ffe1685a0c21d2a1f0`  
		Last Modified: Wed, 15 Jan 2025 07:32:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa157ceb4aed7377211e94d6cc005d0d7f018a733827afca5ca0a88714d6ee7`  
		Last Modified: Tue, 14 Jan 2025 11:08:38 GMT  
		Size: 29.6 MB (29631708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6ff83b38b0d5f8c168c3768981189deaa08e81afb0458baf093d684e12257d`  
		Last Modified: Tue, 14 Jan 2025 11:08:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f96cc36cf5f39e6003d2600943b3fb0fe49131136ce55c5ea7691d87ce261c4`  
		Last Modified: Tue, 14 Jan 2025 18:56:17 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed6f9b9e5f4dd5aa8037efdf25968decf42593deb0467b9df56a52077322a46`  
		Last Modified: Tue, 14 Jan 2025 18:56:28 GMT  
		Size: 70.5 MB (70456771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebda25472b2ca434b949fd1635da4f66204dcb10297c43918096ff11e53a1c72`  
		Last Modified: Tue, 14 Jan 2025 18:56:17 GMT  
		Size: 1.1 MB (1134861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7019426b638ba155a40319efa739ccacc2d94d5d52c58b7ab72792994e6eec`  
		Last Modified: Tue, 14 Jan 2025 20:50:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fba5742836cda49655db7b895a0e231b57dd7ada975fe6633a67144f7df9b9`  
		Last Modified: Tue, 14 Jan 2025 18:56:18 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b6cfaf3670f0e7f759af997cf53b8de31e1cf0ec94d8ae328237f398bdf445`  
		Last Modified: Tue, 14 Jan 2025 20:50:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf084b826cf69652b71d7866827bb49ccfaa772978b400f2a67145372b991bb`  
		Last Modified: Tue, 14 Jan 2025 18:56:19 GMT  
		Size: 3.3 MB (3250718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8da29c00d04123ce2e624e950226272e024fcedc4e579e05c8d6f11f0920b6`  
		Last Modified: Tue, 14 Jan 2025 18:56:30 GMT  
		Size: 73.8 MB (73849310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fada68c5b6a1fb8f8f0f4c61c22614648cf08b90dea26fad09347842d68424`  
		Last Modified: Tue, 14 Jan 2025 18:56:19 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:520ac5ef54d1bee4cf1c248e698b335e3024aab839fa3d3dc50082ecada3b489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469436b32059a92f0cf4e1aaf32ec1d5058554cb78895589900681280cf39839`

```dockerfile
```

-	Layers:
	-	`sha256:bfc6bdf2057d88d4d64775a03bf71066e0166373cdae31db15b711eb5c9e6fd5`  
		Last Modified: Tue, 14 Jan 2025 18:56:17 GMT  
		Size: 40.1 KB (40094 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:9ebb23a9621fd8139d48671d05972f2bee682e99ec80a5b0813fccb60c8ddc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182379600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e31dd54f34fc6c7d8e9f4cae5a5ad10a526a78d9d24c3284154fcd0e55d961`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV LANG=C.UTF-8
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_VERSION=3.2.6
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Mon, 13 Jan 2025 23:09:45 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 13 Jan 2025 23:09:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Jan 2025 23:09:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 13 Jan 2025 23:09:45 GMT
CMD ["irb"]
# Tue, 14 Jan 2025 18:28:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_ENV=production
# Tue, 14 Jan 2025 18:28:33 GMT
WORKDIR /usr/src/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
ENV HOME=/home/redmine
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_VERSION=5.1.5
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.5.tar.gz
# Tue, 14 Jan 2025 18:28:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=2c9739511712fc1381d9584fa005f911a3022e8366d1d6a53fec0f014dac0168
# Tue, 14 Jan 2025 18:28:33 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 14 Jan 2025 18:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 14 Jan 2025 18:28:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 14 Jan 2025 18:28:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 18:28:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 14 Jan 2025 18:28:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27470f160962be7e0327882668c9f8725389d49d37e462a3fd04f6b968da5e0`  
		Last Modified: Tue, 14 Jan 2025 01:47:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0816b75f512d244847ddb83c0509552748ac929c93d88ad1a63f4b84c9c6b6d`  
		Last Modified: Tue, 14 Jan 2025 23:50:54 GMT  
		Size: 31.0 MB (30992732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e3dbf660b401170e2195d47634b524a9772a66e17025aec453e1b4033909c2`  
		Last Modified: Tue, 14 Jan 2025 01:58:50 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36330168bcc623c7031373c17b4bd7d5a08f55241f60cf4b477cfc88a7cbcbdd`  
		Last Modified: Tue, 14 Jan 2025 22:15:43 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee641c6116536e7c6e151d1fca80605eef7cf007f48477d7b43fc569b8053a0`  
		Last Modified: Tue, 14 Jan 2025 22:15:44 GMT  
		Size: 71.9 MB (71943657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e3bf8f5f05fc685239b4b0142772a190c5f92318435c504438f85916a12539`  
		Last Modified: Tue, 14 Jan 2025 22:15:43 GMT  
		Size: 1.1 MB (1131126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74478eda31b45a527363a0663a21f8bbd87f20c433b48f2e2e561573eeab8f9`  
		Last Modified: Tue, 14 Jan 2025 22:15:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5aabfcd7093a4c4e1ef610864454aae2b657f7484ea1cb80891b394c19bfb`  
		Last Modified: Tue, 14 Jan 2025 22:15:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38e06c91b1789542941d1356cc8f01791ac421256c65ac946a45de10eb4d51f`  
		Last Modified: Tue, 14 Jan 2025 22:15:44 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a7bc7f4ca174589e5a46e31ec2fa72246cde18dc0e770e20c411e403f12221`  
		Last Modified: Tue, 14 Jan 2025 22:15:44 GMT  
		Size: 3.3 MB (3250702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbfce4a4c283a363618e696c30f539045cfc12c03eb2563e5ac7f7a141b3cfb`  
		Last Modified: Tue, 14 Jan 2025 23:50:56 GMT  
		Size: 71.6 MB (71594404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0668b327ebdbbad739e51e0791a8b58f791a12a0e7c4beb7516d94239139ae5c`  
		Last Modified: Tue, 14 Jan 2025 23:50:52 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:1c102dcfcc2cabeaf755894890059c62f0aadc6ff07ed5cceff48ea68a5cd594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbd481821c81821bc9974151dd03dd36b94f9603fece3277c71b237d63f647e`

```dockerfile
```

-	Layers:
	-	`sha256:5ca3f20332552208cdc220401aceade2d004a7d5bc1d0718a3a4e7c22466481d`  
		Last Modified: Tue, 14 Jan 2025 23:50:44 GMT  
		Size: 40.1 KB (40115 bytes)  
		MIME: application/vnd.in-toto+json
