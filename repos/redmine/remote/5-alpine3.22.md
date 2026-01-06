## `redmine:5-alpine3.22`

```console
$ docker pull redmine@sha256:5d0e1464b21d2148e0f04f85b850ac21e59026f3e174ac16e92456b436f00813
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

### `redmine:5-alpine3.22` - linux; amd64

```console
$ docker pull redmine@sha256:476ad57e5dcfdbef31c1d45095f404daa2bcc85192bdf339d546751c963a386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188445276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1147df8c0d3c18e7dca126fef819e9b735fce9213e2744c24ed95beff1d7873f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 19:59:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:01:57 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:01:57 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:01:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:01:57 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:01:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:01:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:01:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:01:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:01:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:01:57 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:28:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:28:59 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:29:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:29:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:29:01 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:29:01 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:29:01 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:29:01 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:29:02 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:29:02 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:29:02 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:29:02 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:29:02 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:29:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:29:04 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:30:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:30:45 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:30:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:30:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:30:45 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:30:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893a1e5ed91b36006dcebdd68804b7614effce1162b60813073363c36e086f75`  
		Last Modified: Tue, 09 Dec 2025 20:02:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7eb05d21f171e68b607fe7ff6c3955384e9dbff735a59496343b35d26d6473f`  
		Last Modified: Tue, 09 Dec 2025 20:02:17 GMT  
		Size: 33.9 MB (33871526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96807a7edf84b580d29d9f1d591405e1984bcf2ba7ffe28a1ca036c4f122dfc`  
		Last Modified: Tue, 09 Dec 2025 20:02:11 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a80f96b6f9ec5ff96bc1f846713a6184fbb60913b764558cf080aa56a3e6e90`  
		Last Modified: Tue, 06 Jan 2026 18:31:07 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ef4a2d27f6890da6f94fb2334d454f5ac8a0ce7e45495aa6cd295656dc45c1`  
		Last Modified: Tue, 06 Jan 2026 18:31:12 GMT  
		Size: 75.1 MB (75099966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80e0013b6bc22f4451788c5b7525ee82674ebc317755d818d65b5f1ec3da45f`  
		Last Modified: Tue, 06 Jan 2026 18:31:07 GMT  
		Size: 966.7 KB (966697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1fc3cab10268dfffb1ef671aa9d7abd4b570c8e9e6ca1b07a24c21053d5162`  
		Last Modified: Tue, 06 Jan 2026 18:31:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7762621b1b8782c7a99a94c95fdda83795856546a5b0d629878f9521d86a1538`  
		Last Modified: Tue, 06 Jan 2026 18:31:07 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0497255d462b36b37be23aa344a2df2234314662c32d19e5708bd83743c405c5`  
		Last Modified: Tue, 06 Jan 2026 18:31:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2a6322e74a3ac992e1e3f74bc76a483331186baccd8a080fb8c1050a84563d`  
		Last Modified: Tue, 06 Jan 2026 18:31:07 GMT  
		Size: 3.3 MB (3254010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebb841e3c79e0a95490ca484cc197bd1c755946f4a61bab42b05083f17ca0b3`  
		Last Modified: Tue, 06 Jan 2026 18:31:13 GMT  
		Size: 71.4 MB (71446539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1be52ee2e869132a7657c5cc749c862124bb9237231187297a0e16f830c0d`  
		Last Modified: Tue, 06 Jan 2026 18:31:07 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:46cf2b0fa238f1fafa9318255d6a62f067cfc2d4de17b0fa56369f30b0f79e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e9f17a9e6faff9eb3e79ce6c1cfa547e7b92b0b34ca627a44b371ea67bd149`

```dockerfile
```

-	Layers:
	-	`sha256:7e82d385ad82e9227db46e480f2193a05e329f83d370b4e5299f783b0b82dc2f`  
		Last Modified: Tue, 06 Jan 2026 20:51:36 GMT  
		Size: 39.8 KB (39847 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; arm variant v6

```console
$ docker pull redmine@sha256:3c4fac2aa137156e0f76660d8d8b03587414cee9c0920b2c89669a42024f042c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180339863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddbc91924ec0e100d04b2f66bd42a5bff9db4cd8c09a8c5c89df9236ec21fc9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 20:00:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:02:42 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:02:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:02:42 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:02:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:02:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:02:43 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:02:43 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:30:18 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:30:23 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:30:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:30:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:30:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:30:25 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:30:25 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:30:25 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:30:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:30:25 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:30:25 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:30:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:30:25 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:30:27 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:30:27 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:33:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:33:03 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:33:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:33:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:33:03 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:33:03 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7bc0dc32e2f1b0ab5c2ddd4b221a66016b3cef2eae703f6cf00ed1f55495a2`  
		Last Modified: Tue, 09 Dec 2025 20:02:55 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579bd816ac502e312f993613e1c08450854985e586b460b10f4444d69be0e3fe`  
		Last Modified: Tue, 09 Dec 2025 20:03:01 GMT  
		Size: 30.1 MB (30078328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a09a58bde5447625e4a2cbba2e04d11b8bc451b81ce82e1754c972c5d9cf4`  
		Last Modified: Tue, 09 Dec 2025 20:02:55 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5100f1d6cf5d75293790885a3fd20736914b71055f1535c54d47af656b2d1520`  
		Last Modified: Tue, 06 Jan 2026 18:33:24 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d8216a5d1d46e769342bc9d0548c2998660746bb09ecb003100918ab34cb0`  
		Last Modified: Tue, 06 Jan 2026 18:33:30 GMT  
		Size: 71.9 MB (71910663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c36c7c4ca1ee05cca563be51b6a02642498a723e6ad1804ce04b94f2da1834`  
		Last Modified: Tue, 06 Jan 2026 18:33:24 GMT  
		Size: 934.7 KB (934703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4307bef1ce661ccb9c082d2dd0cee78a4fb8ee1892d1c8235e9e17b997ff4167`  
		Last Modified: Tue, 06 Jan 2026 18:33:24 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bf17fa92e92f7c2ebac70e2f3cb89ed38b44e42f370fd6affc72846552b582`  
		Last Modified: Tue, 06 Jan 2026 18:33:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e802088c2a2b9d1434c6c678601d1383306822f592db07b8171ed1bfc8552e7e`  
		Last Modified: Tue, 06 Jan 2026 18:33:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02e38d754120ffcf913daff3a3990c0e00fee467b5b7ba6e0611c49b65040d5`  
		Last Modified: Tue, 06 Jan 2026 18:33:24 GMT  
		Size: 3.3 MB (3254013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7451a06f831f720b7730f65751cbd08a2e3892ac7e419ce544c164aa34503af`  
		Last Modified: Tue, 06 Jan 2026 18:33:31 GMT  
		Size: 70.7 MB (70653982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4f307c9334362c9426449cbf9bcb44dfc62a89a9b90c8daa1c65910bd4effb`  
		Last Modified: Tue, 06 Jan 2026 18:33:24 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:9bbf3bbcebc046503bb9df2c8d2fe0120fb6b7ef6772a1749c33c0d120ab64b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 KB (39997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd0e60d9efb396cd966e43e5e764eb6349e612b2b2cf02de6ed79fca28d68b2`

```dockerfile
```

-	Layers:
	-	`sha256:c09e9338d87d22457c1fc3b4caf74e97c7cfe0e6fadac02001a6e9260132695d`  
		Last Modified: Tue, 06 Jan 2026 20:51:40 GMT  
		Size: 40.0 KB (39997 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; arm variant v7

```console
$ docker pull redmine@sha256:69bdaddfe6c3728aa34ae7ef493164506b215567a36905656e3d47652eff8249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175779629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8593c051c99f6e6fd005c4351d49ad245309a0a83997e06232610ff0b8cfdca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 20:07:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:09:02 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:09:02 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:09:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:09:02 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:09:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:09:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:09:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:09:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:09:02 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:09:02 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:29:18 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:29:22 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:29:24 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:29:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:29:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:29:24 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:29:24 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:29:24 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:29:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:29:25 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:29:25 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:29:25 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:29:25 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:29:27 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:29:27 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:32:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:32:00 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:32:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:32:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:32:00 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:32:00 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a303d9ca2a0a6365e033b6e6351594c29a002ebd3c8ebf5b138a7b0c49dc6cb`  
		Last Modified: Tue, 09 Dec 2025 20:09:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3554616cf69297e760a899ae4e898a095622071a1f3c242f461e9ddaec3042`  
		Last Modified: Tue, 09 Dec 2025 20:09:18 GMT  
		Size: 29.9 MB (29942764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8be0142c38e7330e4234d1cb3210d3a13848e16781f8d0ee140172eb58de9a0`  
		Last Modified: Tue, 09 Dec 2025 20:09:14 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb566e4e5027491f423c5812c147f7f315ac9d8e579b26794a0a6559121514c`  
		Last Modified: Tue, 06 Jan 2026 18:32:23 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d069aa2d2c1ce9a1f95f2d0a1b39f86431f69a29a1b75f02d2708a7c61eb0c0`  
		Last Modified: Tue, 06 Jan 2026 18:32:28 GMT  
		Size: 68.7 MB (68713086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de032cd644ab2a12e6a204df67f4ded340281371c6352f024457cd97e420c20c`  
		Last Modified: Tue, 06 Jan 2026 18:32:23 GMT  
		Size: 934.7 KB (934689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fc903e78cc5d2e914e346401a1f13add6ace6cd76b1183efe4984bf369b22e`  
		Last Modified: Tue, 06 Jan 2026 18:32:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7f4d4ac81546a0237ee70134fba0b13ef0a9ffa0f9f6a05f26fb93006c52d2`  
		Last Modified: Tue, 06 Jan 2026 18:32:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2af0a94d273544ae863574703de809e9cf7027044e2c6482a0d7ef79448f850`  
		Last Modified: Tue, 06 Jan 2026 18:32:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e3dfbad0550320d1aefdc9a2f948ca8526ed6ba01a6d8b8f163a07adf2ddd6`  
		Last Modified: Tue, 06 Jan 2026 18:32:23 GMT  
		Size: 3.3 MB (3254010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e4868476cd04a9f1cea06840fcd2eb36293edaef73011b38583a8a5ef50688`  
		Last Modified: Tue, 06 Jan 2026 18:32:28 GMT  
		Size: 69.7 MB (69709439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdf7f8e8a51d87205f8fc741def149a550d65a632630d945f852d6dafc10957`  
		Last Modified: Tue, 06 Jan 2026 18:32:23 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:adfbaeba8648727e241da80d38727d6dbb0750345f798e04119ad3ccdee6a429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 KB (39996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c043e8a129c55c3459740d53e0b09c1d4439f684c8cde69491848747c7171fb`

```dockerfile
```

-	Layers:
	-	`sha256:33d560a830c1ac64748e5e5b8f375555a7d263f059e26a4c8e53673aa48890d8`  
		Last Modified: Tue, 06 Jan 2026 20:51:45 GMT  
		Size: 40.0 KB (39996 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:d2bf53bd8727fefaaffbd1c7b679cf22b2a070010a94ef4be7b919161d0ee2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188297800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bc148b768adee8e7b2afa6360f5bb8e60e2d3b3353b7ceb3fba52bf101dc62`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 20:00:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:02:11 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:02:11 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:02:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:02:11 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:02:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:02:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:02:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:02:11 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:29:17 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:29:21 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:29:23 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:29:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:29:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:29:24 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:29:24 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:29:24 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:29:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:29:24 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:29:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:29:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:29:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:29:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:29:26 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:31:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:31:46 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:31:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:31:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:31:46 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:31:46 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965231adfaa38474ba98843686365e96ac0c0c833b734717109a64ca18dab3a7`  
		Last Modified: Tue, 09 Dec 2025 20:02:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018bbb1cf6afb04f74e7b1c9e998bf6818523c3ed922ba5f771d1ea92a7cd1ab`  
		Last Modified: Tue, 09 Dec 2025 20:02:29 GMT  
		Size: 33.8 MB (33791597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f7268fb3755e75d353deaf8a38c837b6ceaacff43600ca6f07c35047bde940`  
		Last Modified: Tue, 09 Dec 2025 20:02:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181053cca17ae479e8f38135cc5318ebbb27e0c2ed1f0013d647764e5096abac`  
		Last Modified: Tue, 06 Jan 2026 18:32:07 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf14e872fe677a00781ba8f4092a065ef011297657c1969fd88719be8ec4f618`  
		Last Modified: Tue, 06 Jan 2026 18:32:13 GMT  
		Size: 74.7 MB (74749225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e04f08ee9711003267c9510d7a53869380a130f067bd1c7f9b7dba10cb4b696`  
		Last Modified: Tue, 06 Jan 2026 18:32:07 GMT  
		Size: 922.2 KB (922187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32c12380074e94ab9cea0e7e6a47d5462ca4b3a3e4e02e7a0020beb8705a56`  
		Last Modified: Tue, 06 Jan 2026 18:32:07 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea0705f42d61ccb44254a4282c580de9f96778009e9b3e80cb93d2d46c91962`  
		Last Modified: Tue, 06 Jan 2026 18:32:07 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b495ab9272fbbe6d5df672143c8c99dd9032fb2c3563369b021ea4be2a6b46b`  
		Last Modified: Tue, 06 Jan 2026 18:32:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed2f7360538f4c8386479524396aceb1faa363c03e8b8d32d92a487fd031e99`  
		Last Modified: Tue, 06 Jan 2026 18:32:07 GMT  
		Size: 3.3 MB (3254009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df64e0f9c9392707f219d07f602b022815c0ccc8ad92a70768621d68500709`  
		Last Modified: Tue, 06 Jan 2026 18:32:14 GMT  
		Size: 71.4 MB (71438618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea90595f2c36159592bc5bd34a77606c4d9967cbf02ff93514c24ee86714f1c`  
		Last Modified: Tue, 06 Jan 2026 18:30:53 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:13e5448a21d16641b8f71b887246f3388ab315cea6c97847f9afad0785f3ba26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 KB (40029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243e07a173672cef19b7eff1c032c5e538952d1aa36b43c301d1d15c012c7d10`

```dockerfile
```

-	Layers:
	-	`sha256:0663677efa519d984622a8667f913d064a6d04904089e5909ea6d5d2d7b38b5b`  
		Last Modified: Tue, 06 Jan 2026 20:51:59 GMT  
		Size: 40.0 KB (40029 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; 386

```console
$ docker pull redmine@sha256:f6f5ff388d41afe3af45ca57c3380270e50b622d25c2471094b2a1141d550b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185102630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04730df77a3745bfbd9724eae75ba1cd5dc133ccffb9bc4217615c74299d2422`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 20:00:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:02:11 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:02:11 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:02:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:02:11 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:02:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:02:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:02:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:02:11 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:27:55 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:27:59 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:28:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:28:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:28:01 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:28:01 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:28:01 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:28:01 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:28:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:28:01 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:28:01 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:28:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:28:01 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:28:04 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:28:04 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:29:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:29:54 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:29:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:29:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:29:54 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:29:54 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5692881991d3757cbf9f0e628a77702c09c4df4ed883556003995979a5a042ea`  
		Last Modified: Tue, 09 Dec 2025 20:02:24 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc87207c3572c38bf4a43337af28f9f1af314be171a665a9ac5f8f40bcb520d8`  
		Last Modified: Tue, 09 Dec 2025 20:02:27 GMT  
		Size: 29.9 MB (29944035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f7268fb3755e75d353deaf8a38c837b6ceaacff43600ca6f07c35047bde940`  
		Last Modified: Tue, 09 Dec 2025 20:02:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b902c0b653550277104cf85abd82f006352dcab1547ba514ce7ed063e75883`  
		Last Modified: Tue, 06 Jan 2026 18:30:17 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769cba340177fa474cfc8cdbc572e260b5d8303cc171b4c0eee9510fe567ed04`  
		Last Modified: Tue, 06 Jan 2026 18:30:26 GMT  
		Size: 75.9 MB (75871035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4879c88968ac8664f859aa11c0a5cf20ca1efd0be150d3408b3bb03b1c33e733`  
		Last Modified: Tue, 06 Jan 2026 18:30:17 GMT  
		Size: 939.2 KB (939231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8308c9f8a3cec8721be1737a9fe7a785bf62b63c18143e053e7e1f2eb3e84cb9`  
		Last Modified: Tue, 06 Jan 2026 18:30:17 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bff5686c2153dc3c64a95c571233d9d71a649e81c8370988490f0cdb2ce7292`  
		Last Modified: Tue, 06 Jan 2026 18:30:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ca63bbb407d2d11dc481d5a98e06c5ae56d6662ceac5d98aa45d05f927a86a`  
		Last Modified: Tue, 06 Jan 2026 18:30:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189213d6a426424d2bdaa92f7ced100f67ca670e24c9bf07a8110d7f7f5c156c`  
		Last Modified: Tue, 06 Jan 2026 18:30:17 GMT  
		Size: 3.3 MB (3254027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec0575366d59c3544e12b2dd1ec5553a3c47e414428d807654354be2e781c6a`  
		Last Modified: Tue, 06 Jan 2026 18:30:25 GMT  
		Size: 71.5 MB (71471283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c52eb690a16f35962ffadbf47d41d43209e94a3e0d9d2a78478d917e3cea8`  
		Last Modified: Tue, 06 Jan 2026 18:30:17 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:29392fa5e4cbcf6662d5b32572e76ec73fd2262237b182c18d806ed501504194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250cfcef3e7f4e7d1f9ba7f77dca4472610bf78334aff25c3d7f904cefb732c3`

```dockerfile
```

-	Layers:
	-	`sha256:d5b5eb5d55309584859cc8782e285377ad0e14a935af5216de706e7a2a1ad927`  
		Last Modified: Tue, 06 Jan 2026 20:52:02 GMT  
		Size: 39.8 KB (39808 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; ppc64le

```console
$ docker pull redmine@sha256:64167a5b3c684317c8d28baba8b14ee047d810764c5db260ff1afcc272bdf9c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189724776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1a29c853d5909f91030177546d44c9c5787155dbf92267078c6c8aa1315d55`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 20:03:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:47:08 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:47:08 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:47:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:47:08 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:47:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:47:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:47:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:47:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:47:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:47:09 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:53:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:53:45 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:53:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:53:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:53:50 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:53:50 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:53:51 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:53:51 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:53:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:53:52 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:53:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:53:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:53:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:53:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:53:55 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:56:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:56:57 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:56:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:56:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:56:58 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:56:58 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdf3e5b236174bf8a7f72eebdcbe39f5672bf2333fec5ff0bb140b22fcddbdb`  
		Last Modified: Tue, 09 Dec 2025 20:07:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b201c656d6d41ce3480456686a8c5fcb6a7dfbfbedb5a8a87530b6dd10988a76`  
		Last Modified: Tue, 09 Dec 2025 20:47:46 GMT  
		Size: 31.4 MB (31415525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929cc3c89d8d9779520ee0f83d486fecefe5a9ceccbcf26bd11eaf975c39d2b5`  
		Last Modified: Tue, 09 Dec 2025 20:47:44 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14c44a2c121a7607d180b4c7edfb28446c700ef908e42c96e7f1d0e1ddef851`  
		Last Modified: Tue, 06 Jan 2026 18:57:35 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a31212fa52ab26661b10040d1c0d34fa1a214d85829f156f052cf70eba7d599`  
		Last Modified: Tue, 06 Jan 2026 18:57:45 GMT  
		Size: 77.2 MB (77187171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2e8f2d0d4d2e4e95c310ac7713b47fb5cec3ddf74a58545107cc23dc8b2af2`  
		Last Modified: Tue, 06 Jan 2026 18:57:35 GMT  
		Size: 927.7 KB (927726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698cebb216fa637da8740c25eab4b0aaf4b9803a44f1da51bd1e64c23e56af57`  
		Last Modified: Tue, 06 Jan 2026 18:57:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48988e59d3fc590090b03fce3651ad31442828274d5d2e3395ebe0e4e0d64e00`  
		Last Modified: Tue, 06 Jan 2026 18:57:35 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b51dc410f9d9241e987f9deac4848567dc1300924bb7c8252c5663b5d0d122`  
		Last Modified: Tue, 06 Jan 2026 18:57:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bb6fe04701ecea168887c40ce65f73816465e4f9cdaa6297c22f8db7554744`  
		Last Modified: Tue, 06 Jan 2026 18:57:35 GMT  
		Size: 3.3 MB (3254007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36065e9680b194afa79c2d7f89018a44793617673e4ffd19d79240cb2c3cf8f1`  
		Last Modified: Tue, 06 Jan 2026 18:57:43 GMT  
		Size: 73.2 MB (73204018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0530d260c76a1428c5eae5ff2e141885df648ec8af6e8f47c18fcacd4dd5540`  
		Last Modified: Tue, 06 Jan 2026 18:57:35 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:0a4d1f81b6744865351f89f656a3e57b68443330a8cce7038abd67590bface6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 KB (39897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acab7eda01d1126d809b8d859163aa9fc6b83de74a55c387828b9754a5a9ff5f`

```dockerfile
```

-	Layers:
	-	`sha256:d86a2ee7e79feaa1cb2ef4c0aff4fb565d2669c852fe0567546ee085759dcd44`  
		Last Modified: Tue, 06 Jan 2026 20:52:05 GMT  
		Size: 39.9 KB (39897 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; riscv64

```console
$ docker pull redmine@sha256:1fa05c1ce6a7106cac4cea11e939ef73cb6dca539601a011a0e0eb593f73fd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184265105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c861dbac55c21864cca0a3309274fe8776328499cc9f90d4c19797eb33638d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 13 Dec 2025 01:39:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 13 Dec 2025 18:28:01 GMT
ENV LANG=C.UTF-8
# Sat, 13 Dec 2025 18:28:01 GMT
ENV RUBY_VERSION=3.2.9
# Sat, 13 Dec 2025 18:28:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Sat, 13 Dec 2025 18:28:01 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Sat, 13 Dec 2025 18:28:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 13 Dec 2025 18:28:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Dec 2025 18:28:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Dec 2025 18:28:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 18:28:02 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 13 Dec 2025 18:28:02 GMT
CMD ["irb"]
# Mon, 15 Dec 2025 02:31:01 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 15 Dec 2025 02:31:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 15 Dec 2025 02:31:41 GMT
ENV GOSU_VERSION=1.19
# Mon, 15 Dec 2025 02:31:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 15 Dec 2025 02:31:41 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 15 Dec 2025 02:31:41 GMT
ENV RAILS_ENV=production
# Mon, 15 Dec 2025 02:31:42 GMT
WORKDIR /usr/src/redmine
# Mon, 15 Dec 2025 02:31:42 GMT
ENV HOME=/home/redmine
# Mon, 15 Dec 2025 02:31:42 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 15 Dec 2025 02:31:42 GMT
ENV REDMINE_VERSION=5.1.10
# Mon, 15 Dec 2025 02:31:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Mon, 15 Dec 2025 02:31:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Mon, 15 Dec 2025 02:31:42 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 15 Dec 2025 02:31:47 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 15 Dec 2025 02:31:47 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 15 Dec 2025 03:31:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 15 Dec 2025 03:31:06 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 15 Dec 2025 03:31:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 15 Dec 2025 03:31:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 15 Dec 2025 03:31:07 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 15 Dec 2025 03:31:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26b0bd4ba0001e62e053563ad2589e2ee25243368f3dce76bed85b6313b4567`  
		Last Modified: Sat, 13 Dec 2025 03:34:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63696b48d2aeee0ffdbb7b78565ca7d0a880422540ab84716fb18cdabc0b659`  
		Last Modified: Sat, 13 Dec 2025 18:29:16 GMT  
		Size: 29.8 MB (29831135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe10c05851c7a0b4074a8dda6aea2b06377e8b8fff8cb57049fbdc6c89612c0`  
		Last Modified: Sat, 13 Dec 2025 18:29:13 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9863aff404585ca5f24b0364c15f43b8d09d317a41c085ca72ad5171556f6aef`  
		Last Modified: Mon, 15 Dec 2025 03:33:31 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee288fa149136dabfc216547f771016e49cd896f4c7f24d8a01b703f47cf809a`  
		Last Modified: Mon, 15 Dec 2025 03:33:38 GMT  
		Size: 72.0 MB (72021387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b91eee386994231d8c208558638b906a2d05b06094d421279e49b330d11322`  
		Last Modified: Mon, 15 Dec 2025 03:33:32 GMT  
		Size: 915.2 KB (915161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300b5acbf9171908ea8f6f0d4ac9df303eb46295496c7b0f7869aabf06161d3a`  
		Last Modified: Mon, 15 Dec 2025 03:33:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e890055c697ab940fd447e60450ba8ce6c8ce548c03f4b6ffa79c55b1f9305e`  
		Last Modified: Mon, 15 Dec 2025 03:33:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f764a525853275ee5d1f4980e6a315815fd45f515b72e69c20f4e904b11a43`  
		Last Modified: Mon, 15 Dec 2025 03:33:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76de68b654bbca47f7c4249bd1ca973db477a40c6b0dcc6fddb776673a5124a`  
		Last Modified: Mon, 15 Dec 2025 03:33:32 GMT  
		Size: 3.3 MB (3252528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50443188cc1875aaa31ccb6c761f7649476e9cc8e08d95b9fc5f4073d8a003fd`  
		Last Modified: Mon, 15 Dec 2025 03:33:38 GMT  
		Size: 74.7 MB (74725571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b20c37b0f9202cdf4efeda91608d8b2083017e752218fdba78df703c6150d72`  
		Last Modified: Mon, 15 Dec 2025 03:33:31 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:a784a9f6ff484550a90092f0a5a8d2f6f2fbf2ed301757e6c93e5573e13b1c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 KB (39897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf74b85e992747c4e3058d3cc03d28d35edea61b1c6932d843e23203a099f50`

```dockerfile
```

-	Layers:
	-	`sha256:ecd5cc965608ff43d2aaf98d9c57afb014b99db2d742e4a801837f291b1369ca`  
		Last Modified: Mon, 15 Dec 2025 05:49:51 GMT  
		Size: 39.9 KB (39897 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.22` - linux; s390x

```console
$ docker pull redmine@sha256:050541b2a08b68f94ad889318d02a06560b8e7f95edaf53ca7ba2693d7ec2135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185855677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67897d0bb412c4d669b330a434615c9d705e836b7318278b3b278d6c1e1c968b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 19:56:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:16:09 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:16:09 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:16:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:16:09 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:16:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:16:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:16:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:16:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:16:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:16:09 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:33:00 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:33:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:33:08 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:33:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:33:08 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:33:08 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:33:08 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:33:08 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:33:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:33:08 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:33:08 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:33:08 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:33:08 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:33:09 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:33:09 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:35:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:35:18 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:35:18 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:35:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:18 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:35:18 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559a492a9261e799874f27f97a8210839dee9952835594c19282c304847eaf8b`  
		Last Modified: Tue, 09 Dec 2025 20:00:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cc0c82f2b5d5a6b93d14ee77ab6ee8aaa17b66d1a799f2d2f654d9c29b06a4`  
		Last Modified: Tue, 09 Dec 2025 20:16:29 GMT  
		Size: 31.3 MB (31265098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3ca95c701ca87ac5722618245cc18035889f83af3fe96f29f2a31e9da6ae49`  
		Last Modified: Tue, 09 Dec 2025 20:16:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edbfb75f2048b266fa38f3a30860f2e5524a86edf6a2716907f023023416cba`  
		Last Modified: Tue, 06 Jan 2026 18:35:44 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d498ea6917fb2b38bdaeefc00b9d24aa9a0bb7b3657086be9c4a389c7d6bc4`  
		Last Modified: Tue, 06 Jan 2026 18:35:48 GMT  
		Size: 74.1 MB (74083286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e34b13a8b920dec2abc9a1314f93f4d763c8cf85cb2918487d6b6055a235201`  
		Last Modified: Tue, 06 Jan 2026 18:35:44 GMT  
		Size: 943.2 KB (943208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b897c3499cfcf9ba0d909918fcb8ebff9e17650b18682f8346e662b7d320693`  
		Last Modified: Tue, 06 Jan 2026 18:35:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cf03993da440b30cc551e1edc8d4a7c0e8cf08effa03ace12197b31c9607ff`  
		Last Modified: Tue, 06 Jan 2026 18:35:44 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df3e410c2559ba91d371dc2903bc916081396c9e8adc2b39576ff28c0caa203`  
		Last Modified: Tue, 06 Jan 2026 18:35:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57ced01234572c9952fe44196ca4023877204aa16dad1c063a4a4162d31f885`  
		Last Modified: Tue, 06 Jan 2026 18:35:45 GMT  
		Size: 3.3 MB (3254023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112ba695d827541bdedaef8fe95e89e417a4b8f2d7a1aee1ad23fd3af08cb4e7`  
		Last Modified: Tue, 06 Jan 2026 18:35:49 GMT  
		Size: 72.7 MB (72656726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e385b501dbd23aabe31f90aad6db6ce30a64d897615374be72b8323745fc74`  
		Last Modified: Tue, 06 Jan 2026 18:35:45 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:c02a77151e8d2adee9ac1ed506bc7343d236e8f9068f66d8712778023bd5e977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7294328bf4de31a2e7a44f82c11f38d73ead794e12bab2a0d9425181c67d9dc`

```dockerfile
```

-	Layers:
	-	`sha256:4e614cc7a63d895b51d534491d903a0c585a26363b678b79a7aa0ff93a9e3655`  
		Last Modified: Tue, 06 Jan 2026 20:52:10 GMT  
		Size: 39.8 KB (39847 bytes)  
		MIME: application/vnd.in-toto+json
