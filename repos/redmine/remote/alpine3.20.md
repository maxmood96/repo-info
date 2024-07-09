## `redmine:alpine3.20`

```console
$ docker pull redmine@sha256:cec4ed667f191a33e485ca1d082dbe53590cadcae3072c883393adb249719268
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

### `redmine:alpine3.20` - linux; amd64

```console
$ docker pull redmine@sha256:6a18b604d9855976de53fbd8c8bda9ff721fef1d17cbb02f7d037840812dc04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187240778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdaf64c4909ccb3827b71727aa4737df6b20bd83502542cfe2a2779aa065ff0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 21:02:17 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Wed, 22 May 2024 21:02:17 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae1125194a30668333718edaca9f40ae5f9f9ddeb9ff2af91c4b2d0c3bffdf0`  
		Last Modified: Thu, 20 Jun 2024 21:00:03 GMT  
		Size: 6.7 MB (6686055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7293d14d6f0c470da9e028e86cf7160b517ed12faa7d56c568a33a395e9d23`  
		Last Modified: Thu, 20 Jun 2024 21:00:02 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c660f09fe418600bdce450c2bd74bcd9a171b8416951ae7fe920d326ff1b7872`  
		Last Modified: Thu, 20 Jun 2024 21:00:03 GMT  
		Size: 32.1 MB (32104581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1593045cd65ddfc3faced122b87bda8052867a5b2448b60794480ac6281ab1c0`  
		Last Modified: Thu, 20 Jun 2024 21:00:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c024030876c91dd09d3d2ca0efe22eae9f530b17beaaa6242f8538868120c3`  
		Last Modified: Mon, 24 Jun 2024 23:00:08 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b97597b0db2c6a707a9b6abf3cef9e56e1f16c0261265684f071b2e3d45022e`  
		Last Modified: Mon, 24 Jun 2024 23:00:09 GMT  
		Size: 69.6 MB (69605261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd5c6b76b03ba4388cbee263ee2d3fa34dfdb77035c863a390095113bfb116`  
		Last Modified: Mon, 24 Jun 2024 23:00:08 GMT  
		Size: 1.2 MB (1195323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6697c79723501055d94d15545342159a77768e6939ba37923cdf5e7717932a2`  
		Last Modified: Mon, 24 Jun 2024 23:00:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a798fd8e0ead3d3f6a3f18d5497d1aec05de57ef0066ae4058c61f7b882432`  
		Last Modified: Mon, 24 Jun 2024 23:00:08 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c87988a5218c5e6ac4c41dce7f3260364b9dde7985bc625733ab954fa3f8fd`  
		Last Modified: Mon, 24 Jun 2024 22:59:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743f8578996ad58e3572880b63ba3dd93516583bdc363a72a41f3ae90ebd97fa`  
		Last Modified: Mon, 24 Jun 2024 23:00:09 GMT  
		Size: 3.2 MB (3244012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715bb2631a3c3d68ec9ff665f1e8c8229b3d57f8d3ac10ec42ba42f56e220f1`  
		Last Modified: Mon, 24 Jun 2024 23:00:10 GMT  
		Size: 70.8 MB (70777992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b56d193661292c97e98e9351fc86905590e6da17a7cc50e11f6b7236f440a2`  
		Last Modified: Mon, 24 Jun 2024 22:58:48 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:8795650a65c51941566eb4486b1c740af08be839f1f17b2e20ca0e52a7bac79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee756b8f72b82d3b6629fb9f4b296af073a644ed486483d8ab2281c7c10f7e4`

```dockerfile
```

-	Layers:
	-	`sha256:4b609e828048e98b7fc8bb09db96d2816ebfa09a78df6f9f46bb689fd5ff6eef`  
		Last Modified: Mon, 24 Jun 2024 23:00:07 GMT  
		Size: 43.4 KB (43394 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm variant v6

```console
$ docker pull redmine@sha256:ee44fa878a6a89173f45c45b7ec49f22b7c239de4708dd353489c20799a3aa98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181523783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d1a6860d870e158e006399cad164af72a308fec4e83ac5a6a9cd2d2f90c287`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 21:02:17 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Wed, 22 May 2024 21:02:17 GMT
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57b3cf00bb4d0f3ebe9aa2c55b2ec958316da1df5b1fe170a5c145f225f8ded`  
		Last Modified: Fri, 21 Jun 2024 05:01:09 GMT  
		Size: 6.5 MB (6533793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e78e55e8ab15611535f1d0d522c1e6ba3d803ae390f07781dd5ec8e4ae33e42`  
		Last Modified: Fri, 21 Jun 2024 05:01:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46866868b2245b678e2f6485e4c861ea6bdf78ead22a95db9110d47a19984ccb`  
		Last Modified: Fri, 21 Jun 2024 05:12:30 GMT  
		Size: 28.2 MB (28244129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db156915fa090a3c7f2c284a32e874c75c793d09404a15253ea9da7a6f220f0`  
		Last Modified: Fri, 21 Jun 2024 05:12:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831e421e41b92477c037dac6a38a55d80b805c20874a54ef45f9a35ad75d5315`  
		Last Modified: Mon, 24 Jun 2024 23:48:06 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a403e189c2935ae3eeb4775b65c9065f103c4febcadf313846df7ed7088c4b`  
		Last Modified: Mon, 24 Jun 2024 23:48:09 GMT  
		Size: 68.8 MB (68848350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d922173f2d75188546c83c05c6275eadfc901f24871d772c698ca213f4147a`  
		Last Modified: Mon, 24 Jun 2024 23:48:07 GMT  
		Size: 1.2 MB (1162084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a73d09b6a85c323f29d5fdb1db7ed46baf032e29d3de461cc36731e9c29c13`  
		Last Modified: Mon, 24 Jun 2024 23:48:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e64d0dd01aab0085d1afff155d81010679519db45fcb5e5da5b72ea0809995`  
		Last Modified: Mon, 24 Jun 2024 23:48:07 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72ae3e6795766cbd17c570c1ce4e4f97f6145a5146091deacb7c2540065afa`  
		Last Modified: Mon, 24 Jun 2024 23:48:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc03dc4ae3122431052a4941c92bb1aa7c2794f2eb90d3d3c00e70a4061bd75`  
		Last Modified: Mon, 24 Jun 2024 23:48:08 GMT  
		Size: 3.2 MB (3243943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f9ee7502ff565557aa270ffbe74e4ec40298a3e9ab5e6209d5aed6127aae7`  
		Last Modified: Mon, 24 Jun 2024 23:48:11 GMT  
		Size: 70.1 MB (70120625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1585bb6049a6a76e25f64f0e5a241b4c92a202080e7f018f7f0dce6d03a9d6`  
		Last Modified: Mon, 24 Jun 2024 23:48:08 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:30884b94031f90474af296a3af05ce6bb8ccd0a561a3f9de441a2bf13d372f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b630c9a1e62bbb17d90fad43239f8fd5c3e41c2b4f42095c55646493961aed`

```dockerfile
```

-	Layers:
	-	`sha256:edfe35a15fb3725dd302c92230ca1d6118c733531a5cd8fb7aef292999d659fd`  
		Last Modified: Mon, 24 Jun 2024 23:48:06 GMT  
		Size: 43.6 KB (43639 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm variant v7

```console
$ docker pull redmine@sha256:f53dc40d45a3aecf4c788a04cc0babc76396f67c774a388a984641a9cd2ae3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177109264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafafe7566c40336a1ed539df367e5c13f17899a9698ccffee53e80cf8179f80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 21:02:17 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Wed, 22 May 2024 21:02:17 GMT
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0239873a8680b2dd07d6128919f96fa2f55d7494a468ee097fba5ba6bf65f1d6`  
		Last Modified: Fri, 21 Jun 2024 04:50:21 GMT  
		Size: 6.4 MB (6377929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1c76c0a287f598726c03f232330ba1cc7b75c20061e244cca7aabbd27bd523`  
		Last Modified: Fri, 21 Jun 2024 04:50:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a325889c4f196d2e23d4b5282b27e260a2fc3bc55d7aa716e8a3492c10963`  
		Last Modified: Fri, 21 Jun 2024 05:01:54 GMT  
		Size: 28.1 MB (28118646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84aa4e78aa723458daaaa36904ebeca6902291def102f2812aa909ea5272988`  
		Last Modified: Fri, 21 Jun 2024 05:01:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed1b2df9a4196dab5618ea4d66f668c8ae0690a01f5436f89154c48adf4f425`  
		Last Modified: Tue, 25 Jun 2024 00:16:37 GMT  
		Size: 924.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4f75bb0ebf4f03f6b1b59af5e8cfd73c8b55463e14ceeda031f173bc9f5da3`  
		Last Modified: Tue, 25 Jun 2024 00:16:44 GMT  
		Size: 66.0 MB (66002845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04253481242a4264c99c07a34c24a611bf4b85715ddf44c0508a1feff6a61a5`  
		Last Modified: Tue, 25 Jun 2024 00:16:38 GMT  
		Size: 1.2 MB (1162096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c5343fd738427080d389c92fb612f028d5d60506d529df1e1877fbd8e2045b`  
		Last Modified: Tue, 25 Jun 2024 00:16:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516e6874d3569aa3f58a574cf73a69cbbae83d3399c4400a789459cae11b9cd3`  
		Last Modified: Tue, 25 Jun 2024 00:16:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38466a991c255f5529638cbb7a217eadb06bb4d9d457e6eb74446066d24a2a2e`  
		Last Modified: Tue, 25 Jun 2024 00:16:38 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f99d48f8d15139bf796bb86c4c9c69597960e07d809b5635ac3a09fa7587a3a`  
		Last Modified: Tue, 25 Jun 2024 00:16:39 GMT  
		Size: 3.2 MB (3243991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e962ca22725573c6fd6915d99118f09eeb1488bf7642cc543a3eee4e24b9de`  
		Last Modified: Tue, 25 Jun 2024 00:16:42 GMT  
		Size: 69.1 MB (69105194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09290ae309c739c2713a3d64719d2a457bb2978bbcac5209f9df295475e52904`  
		Last Modified: Tue, 25 Jun 2024 00:16:40 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:ef02bf65c284d7f6a716368e098fc406a75bc37af92ee79c5822ff67de321186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf77166576405485c6a40f8341ad74b38cfc1418d5db769f059bcf8a9880da5`

```dockerfile
```

-	Layers:
	-	`sha256:ac853373be620d308fab846e735de6696bf55fa6fb383465e62c7fdbc11e7da9`  
		Last Modified: Tue, 25 Jun 2024 00:16:37 GMT  
		Size: 43.6 KB (43641 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:fc3990516cdf6e8dc1ab1e6e5fd7d896f180a12173424e28b2aba84cf5c290d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188344967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c2bb80e67f412147fd55cf41962fbcf58d80c8fc003e415a417323d1eee5bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 21:02:17 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Wed, 22 May 2024 21:02:17 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f659b8850f5f4bec7d7d3c580cd0db8beb1e8379eca4fad658ebfd259b99b5`  
		Last Modified: Fri, 21 Jun 2024 06:30:19 GMT  
		Size: 6.8 MB (6752310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3180c4dd2ce07d0a20d5da66bcc4e514ad02ed1d2ffff7a71178e155f719f4df`  
		Last Modified: Fri, 21 Jun 2024 06:30:18 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe2b8b2599300a79149548f0ec8e6f84d5e87da775c0a722da3c17b10fcf302`  
		Last Modified: Fri, 21 Jun 2024 06:40:48 GMT  
		Size: 32.2 MB (32169212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f751e6d26d3961a7e15584e1729048a02101d9681181fce2f492c016a3d2308d`  
		Last Modified: Fri, 21 Jun 2024 06:40:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad17b35afcfe24403bfaee16aa16051a95a578c666c5a0f86cd2a8d708ae5acc`  
		Last Modified: Mon, 24 Jun 2024 23:15:37 GMT  
		Size: 927.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8385c5e1b3be9c267e43c1514641b2d4f0f623682142aba3944ac848b26787d9`  
		Last Modified: Mon, 24 Jun 2024 23:15:40 GMT  
		Size: 70.1 MB (70105255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73816136bd3bfccce68e9d0218a420ec3918e75a75a68c40545aab3916f9f5d8`  
		Last Modified: Mon, 24 Jun 2024 23:15:38 GMT  
		Size: 1.1 MB (1121079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c694dbb4290e69f51583fe7ffaa48272d070a45850a6b982494e06c3609116f7`  
		Last Modified: Mon, 24 Jun 2024 23:15:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72aff879f880b4d097b44c71e7b684b9c2f76f8aede33ddcee61b1fd4b60045`  
		Last Modified: Mon, 24 Jun 2024 23:15:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153527ca4453d052d7e6c6d6cdce6abe17e11e676bb5e92f11b57f0440ea1b4`  
		Last Modified: Mon, 24 Jun 2024 23:15:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a067596bea9e28869a5c5cee9a2f1d7fd24782cb0c799e9f2c797ffea09540`  
		Last Modified: Mon, 24 Jun 2024 23:15:39 GMT  
		Size: 3.2 MB (3243997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73555538c867ad7517da0c78385d5c299e86e9f674976fbe96ae591b5b25dab1`  
		Last Modified: Mon, 24 Jun 2024 23:15:44 GMT  
		Size: 70.9 MB (70860603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4a2d093002b00a0924e005c6247ed788f9da3767cc632575553050d6d06371`  
		Last Modified: Mon, 24 Jun 2024 23:15:39 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:b0787a08e351b616132dda33da9b82d80b7880b71c5279e229b627c22327fa0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 KB (43887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784cfd0778b2293b4b24c953db98cfcb33d47734a43e9d9a3187a39550e37e18`

```dockerfile
```

-	Layers:
	-	`sha256:7e14ac57533adc72c4e16a2f1d3dd492acce43ac9bf673ff31d3ce95f8543eb3`  
		Last Modified: Mon, 24 Jun 2024 23:15:37 GMT  
		Size: 43.9 KB (43887 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; 386

```console
$ docker pull redmine@sha256:f9ad0a18939cee7ed8a425ddb49e75095bc8053bbdfd67fbff34af15cb48bb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185514093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ebcdd3a55cf6d27f53e16670284132af6fa32762c0e9065f31c1b0a5a59ac9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 18 Jun 2024 22:07:17 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038afae98d67a59d1e161e01f7017950baac692f0072cab79c9da82c00b4be6`  
		Last Modified: Tue, 09 Jul 2024 19:02:03 GMT  
		Size: 6.7 MB (6749356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2847ded55e0d1c4400d719aa44231fd1e8afed61f9255a41b43d285a327b71`  
		Last Modified: Tue, 09 Jul 2024 19:01:57 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe116fb29691e17829eee94b50f8bc6b6953c7db06c877671d04ae15635065d`  
		Last Modified: Tue, 09 Jul 2024 19:02:03 GMT  
		Size: 30.3 MB (30341466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02c433f0b12317b4dc31323081efcabbe4d343756c6063e1de49e5ebf42c787`  
		Last Modified: Tue, 09 Jul 2024 19:02:03 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b19e39c36e0c857d5dc2c2d7c85b4b42c56803da578c7775f78e6203a1da88b`  
		Last Modified: Tue, 09 Jul 2024 19:54:53 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c0e6c6cbcefb5f745d0b2665de748adfe320df5283987b9e7c62d08a62eab5`  
		Last Modified: Tue, 09 Jul 2024 19:54:55 GMT  
		Size: 69.6 MB (69620005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6392549fec9b4b03639b9cd5b508b359c63c7f5ed956285c9a5e1893e7acc3`  
		Last Modified: Tue, 09 Jul 2024 19:54:53 GMT  
		Size: 1.2 MB (1170756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947c8030b8aa08f34a94b6f1375ca4bed69899bedf22b0fd3f8b17e561dfa328`  
		Last Modified: Tue, 09 Jul 2024 19:54:53 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa85a3eee22ad2a2e9e71219f9d554cfcf4ef637493dddc8651d172fc284d95`  
		Last Modified: Tue, 09 Jul 2024 19:54:54 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8859a532c2efb0ae62164a9383b44437674f8bfa000198d2bfddc7b8e9e63a`  
		Last Modified: Tue, 09 Jul 2024 19:54:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a589b22b05024628cd7ca52f276bd6eeacc88f6d710fac180f6a8aecd17bbd3e`  
		Last Modified: Tue, 09 Jul 2024 19:54:55 GMT  
		Size: 3.2 MB (3244026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c1308b65ba9e2b9c098dd14438920cf2beae62d41bd0fe1a130be5daaffa1b`  
		Last Modified: Tue, 09 Jul 2024 19:54:57 GMT  
		Size: 70.9 MB (70915309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56be572d165677377c227eb23b8a666010e1636d71c1e953c3d1a720e5c491a`  
		Last Modified: Tue, 09 Jul 2024 19:54:21 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:39d52717485ec2b61f224f1d073bd58425c84281a3cd8a5546496261f21a65ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 KB (43330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33ef4fad8b1f0096a432301d590a6480529e7ed7b39172540466051d762b387`

```dockerfile
```

-	Layers:
	-	`sha256:09a04b458c95e9a9c52e44d89b28c16e7f4637ccad69c9e6d875ef49136655c7`  
		Last Modified: Tue, 09 Jul 2024 19:54:53 GMT  
		Size: 43.3 KB (43330 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; ppc64le

```console
$ docker pull redmine@sha256:4d821f05e4e8d9d97e8f57822c8b6192b2d4dd1e994e80aa74635ae46eb2b203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188175656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f4e6a8084b609f20337d6cb556a4c2eee7149b7e491e8267eebd6007692ce5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 21:02:17 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Wed, 22 May 2024 21:02:17 GMT
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
	-	`sha256:d26518361dced19e8d2c5e6372987cd9370cefefb5183b4df9e332a8d2940ba1`  
		Last Modified: Fri, 21 Jun 2024 02:58:15 GMT  
		Size: 6.9 MB (6913049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9302f743f488b2d353f6a4911a5a91a857d0533e85f1f416d5d20e4802a41c7`  
		Last Modified: Fri, 21 Jun 2024 02:58:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b524125848e7b3c4a4bd8613d2a3f6e442564fc4313ffe3f5d48af20d0403c00`  
		Last Modified: Fri, 21 Jun 2024 03:09:46 GMT  
		Size: 29.4 MB (29409001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0974543bd6b4c07b13deb9edbb0a6a9ddd26a361ea589b3f3fa566e6f613977a`  
		Last Modified: Fri, 21 Jun 2024 03:09:45 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05373d304abebbe40c2a05a26ada3ccdfda57fea5e8b9eb3f16d4d2c0ec5c969`  
		Last Modified: Mon, 24 Jun 2024 23:24:04 GMT  
		Size: 925.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fa8927f5dc67944989f8d180a1234515cc3aaa221bc17de72da3dd6275b26b`  
		Last Modified: Mon, 24 Jun 2024 23:24:07 GMT  
		Size: 71.2 MB (71209045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bb2dd6047ae54d2da94dd95678d2c4dc0d2147974fa8eecb86ba6a705e57c1`  
		Last Modified: Mon, 24 Jun 2024 23:24:05 GMT  
		Size: 1.1 MB (1111560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bab737a1964e24b33fae113acf867ed28539d0deac96bc4117735d334f9060`  
		Last Modified: Mon, 24 Jun 2024 23:24:04 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd59c63f364ab5c3dadbaa3c6463a642fcfa8b9cc71ec744c20f8e30bac6eb5`  
		Last Modified: Mon, 24 Jun 2024 23:24:05 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bd2a2efe60016f2a3f4572654034690eaa54f8fd60e1b7dffce43a440a8d8a`  
		Last Modified: Mon, 24 Jun 2024 23:24:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916fa527c1d46acc1d0a0704970dedd0b0ce78d724bac8708e4d30aab1298b81`  
		Last Modified: Mon, 24 Jun 2024 23:24:06 GMT  
		Size: 3.2 MB (3243943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca22e893326807a833991b3ea94758e38fbd9670b7f28e3febec2c9da7c1b57`  
		Last Modified: Mon, 24 Jun 2024 23:24:09 GMT  
		Size: 72.7 MB (72713648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ef794b1048d665ecf9e87f2983cb1b6493f5e0ab7cec1d150a5e968b9be90f`  
		Last Modified: Mon, 24 Jun 2024 23:24:06 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:0cb7022ac0d6ca2b72668c6fc6adeb0ab7a02b416a3f71a622ebac8e2b6fc230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 KB (43535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677322c295b48dcdc840133e78eac6270f73d65c4a909bb61372fafe82b8093f`

```dockerfile
```

-	Layers:
	-	`sha256:bd43ec8ea8195362421e9f4a251f1255a56287177f2e5079f48e5e6dc9f8bc31`  
		Last Modified: Mon, 24 Jun 2024 23:24:04 GMT  
		Size: 43.5 KB (43535 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; riscv64

```console
$ docker pull redmine@sha256:0b55808c8b9c007aae492034618cb6d2f1b9de306807118572f2e37eb8b87050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186183841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dceeb7228a369fb902832c9e50ec273313ad7319b60131e437cf9701e900a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 21:02:17 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Wed, 22 May 2024 21:02:17 GMT
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b05d3238fd29573005023f78c6c9f003e0ef5b5e5db34bbcc4bf6408de8cfa8`  
		Last Modified: Fri, 21 Jun 2024 16:31:00 GMT  
		Size: 6.9 MB (6947827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e5b2af786e9ec5a823fcf63759846ef4324c85763c6f2ba8e9db009e716c4`  
		Last Modified: Fri, 21 Jun 2024 16:30:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139decb9780011a4be717074aeb4c90fe326e35bcb4e26e615ffd869d1005f24`  
		Last Modified: Fri, 21 Jun 2024 18:56:52 GMT  
		Size: 27.3 MB (27330552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d18739d6da47c443cba56b6e0b0b12c5cc6d642f5ef952d83f997f1d2b1406`  
		Last Modified: Fri, 21 Jun 2024 18:56:48 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2260754e085a985f7eb1e9e2b266d5d21f1b8b982e6f08d78a637c4845a931`  
		Last Modified: Tue, 25 Jun 2024 00:05:36 GMT  
		Size: 923.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e5e00bfb6e8487ec3391f34bdb408457357f85a3a868233e86fa411ca18f8b`  
		Last Modified: Tue, 25 Jun 2024 00:05:46 GMT  
		Size: 69.9 MB (69936632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4200b20a37f851c932869f70125dfd95cf3d55e8229a3829e1ab72d431a50448`  
		Last Modified: Tue, 25 Jun 2024 00:05:36 GMT  
		Size: 1.2 MB (1163714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37a8206d48d467274bd303f56483c8b356aebce1a45ddc608fdb0b5c2524180`  
		Last Modified: Tue, 25 Jun 2024 00:05:36 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e223713494d3d0a43fa38a43d22b32e09a32b9b68c55641beb5c80d4cb985744`  
		Last Modified: Tue, 25 Jun 2024 00:05:37 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a7d3a3f17a2f1d2a82bc3d07448948fe11919ff4b6909cb09373ba934ae16d`  
		Last Modified: Tue, 25 Jun 2024 00:05:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4b16354e3e0d32d62e053daf5584ae50c841740177e2451202d67a347d19c5`  
		Last Modified: Tue, 25 Jun 2024 00:05:38 GMT  
		Size: 3.2 MB (3244051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f722de35a4f47866eb19749f61ce8794db4477e5389c739b1fedc82544c046`  
		Last Modified: Tue, 25 Jun 2024 00:05:49 GMT  
		Size: 74.2 MB (74186313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443f7a8950f5fd38cf154999ed39b6a40e3daee8eb5c920067b2eb11acc33ac3`  
		Last Modified: Tue, 25 Jun 2024 00:05:38 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:c154491f38b1042beb4d6a58616d7e6486b8c6623f133237f00b7e29a5de5564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 KB (43535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48eccaf60b2ecada9d30c2d96aefbfd4c96607ba70595cff374a015119f0f427`

```dockerfile
```

-	Layers:
	-	`sha256:d938817a19e301a9391b3a98bd6214fadb638f2276e4cac2bd1b4e8527110c6c`  
		Last Modified: Tue, 25 Jun 2024 00:05:35 GMT  
		Size: 43.5 KB (43535 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.20` - linux; s390x

```console
$ docker pull redmine@sha256:787102d6194a46b7d95a1ba6589a856840755406b91d5f7460c542b78a426c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187433216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724ab3aa6bfe40716f91d366de01c40b879035479d795c8103021325f5b68b1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 22 May 2024 21:02:17 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Wed, 22 May 2024 21:02:17 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0eef10a64a8b21e03490ef94a6cabb8e653ac9958688cbb38479d42f08e38f8`  
		Last Modified: Fri, 21 Jun 2024 05:43:46 GMT  
		Size: 7.1 MB (7063151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3901955a16f71f82b20e7f5e22c65d2dfd7c52937c48f4577cea7874b477ba0`  
		Last Modified: Fri, 21 Jun 2024 05:43:44 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abad595f37c8bfc2cb7b29d5cc2a63c14e87d08a6822c1cdc3cd3b6e1b4f53c2`  
		Last Modified: Fri, 21 Jun 2024 05:56:12 GMT  
		Size: 29.3 MB (29261608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b59c096f34349ad219d48605f622eef16739b1e195f852c46edb8d9e3784d`  
		Last Modified: Fri, 21 Jun 2024 05:56:12 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf913aedf961b863dc04216d74b105906b6656ef280587f1b077e0e96ad6f979`  
		Last Modified: Mon, 24 Jun 2024 23:43:36 GMT  
		Size: 926.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66827448c2681ddbc8ba7e95b65403c3efa06fc8e9ec2446a56b3d26ff12c17f`  
		Last Modified: Mon, 24 Jun 2024 23:43:38 GMT  
		Size: 71.3 MB (71288155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea67896517bd87e9affcebcf5bb9516126337aa27c6804a99132cd5f6c51a3e`  
		Last Modified: Mon, 24 Jun 2024 23:43:37 GMT  
		Size: 1.2 MB (1160296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f660f7742ee26bec465dcb5a30be99dc7e602d94305e8ab1c2b65585f4abb76`  
		Last Modified: Mon, 24 Jun 2024 23:43:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d4ce1e80d8bb5978b7fdf1e35aac0c726782db89e242ee04ff4630a6941112`  
		Last Modified: Mon, 24 Jun 2024 23:43:38 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76bac1d9d3766082314a46068252bc50e36315bb31b42557bab48ee10f0fc9e`  
		Last Modified: Mon, 24 Jun 2024 23:43:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcce02d5e2fd1b19379e92e066f6aaf7314b2d871de71496077e006c5d649296`  
		Last Modified: Mon, 24 Jun 2024 23:43:38 GMT  
		Size: 3.2 MB (3243885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034823a7bdad004e2f139dd8bb98b418225234bda1ec590f899c39b79042605a`  
		Last Modified: Mon, 24 Jun 2024 23:43:40 GMT  
		Size: 72.0 MB (71950556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952af843edbb760b2ce8d148bc71681f58ac9c382683205cc0a2c2a2e045df55`  
		Last Modified: Mon, 24 Jun 2024 23:43:38 GMT  
		Size: 2.0 KB (2011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.20` - unknown; unknown

```console
$ docker pull redmine@sha256:a4472bf67179bf22d6f5f928d1065a2d44e664feb28bd6a5966a26381f58a678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 KB (43455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033da14af6a4d8993fa2a4a842c4a4a98d9042b443a1302cdeedabce6a18cd22`

```dockerfile
```

-	Layers:
	-	`sha256:9f979b02499256f44ae747145b7e39cd62376b7bd07852f5367f09e36a174682`  
		Last Modified: Mon, 24 Jun 2024 23:43:37 GMT  
		Size: 43.5 KB (43455 bytes)  
		MIME: application/vnd.in-toto+json
