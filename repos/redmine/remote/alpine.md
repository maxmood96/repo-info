## `redmine:alpine`

```console
$ docker pull redmine@sha256:07b51e4e4f19ca513569cbbe0f95d18c6a6f4ca88a73a088707e4384c486b350
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `redmine:alpine` - linux; amd64

```console
$ docker pull redmine@sha256:a0d567487b52696c4e7d31ec9e0acb9b192b365e350f7d485c3b1772ae3238b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186043966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5f0f4cbe9c90d06f421fed7fb6148ea060e73f8942fccb3a3eaf3353bafb8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 29 May 2024 20:43:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV RAILS_ENV=production
# Wed, 29 May 2024 20:43:51 GMT
WORKDIR /usr/src/redmine
# Wed, 29 May 2024 20:43:51 GMT
ENV HOME=/home/redmine
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_VERSION=5.1.2
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 May 2024 20:43:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 May 2024 20:43:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 20:43:51 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 May 2024 20:43:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a78ef59060f3f9982a40978bcf075f74504bbb0af32248ee79ad51f0ce54be1`  
		Last Modified: Wed, 22 May 2024 22:58:28 GMT  
		Size: 6.7 MB (6686041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6898f7a531277cf5705741be398abc8711f7505fd9d6185765b43d89913053`  
		Last Modified: Wed, 22 May 2024 22:58:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d6bc5296deeebda15a473f06132e7871bbaec9a52f1f71789e81f4448f028e`  
		Last Modified: Wed, 22 May 2024 22:58:28 GMT  
		Size: 32.1 MB (32104623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7b555ad78e3b45dbfe496278dfd744c045965720e892755832b38f3671f94c`  
		Last Modified: Wed, 22 May 2024 22:58:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770a8722f315a8d407a226f7c11a82a48d6dd5b7749b2436eb852eb4a3b304a6`  
		Last Modified: Thu, 30 May 2024 01:02:11 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3c3d9dedbe06defde9987d90ae98642ac7f563fafbe81ea9be900128860f30`  
		Last Modified: Thu, 30 May 2024 01:02:14 GMT  
		Size: 69.6 MB (69610064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3701455cd5a6813b564fd93c0e6e3fa7e6fc5717cbebba0d15d95b7e9e11bd5b`  
		Last Modified: Thu, 30 May 2024 01:02:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15901ddc6ed8978a3c41c54483dc7efc651a0eec8496906794cb6ea1faf6427c`  
		Last Modified: Thu, 30 May 2024 01:02:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2869ceb41b7aa7a85f37af407b3e9997ce5bc2cdbb676f862631fe759dd68dd1`  
		Last Modified: Thu, 30 May 2024 01:02:13 GMT  
		Size: 3.2 MB (3243018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c427c362cc90309e9132fc82f2d00167b86aa7cd4a7c6c09aec8d082d038fe45`  
		Last Modified: Thu, 30 May 2024 01:02:15 GMT  
		Size: 70.8 MB (70774594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9977be28194f377980f359cd72dbbd2065d6467fff5e62c799c1f5d212582`  
		Last Modified: Thu, 30 May 2024 01:02:13 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:24ca6cddcb62b5d2a794d5c5262c9e8d1c3b1296e4b15a1c98ea4dcddb53817b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b0319f26b12a611609c3d8f3013a741ae66fcd5b68f37e9112681ace307b0`

```dockerfile
```

-	Layers:
	-	`sha256:6fc6429a1d178bcccc617b57b72f78c0ed471d69d36173cb07d93ec572fef879`  
		Last Modified: Thu, 30 May 2024 01:02:11 GMT  
		Size: 34.2 KB (34215 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm variant v6

```console
$ docker pull redmine@sha256:17f9773809a79267f66f2787598f459da159b1f96507221c9b81edf5287718a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180365564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af26bb8739f9e7122ac566e2ca39b159608f4d6d7a1ea489b25bfb498396f04b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 29 May 2024 20:43:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV RAILS_ENV=production
# Wed, 29 May 2024 20:43:51 GMT
WORKDIR /usr/src/redmine
# Wed, 29 May 2024 20:43:51 GMT
ENV HOME=/home/redmine
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_VERSION=5.1.2
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 May 2024 20:43:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 May 2024 20:43:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 20:43:51 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 May 2024 20:43:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba601ab84a54fbd88961a2445fe3844aa545bb92bceb0a919bbf9c4416bc413e`  
		Last Modified: Wed, 29 May 2024 00:39:01 GMT  
		Size: 6.5 MB (6533788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb6864cb0b33a079eb5dd296147ff306afee376b622082f53b002425c6acb48`  
		Last Modified: Wed, 29 May 2024 00:39:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95034f7f916814c7d2a405c96a859607debcbc56115a28d3c15962f45f222016`  
		Last Modified: Wed, 29 May 2024 00:43:38 GMT  
		Size: 28.2 MB (28244111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e150d1811856ad961fec6b7806efadfd550ccd8171b6564db13a681165e678b2`  
		Last Modified: Wed, 29 May 2024 00:43:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80883709f1dd3111cd0d5fde58af5cc8b14999fd5f67a32b0fcaaead76d05a3e`  
		Last Modified: Thu, 30 May 2024 01:15:24 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1aa2e84c023ec6d0ec622d9d4b0c015ed1df5b85a6aeb48c58ab7719529b16`  
		Last Modified: Thu, 30 May 2024 01:15:26 GMT  
		Size: 68.9 MB (68863877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3403bdc533164c1730a9f58b307241a86eee3ce947cff49fb8e14a9b26df42`  
		Last Modified: Thu, 30 May 2024 01:15:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af478e90e6f4b39f11d95c819fd9944530ac147f1bd556e9c44388f194ebeda6`  
		Last Modified: Thu, 30 May 2024 01:15:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfa6da0af449aeab6c14a3038f96cb4ae477c4c0c75597d53d62db750474bcd`  
		Last Modified: Thu, 30 May 2024 01:15:25 GMT  
		Size: 3.2 MB (3242972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d158a990c7ae5fa4f353fa8814d3f372a56a953093efeeafc74027753e97f5e`  
		Last Modified: Thu, 30 May 2024 01:15:27 GMT  
		Size: 70.1 MB (70112229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9521177e01cb1ed80286b7bb9cbb5164bd9587f67db82259b58c1c0ba33b43`  
		Last Modified: Thu, 30 May 2024 01:15:25 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:0d6b394ff084d478328d11a356dcb307b646d5bc41d8e0ffdaba2ecef8029b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 KB (34424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b81b3e8e34f4c106eefe500c64bed755adb9f83a98ec23dc96f9fea6dbc108b`

```dockerfile
```

-	Layers:
	-	`sha256:d03e3d0dd4efd478aed5dc8f5188525773b6bef064beaf2d8293ccd633675e9c`  
		Last Modified: Thu, 30 May 2024 01:15:23 GMT  
		Size: 34.4 KB (34424 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm variant v7

```console
$ docker pull redmine@sha256:f2f53e0a62ef9cb3369d2c83cd85fcf6877d303c08f0a10761649e7f9f2e1979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187568732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c8410993a1a49da6ac68d09ce5124081569226661cb9c39a82fa83687507ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV LANG=C.UTF-8
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_VERSION=3.2.4
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:34:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0024e184ce899205e2450f8f2b33be31d0264636f395ec416b756755089189d3`  
		Last Modified: Sat, 16 Mar 2024 18:03:00 GMT  
		Size: 3.7 MB (3717087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d2ff0bc9c4fcf8807846cd7cdeeb2c3a3ed5d647d6e1e9c6b3afa13c0d033`  
		Last Modified: Sat, 16 Mar 2024 18:02:59 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6540439ddf5e1e7b6eb4e80bc550670012c5d4e0d098079197a75778381420bf`  
		Last Modified: Tue, 23 Apr 2024 17:52:19 GMT  
		Size: 29.8 MB (29754450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bde9ed09649652548112347e7fa668e1245eace35a31b84bbaecf7a980b6fa5`  
		Last Modified: Tue, 23 Apr 2024 17:52:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd495bf30f5c58f23e1922d56ec490de45a7717f04f6fc4b0d3c8f16092d1b`  
		Last Modified: Tue, 23 Apr 2024 19:32:40 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab694c316adca0f9778be934bf4b020f3024b07bf949173cc6ded55a560479aa`  
		Last Modified: Tue, 23 Apr 2024 19:32:42 GMT  
		Size: 79.4 MB (79403229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd607d1c494d3da2ceea470cc1f132da70141ee5c3d2808f9446d9bb94569fe`  
		Last Modified: Tue, 23 Apr 2024 19:32:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3280177164c2da3c419b7c80168fbe9fd42056288810350bd3e7cd1fbd9f3a`  
		Last Modified: Tue, 23 Apr 2024 19:32:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ed7ddaa6a96df0c0240c7a724ff98e57eb03958b75c42a3bc0f85ea72c04f0`  
		Last Modified: Tue, 23 Apr 2024 19:32:41 GMT  
		Size: 3.2 MB (3242811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291b06cbca4f9e426a7d87e77d69de734c5b60650bdc4414a767bb8e6c7efb0c`  
		Last Modified: Tue, 23 Apr 2024 19:32:44 GMT  
		Size: 68.5 MB (68545949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23622c2e5b1b44898b5d8f6784340ec0fca027e24b409f8b5ee362103ae4da0`  
		Last Modified: Tue, 23 Apr 2024 19:32:42 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:138b71f02370d19cc4bf549f52d3960b732aa424e63b87740e7201eebaca9e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5372999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20932b66c6b9c3114abb329eabe51b88f0849956849310ea4122381593945265`

```dockerfile
```

-	Layers:
	-	`sha256:93f0531312f6bd3d85f6d74420b77785514bc2b79d26a9eb8cda3ee87ecf4a3d`  
		Last Modified: Tue, 23 Apr 2024 19:32:40 GMT  
		Size: 5.3 MB (5337558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b087b012cdb2fcabebc1001b8ec886ce634dc8f3dde7dfaf99e37b24e51d27`  
		Last Modified: Tue, 23 Apr 2024 19:32:40 GMT  
		Size: 35.4 KB (35441 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:a608c688d4890209b6c45313530ab6c9d277652914cc76b1795aa3f3f0aabc0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201760004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eef305668652a740aa72fd92c2a8e9ba7ae7ebadcc08466fc29782801277d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV LANG=C.UTF-8
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_VERSION=3.2.4
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:34:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d002cb486864f216503b0e91a5fbfa1d4bff221bedad1208479f784d068c0ca6`  
		Last Modified: Sat, 16 Mar 2024 17:00:31 GMT  
		Size: 4.1 MB (4061386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73f9a3c5db2eccc0dbf307416289b5d4fa59b45ae3ae604086cb3c854fecba`  
		Last Modified: Sat, 16 Mar 2024 17:00:31 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bf32488dbfcebe416f45916c55ef4000ef91383c4aca2d50db6a7bdc7cb484`  
		Last Modified: Tue, 23 Apr 2024 17:31:43 GMT  
		Size: 34.1 MB (34093624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc96d205ec96f39276a028a0e2d5defb2f7bceb0abf226f4f41a940a9887e32`  
		Last Modified: Tue, 23 Apr 2024 17:31:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85b52f5edc8d06e148b466efad57334ad15f4eb0c1c0e2edb03dc56e9a14a79`  
		Last Modified: Tue, 23 Apr 2024 19:41:07 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec32c6bbef7c137766aef7678a7f297a58a0ae78b63e293e3b3937a1a6987aee`  
		Last Modified: Tue, 23 Apr 2024 19:41:09 GMT  
		Size: 86.8 MB (86817836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8675a8972361f4647535a62a9eeebe4fe0d218cd35f6e4dd0b1087e3ed54ba74`  
		Last Modified: Tue, 23 Apr 2024 19:41:07 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83483e3e47c27ac974fc5a41d251f2b92164a662f8e8985cfc12f10f612966c`  
		Last Modified: Tue, 23 Apr 2024 19:41:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf3e99d372d622f17bea3c17618cda09a0abbc06edd5b68002323e977ebeb8b`  
		Last Modified: Tue, 23 Apr 2024 19:41:08 GMT  
		Size: 3.2 MB (3242907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6b290506ad4a45a05c0ff2253f60f1e18512954d070c61466f810524d1feaf`  
		Last Modified: Tue, 23 Apr 2024 19:41:11 GMT  
		Size: 70.2 MB (70207083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a590804d5f65b7aad1eff2c3c4fdc730f8397845f6889efe48a8a8f399547f0`  
		Last Modified: Tue, 23 Apr 2024 19:41:08 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:13ec1927b9437722f6d250dc659560fbd3b0c4819a76a35fe4095615a12fd58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5373805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120f9d026d4e13f14a732e33c4a8606c102855aa04df84740ec9fb42c1583c69`

```dockerfile
```

-	Layers:
	-	`sha256:2e04a5ddeb4ccb12c574d19090ce27bc5a75254f27d361efb30b5d06e68af657`  
		Last Modified: Tue, 23 Apr 2024 19:41:07 GMT  
		Size: 5.3 MB (5338500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e459e6e06a46001e1d069599391e1151722e53d20b2326475bc6cd02265f0d84`  
		Last Modified: Tue, 23 Apr 2024 19:41:06 GMT  
		Size: 35.3 KB (35305 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; 386

```console
$ docker pull redmine@sha256:e29778313dd24b9b847cef373db215d772d82e30ac515dac5e91c50a59cec639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182669296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6834fba05a8dd994d98ccdc2386de57efd14b351c73772bd36d35245d57839`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 29 May 2024 20:43:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV RAILS_ENV=production
# Wed, 29 May 2024 20:43:51 GMT
WORKDIR /usr/src/redmine
# Wed, 29 May 2024 20:43:51 GMT
ENV HOME=/home/redmine
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_VERSION=5.1.2
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 May 2024 20:43:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 May 2024 20:43:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 20:43:51 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 May 2024 20:43:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb08ac503ebcf4397d4fa11e0520a0938a3e976fc45f1d61f538e2ba6d9911a`  
		Last Modified: Wed, 22 May 2024 23:00:44 GMT  
		Size: 6.8 MB (6751140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f043e3055c861ca938580df08a0bfc51f14c7f372b61a210a1d19f50f50d79`  
		Last Modified: Wed, 22 May 2024 23:00:44 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d056aa172db88a373137c3b3b98420cb7fde198275cf4605dd131723a906385`  
		Last Modified: Wed, 22 May 2024 23:00:45 GMT  
		Size: 28.1 MB (28098911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6d1555cad442fc1af56fcf70ca34a042cf1c021ea06161d2705e258a9b0e12`  
		Last Modified: Wed, 22 May 2024 23:00:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83740c4bcd0fedbfe846a32d88fd6db25d7b4515861e205648b06227fcca226`  
		Last Modified: Thu, 30 May 2024 01:01:40 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2eb42aed7dc4776bc57915e350afa57fec259a8c81809d3194769227e95ca9`  
		Last Modified: Thu, 30 May 2024 01:06:37 GMT  
		Size: 70.2 MB (70193344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95643b68aeb9bd509cda10ee0f705171adbea82ee4d1a56dea09b16421acdd9c`  
		Last Modified: Thu, 30 May 2024 01:06:34 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94332aee84be63c3ae76686ebdb7cd58dd9ef286d60c357aae6581695909136`  
		Last Modified: Thu, 30 May 2024 01:06:34 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b417797fd367d2fc240d3fda24ae6555db44c77e1b06888eaf50ab5f14af971`  
		Last Modified: Thu, 30 May 2024 01:06:35 GMT  
		Size: 3.2 MB (3242995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d36f54cc757ab22689c096117ea2d8279b2dfddaf6397636d97c5f558d3522`  
		Last Modified: Thu, 30 May 2024 01:06:38 GMT  
		Size: 70.9 MB (70912190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc6a3d980d44144b46db1c2324d44fadb2d01634aed5a27ed47d63e134d025`  
		Last Modified: Thu, 30 May 2024 01:06:35 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:ebe62d6a07497cf108053514e228641922b4d199599b41e2e07dba3eb1f0e295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0c8796c56b36f7543419864e70609a4038d508c97461d655d3035bcb1506ea`

```dockerfile
```

-	Layers:
	-	`sha256:aced71ae3f0e3d90f764fd0363cac5d66e87896b8d03bd1f6ff111036ec0a532`  
		Last Modified: Thu, 30 May 2024 01:06:33 GMT  
		Size: 34.2 KB (34156 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; ppc64le

```console
$ docker pull redmine@sha256:07a73eb0e4bb8c5e15cbd77aee20e2b5c09d0625bb62c74483bac55b3b09edfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207537658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a859c5086442b265595e7794113aa7c570254798e038bf7ceec46cee163897d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV LANG=C.UTF-8
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_VERSION=3.2.4
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 04 Mar 2024 21:34:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:34:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["irb"]
# Mon, 04 Mar 2024 21:34:05 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV RAILS_ENV=production
# Mon, 04 Mar 2024 21:34:05 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
ENV HOME=/home/redmine
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_VERSION=5.1.2
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Mon, 04 Mar 2024 21:34:05 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Mar 2024 21:34:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Mar 2024 21:34:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Mar 2024 21:34:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:34:05 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Mar 2024 21:34:05 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c6ec9fb504c07d1c16c1b449d00bcc19cc9559e9f63e741d265c315636bea`  
		Last Modified: Sat, 16 Mar 2024 11:45:41 GMT  
		Size: 4.3 MB (4279192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f03c40289ce1a749a54c1b09ca1e696aa84b538250c4fe7a36474bb3e3ea06`  
		Last Modified: Sat, 16 Mar 2024 11:45:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d1b9e46c762a0cfa57794c331b5b6e95c451702d28589536de047939fef272`  
		Last Modified: Tue, 23 Apr 2024 17:54:47 GMT  
		Size: 31.4 MB (31386015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da2cb3e58f68e89746f7d5ad88ab8c95ab689a0b4bbc2939850e39d92feed3`  
		Last Modified: Tue, 23 Apr 2024 17:54:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49684402f6c531767ac5d72d7a856645ac98a9ef0b953f4ddd1b560cafda0bd8`  
		Last Modified: Tue, 23 Apr 2024 19:27:31 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a5ed65d4b83d537e7f11153334eeec03c60789cd035c7b1df2fd4866c5855d`  
		Last Modified: Tue, 23 Apr 2024 19:27:34 GMT  
		Size: 93.0 MB (92991128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3cd7a6f20cb79278b50a36bcf27073b601cbbee20102b29a2c4125d99d1c16`  
		Last Modified: Tue, 23 Apr 2024 19:27:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc77e83fa4ba478882f50e096025b79ae9319f4ae22efb58c93cdb103e0173c`  
		Last Modified: Tue, 23 Apr 2024 19:27:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca20dbe810714341e3a1f57cd248e663fdd721812f9dedd41c20649bf914ea9`  
		Last Modified: Tue, 23 Apr 2024 19:27:32 GMT  
		Size: 3.2 MB (3242912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744ef1da90bda5e2893611d8fe289aabfa11181c007ee3cbdd6bf470fc399e5`  
		Last Modified: Tue, 23 Apr 2024 19:27:35 GMT  
		Size: 72.3 MB (72286110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908a8089db74f75449569d6e1a00552d8f5a781754be30ff196535a8e3961169`  
		Last Modified: Tue, 23 Apr 2024 19:27:32 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:4650e1987bfe9ff0932be492447601f8a08ed66636b197fffe3205b0827cbc6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17655954e73ff40b468a68c705db7a3696d67d544989477b10dd40b015c2a9e1`

```dockerfile
```

-	Layers:
	-	`sha256:1f85b81653ab28ddf6681500712ac73fcbbde20028fd0e1cdf100d3153ceafd1`  
		Last Modified: Tue, 23 Apr 2024 19:27:31 GMT  
		Size: 5.3 MB (5344985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8275738f387ee3fba99a12f9d2dc6d44d7a8e16fb901564e0894c6c7805c17e4`  
		Last Modified: Tue, 23 Apr 2024 19:27:30 GMT  
		Size: 35.4 KB (35356 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine` - linux; s390x

```console
$ docker pull redmine@sha256:270a2e76e3c81772b953bd7db1cf9db33c32e03a96d9b124a804b22cdfdb54ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186289396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8379cb88147b27a2c4681b14c8398661757bc47253a791b7562d0dfdb73ac265`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_VERSION=3.2.4
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.4.tar.xz
# Wed, 22 May 2024 21:02:17 GMT
ENV RUBY_DOWNLOAD_SHA256=e7f1653d653232ec433472489a91afbc7433c9f760cc822defe7437c9d95791b
# Wed, 22 May 2024 21:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 May 2024 21:02:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 May 2024 21:02:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 21:02:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 May 2024 21:02:17 GMT
CMD ["irb"]
# Wed, 29 May 2024 20:43:51 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		su-exec 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV RAILS_ENV=production
# Wed, 29 May 2024 20:43:51 GMT
WORKDIR /usr/src/redmine
# Wed, 29 May 2024 20:43:51 GMT
ENV HOME=/home/redmine
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_VERSION=5.1.2
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.2.tar.gz
# Wed, 29 May 2024 20:43:51 GMT
ENV REDMINE_DOWNLOAD_SHA256=26c0ca0a9aaee1ceb983825bf1266c99b0850bf013c178713f5a3b0080012123
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Wed, 29 May 2024 20:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		su-exec redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	su-exec redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 29 May 2024 20:43:51 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 29 May 2024 20:43:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 20:43:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 20:43:51 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 29 May 2024 20:43:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe04587d67a77c068d15e0aae54bea82e27ce2196da5830bb733e1485199fe8`  
		Last Modified: Thu, 23 May 2024 03:23:09 GMT  
		Size: 7.1 MB (7063173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1781a16f232f5d025bb0b2e544a1826920fb8daec80f55ba678c7d7db6bdc4`  
		Last Modified: Thu, 23 May 2024 03:23:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565733c34c617aba5fb20e8d86b20d297e2e2bee12d185287cd0b4e9963722dc`  
		Last Modified: Thu, 23 May 2024 03:31:41 GMT  
		Size: 29.3 MB (29261564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193f98c2e7626bdf49c6f9f012f9ad50d03e50854b3b8461f6c8cada54e79bb`  
		Last Modified: Thu, 23 May 2024 03:31:40 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30e33bff809c7e03c2481d16243a678db81c606fb8db0a7002750d5495cd50b`  
		Last Modified: Thu, 30 May 2024 01:55:28 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe50430b5565b510d6710763021e39981f68421a59bee78a46df675369a4b85a`  
		Last Modified: Thu, 30 May 2024 01:55:31 GMT  
		Size: 71.3 MB (71300842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d685fe2260a562e456ee730691b7fa9f8ce7b98d88c16b63916a5891382b3e3a`  
		Last Modified: Thu, 30 May 2024 01:55:28 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580513526b82627dc63a74ab28b841a5adc563981b924f64b441d8cfc2e623f`  
		Last Modified: Thu, 30 May 2024 01:55:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c371c9723b980c77f17f0df3e1a7f2f185037eb3bfa922d993eccd856480db7d`  
		Last Modified: Thu, 30 May 2024 01:55:29 GMT  
		Size: 3.2 MB (3242965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b59cbb09a7e5e4faa5ee2894c45785f3fd06bc66e71cad81f6306dd5ec4d1c`  
		Last Modified: Thu, 30 May 2024 01:55:31 GMT  
		Size: 72.0 MB (71956979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbabba0e2dc6c5bdb9a17253f257f1189312139de856459ac8b1f5475937530a`  
		Last Modified: Thu, 30 May 2024 01:55:29 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine` - unknown; unknown

```console
$ docker pull redmine@sha256:288c996cb4452e7227abee20de90bfd578c324a3944633e006340ff4bd2d5456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f1123586cd45bca394cd0b46f1de3d025cb635c5e2341f7e302c964368ebfe`

```dockerfile
```

-	Layers:
	-	`sha256:dc9e09dd5229a6500864df18ce85a3fa9c87a75ebc80fa22f0e3d12182e20e47`  
		Last Modified: Thu, 30 May 2024 01:55:28 GMT  
		Size: 34.3 KB (34264 bytes)  
		MIME: application/vnd.in-toto+json
