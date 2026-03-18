## `redmine:alpine3.22`

```console
$ docker pull redmine@sha256:203de05db24c9cd4f4b1fb60e32c49451d303bd6f8b95d43fb152a1cc8cc8f57
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

### `redmine:alpine3.22` - linux; amd64

```console
$ docker pull redmine@sha256:0679b48cf01d19da78710564a03fb70c9b5d7fc3c51267739b81269bcd1fc876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195100932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf4552bf5a92f9a26c7cd9a49cef6556d4c427f32c6d266d64a3371c2c289ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:38:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:40:34 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:40:34 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:40:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:40:34 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:40:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:40:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:40:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:40:35 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 16:31:12 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 17 Mar 2026 16:31:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 17 Mar 2026 16:31:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 16:31:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 16:31:18 GMT
ENV RAILS_ENV=production
# Tue, 17 Mar 2026 16:31:18 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Mar 2026 16:31:18 GMT
ENV HOME=/home/redmine
# Tue, 17 Mar 2026 16:31:18 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 17 Mar 2026 16:31:18 GMT
ENV REDMINE_VERSION=6.1.2
# Tue, 17 Mar 2026 16:31:18 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Tue, 17 Mar 2026 16:31:18 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Tue, 17 Mar 2026 16:31:18 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 17 Mar 2026 16:31:21 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 17 Mar 2026 16:31:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 17 Mar 2026 16:31:58 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Mar 2026 16:31:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 16:31:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 16:31:58 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 17 Mar 2026 16:31:58 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b11cdfcaade8867c80cc4a735d30d0b0c5b102e8435d4b62cc7d3727c65aee`  
		Last Modified: Wed, 11 Mar 2026 18:40:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f044033e33c85a0de2061193821568740f9f257609b2828b28c0f0c2225fd212`  
		Last Modified: Wed, 11 Mar 2026 18:40:43 GMT  
		Size: 39.3 MB (39279026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9173d7cdd746ca59b17112215b4da455db578880f3aa5a69d9aa07a7552cb93a`  
		Last Modified: Wed, 11 Mar 2026 18:40:42 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dac14e748c5e18036a516730e711a19e8fa8e658680cae154a70c3f82d5c894`  
		Last Modified: Tue, 17 Mar 2026 16:32:08 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51d7dc8b72769b660c0f097a8f80f44294cfea8e1304b9286abdbcb9565226`  
		Last Modified: Tue, 17 Mar 2026 16:32:11 GMT  
		Size: 75.5 MB (75465152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3557c11377ec7e9a62a421ad276632a4af6c6e69e1c8ebb183752fe05a3693d6`  
		Last Modified: Tue, 17 Mar 2026 16:32:09 GMT  
		Size: 966.8 KB (966771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ea43cd75cba233789f52191227dcacc690e4e52363118d57c3bea72481cb5d`  
		Last Modified: Tue, 17 Mar 2026 16:32:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7b9ffa8bac0051defc8c9aab268efd8b74c9e83911076e86bfc30e3a7dc1e4`  
		Last Modified: Tue, 17 Mar 2026 16:32:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31c08a392744df2045ff563bba1775afa7686c8ea2f79d324af39daef17186c`  
		Last Modified: Tue, 17 Mar 2026 16:32:11 GMT  
		Size: 4.1 MB (4149815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae6938bfa4b9e64592be2866879a3e6136551139187209659d21182ee57090e`  
		Last Modified: Tue, 17 Mar 2026 16:32:12 GMT  
		Size: 71.4 MB (71431379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57db669e895fd9a378322f798a952b385ef109739edb18532c8a23d540e57b72`  
		Last Modified: Tue, 17 Mar 2026 16:32:11 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:2577ff0e53cd0ac27613adfb4ffe63c2fc7db02c767ebda78312d6807b2de797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7211241af92eeb3cc843a9bfe583f0491b1182d074dacb1c47ddaa432444446b`

```dockerfile
```

-	Layers:
	-	`sha256:2102276a7a24e69cc3aee3b948a76de3bca2e63dafacba85b46e144a93bb156d`  
		Last Modified: Tue, 17 Mar 2026 16:32:09 GMT  
		Size: 36.7 KB (36748 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; arm variant v7

```console
$ docker pull redmine@sha256:c51c8f9de62cee95298118314f6bdc91f4bbdd2929bb41071f77cc60ba1ecdaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199143849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20aa60ef01ba5b569b1c273c1c7aaea183f9c8f61ab315864502c52e64c9cfc6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:38:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:40:56 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:40:56 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:40:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:40:56 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:40:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:40:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:40:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:40:57 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 16:32:24 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 17 Mar 2026 16:32:34 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 17 Mar 2026 16:32:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 16:32:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 16:32:38 GMT
ENV RAILS_ENV=production
# Tue, 17 Mar 2026 16:32:38 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Mar 2026 16:32:38 GMT
ENV HOME=/home/redmine
# Tue, 17 Mar 2026 16:32:38 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 17 Mar 2026 16:32:38 GMT
ENV REDMINE_VERSION=6.1.2
# Tue, 17 Mar 2026 16:32:38 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Tue, 17 Mar 2026 16:32:38 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Tue, 17 Mar 2026 16:32:38 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 17 Mar 2026 16:32:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 17 Mar 2026 16:34:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 17 Mar 2026 16:34:02 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Mar 2026 16:34:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 16:34:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 16:34:02 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 17 Mar 2026 16:34:02 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e866a3a56411b18e3fccbdfcceb747e57a4fd8c56d27b14fb22fe4b7d079647c`  
		Last Modified: Wed, 11 Mar 2026 18:41:05 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d06d1b8515850129b34f14ba8bae20e1beb6c66eecf11db319193dbd55496f`  
		Last Modified: Wed, 11 Mar 2026 18:41:06 GMT  
		Size: 34.8 MB (34794864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce704f3fb5c10979ffca832846860a8b4c0a2790a0606cefc129f15a88231bb0`  
		Last Modified: Wed, 11 Mar 2026 18:41:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be7d20be3e07f9399c1e03b103a50190a9d06af65c0023e82aae31f76fcd976`  
		Last Modified: Tue, 17 Mar 2026 16:34:12 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332d01f4aa9f8c79b43b765fd2c93ba3e84f66f196dd8dbc367519a3775bfb6`  
		Last Modified: Tue, 17 Mar 2026 16:34:14 GMT  
		Size: 69.0 MB (69015251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b8221c60948f6a5946adfa00762ca2bb3f0916ae9ef9efaa24a2218944d63f`  
		Last Modified: Tue, 17 Mar 2026 16:34:12 GMT  
		Size: 934.7 KB (934709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e645da728cfce1425f5b0370cf83812095f16c421b7824578e2be718186a4b`  
		Last Modified: Tue, 17 Mar 2026 16:34:12 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56f6e37f0158f8a427a5af646e7d0890058f682732b62074873fcb49701260c`  
		Last Modified: Tue, 17 Mar 2026 16:34:13 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e8a1e3c6e0194d292a4af317d95d8fa89d388bc4cc7b2fbe3eeb59fe3161f`  
		Last Modified: Tue, 17 Mar 2026 16:34:13 GMT  
		Size: 4.1 MB (4149785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65daf37c89cfa3207d1f320d2d5ac3ddab08a97d0e706e9dba46ad782b6c1cda`  
		Last Modified: Tue, 17 Mar 2026 16:34:15 GMT  
		Size: 87.0 MB (87021699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9455d116a9414ea97a0758c0c361bb6f1624c4e8853b4e29eae243c4d6f54d51`  
		Last Modified: Tue, 17 Mar 2026 16:34:14 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:3c8be30b04e54ccff038be798e3e801329354c4d6485aa5ba6d87746ebf2ff6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5641353c5b788196a7a46cc1471568c1c6624bd1bb40dd76af22c5b40b1bfdf6`

```dockerfile
```

-	Layers:
	-	`sha256:55a44c860f3da8ca478eb4befff427d45b7278ed2434aa51b0235c5bb41f6a77`  
		Last Modified: Tue, 17 Mar 2026 16:34:12 GMT  
		Size: 36.9 KB (36892 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:033032f73b5316ddbce8cdca70be25ae82f03156d83aa2276cf980a2481cc451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194660080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592731aa2827069b3eda2e9c97f030740f6c14e1cb97687d548e1c1ff382847c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:38:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:40:27 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:40:27 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:40:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:40:27 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:40:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:40:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:40:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:40:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:40:27 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 16:30:44 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 17 Mar 2026 16:30:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 17 Mar 2026 16:30:54 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 16:30:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 16:30:54 GMT
ENV RAILS_ENV=production
# Tue, 17 Mar 2026 16:30:54 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Mar 2026 16:30:54 GMT
ENV HOME=/home/redmine
# Tue, 17 Mar 2026 16:30:54 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 17 Mar 2026 16:30:54 GMT
ENV REDMINE_VERSION=6.1.2
# Tue, 17 Mar 2026 16:30:54 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Tue, 17 Mar 2026 16:30:54 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Tue, 17 Mar 2026 16:30:54 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 17 Mar 2026 16:30:57 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 17 Mar 2026 16:31:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 17 Mar 2026 16:31:57 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Mar 2026 16:31:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 16:31:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 16:31:57 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 17 Mar 2026 16:31:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a6f998bb274ad4e6a07d4917c684860e48dc843b8b9842e0b1e3d657732071`  
		Last Modified: Wed, 11 Mar 2026 18:40:35 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640a475ad9bb2c787fdd7e59ecc9922b62ca5447e2cae7c9c4797ae88a956db9`  
		Last Modified: Wed, 11 Mar 2026 18:40:36 GMT  
		Size: 39.2 MB (39193144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d357d4fb1dad8fd358a01312bd4a508256f4e6ee3f44cd765c77bb54f5622fde`  
		Last Modified: Wed, 11 Mar 2026 18:40:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a4c39d83c94449aade98a189285bbc0c33ecb30119e10da761bb0f7fe5de80`  
		Last Modified: Tue, 17 Mar 2026 16:32:07 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a332d9d4e0b7f5efd04bafe3507e91aa8e88a876f7bb4c63a5456c1479668e5a`  
		Last Modified: Tue, 17 Mar 2026 16:32:10 GMT  
		Size: 75.1 MB (75095266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaeae1e491be189494199cdfaaeb1438cf231db5eef312f02f08203146910be9`  
		Last Modified: Tue, 17 Mar 2026 16:32:08 GMT  
		Size: 922.2 KB (922197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4c2697982f75f2c991ec5f0ade94f1e3abc93284c89e1783f12c39df88ac4`  
		Last Modified: Tue, 17 Mar 2026 16:32:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfbdf9c94fd1b6886857109d537be9fd4329f28d396a795df874ac6892db36c`  
		Last Modified: Tue, 17 Mar 2026 16:32:09 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b0a254ed3d1f605192ca530373d56f047600b63e9997eb1c247e5457ef577`  
		Last Modified: Tue, 17 Mar 2026 16:32:09 GMT  
		Size: 4.1 MB (4149822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f805625ec605b1adf7bd7730c93a0b8b7f4a42c22459fb9b45e2c100da69a0d5`  
		Last Modified: Tue, 17 Mar 2026 16:32:11 GMT  
		Size: 71.2 MB (71156218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac287ea719b728914aab014fc1363f897ae61bb3ccd4254028391871cf0d2b0`  
		Last Modified: Tue, 17 Mar 2026 16:32:10 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:1ac424d2b91e3f51768e4ffa3ada24f494a2be07b0868504c91166a839b4c044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674a8f2c88a528291edf7c4e711d964ba4092b771d9e8669c149aa77256bf109`

```dockerfile
```

-	Layers:
	-	`sha256:5c303646e6c71d5fba378592e7aed22f244b7836389e9f6ff1b7ace8c471a665`  
		Last Modified: Tue, 17 Mar 2026 16:32:08 GMT  
		Size: 36.9 KB (36927 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; 386

```console
$ docker pull redmine@sha256:3ce64ef663ca03f34baff82edc89e748571d374d986c43ad007ab27bf5c66ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212549684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510c7848a816fb10217740e28cd9fbdf7f622b46650d26b8afcbe596199d6eb0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:29:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:31:41 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:31:41 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:31:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:31:41 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:31:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:31:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:31:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:31:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:31:41 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 16:30:45 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 17 Mar 2026 16:30:59 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 17 Mar 2026 16:31:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 16:31:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 16:31:04 GMT
ENV RAILS_ENV=production
# Tue, 17 Mar 2026 16:31:04 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Mar 2026 16:31:04 GMT
ENV HOME=/home/redmine
# Tue, 17 Mar 2026 16:31:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 17 Mar 2026 16:31:04 GMT
ENV REDMINE_VERSION=6.1.2
# Tue, 17 Mar 2026 16:31:04 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Tue, 17 Mar 2026 16:31:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Tue, 17 Mar 2026 16:31:04 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 17 Mar 2026 16:31:06 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 17 Mar 2026 16:33:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 17 Mar 2026 16:33:19 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Mar 2026 16:33:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 16:33:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 16:33:19 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 17 Mar 2026 16:33:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d1f37121f7a1d4388eb81223443f4a79ee5c328e020c28472aac97fae65b71`  
		Last Modified: Wed, 11 Mar 2026 18:31:47 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88776a0de847d517f0ef2c1b780e6d54f3390a54a6430ff1a885f8f28cf738e4`  
		Last Modified: Wed, 11 Mar 2026 18:31:48 GMT  
		Size: 34.8 MB (34789078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7759d014de47a1a9b520de8d68e8b099deffd4b00faa599dbcf8a5a9c9408`  
		Last Modified: Wed, 11 Mar 2026 18:31:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d300f96c92fdc7c09a912bc267d9d2f7895ead8e4ec49287e9f17fb5bd8bbde`  
		Last Modified: Tue, 17 Mar 2026 16:33:29 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c473f105f2d0675162a2083df9e5f8bd4018870b09057b353609f0812901a88d`  
		Last Modified: Tue, 17 Mar 2026 16:33:32 GMT  
		Size: 76.2 MB (76218370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb9d9ca01cc3f803d8a83346dfe021cc2e8e83d762425d19fcd9798ed054a44`  
		Last Modified: Tue, 17 Mar 2026 16:33:29 GMT  
		Size: 939.3 KB (939255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26f906ea60f994d7d4635f2446ae9e00681efdc62a1c7138198b9edf3f72401`  
		Last Modified: Tue, 17 Mar 2026 16:33:29 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811a4094effe32b337c44ce5c3fb00f24d89514c1550e77b8ef5e0bca92707f`  
		Last Modified: Tue, 17 Mar 2026 16:33:30 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdabf9d84589c4dc76dac4a3839032d0580d8118a386b86f3727500c27a1020`  
		Last Modified: Tue, 17 Mar 2026 16:33:31 GMT  
		Size: 4.1 MB (4149825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2760403ca500354b50961c303938f69b0606d918816c54f811f128e2c20b6fe7`  
		Last Modified: Tue, 17 Mar 2026 16:33:34 GMT  
		Size: 92.8 MB (92828512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c525f41ab9e6d9f7383927ffdf04684283f5ebb21c58780359bb5cbc2e471917`  
		Last Modified: Tue, 17 Mar 2026 16:33:32 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:1fd1bc60d0e1c4d9a498652daa06b1257331d3c33c96d45c0524f4932aff9719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce2c85afc64e22861fafadf62b6fb44fedf3ae42f1d1fc378957587175688cf`

```dockerfile
```

-	Layers:
	-	`sha256:1340deecce037433ff63ff044d749c6fe629d3be5d486b35ba1d12b3539a4c4c`  
		Last Modified: Tue, 17 Mar 2026 16:33:29 GMT  
		Size: 36.7 KB (36706 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; ppc64le

```console
$ docker pull redmine@sha256:8bdda09f5f0cb7488f73912d012b813e019bd8b9a3f74e5aab77a69c29d03da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231346630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d3ed2f600651cf52b84ef8d840eff19123fa6cbe96373e14b6f4d8bee3605b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:51:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:55:22 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:55:22 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:55:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:55:22 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:55:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:55:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:55:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:55:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:55:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:55:23 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 21:27:06 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 17 Mar 2026 21:27:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 17 Mar 2026 21:27:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 21:27:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 21:27:35 GMT
ENV RAILS_ENV=production
# Tue, 17 Mar 2026 21:27:35 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Mar 2026 21:27:35 GMT
ENV HOME=/home/redmine
# Tue, 17 Mar 2026 21:27:35 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 17 Mar 2026 21:27:35 GMT
ENV REDMINE_VERSION=6.1.2
# Tue, 17 Mar 2026 21:27:35 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Tue, 17 Mar 2026 21:27:35 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Tue, 17 Mar 2026 21:27:35 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 17 Mar 2026 21:27:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 17 Mar 2026 21:32:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 17 Mar 2026 21:32:12 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Mar 2026 21:32:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 21:32:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 21:32:13 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 17 Mar 2026 21:32:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2164258dfb1a4210b66bdb1cd7cd294200c85c34c5d2385a2fa87d0e8d04d4e7`  
		Last Modified: Wed, 11 Mar 2026 18:55:38 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728a2cac2a5f4c5ac3ddeafea7998bb4a36424f308ab256b6d18346e53322e9c`  
		Last Modified: Wed, 11 Mar 2026 18:55:39 GMT  
		Size: 36.4 MB (36448451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137503cffc1d50ede26f0fb9dfc45cf530badb0376089b2a76152f8c918e165a`  
		Last Modified: Wed, 11 Mar 2026 18:55:38 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f065b321907aecc65aaff36e93906b1e6061827604d95235a17eaf51f19534d4`  
		Last Modified: Tue, 17 Mar 2026 21:32:33 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c514ec5c9cd7ba6f76f0acd76f89c85f7796c567cd2a794cf24552787ea3d4d`  
		Last Modified: Tue, 17 Mar 2026 21:32:36 GMT  
		Size: 77.5 MB (77533720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc7e74e376f7d30f02cc1dc3529d1aee786bbd1df9cd60df8ff02d4acad68da`  
		Last Modified: Tue, 17 Mar 2026 21:32:34 GMT  
		Size: 927.7 KB (927748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa45fe98071a959eb19d705921517ffeaf657c1a2b258327e7cccd982f3cb76`  
		Last Modified: Tue, 17 Mar 2026 21:32:34 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cd80823c4e77b3cea741b1b30bb6405758fb8166d0327b7194012a0ca8f889`  
		Last Modified: Tue, 17 Mar 2026 21:32:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90dfb09b8601d074ff75aec08e21f37a46031a37c519b0e186ed39fb7c4c49b`  
		Last Modified: Tue, 17 Mar 2026 21:32:35 GMT  
		Size: 4.1 MB (4149843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eac964fb42755905aa6fa572c5593ebd1e77d6aa66e5cafeb53f431d219c32`  
		Last Modified: Tue, 17 Mar 2026 21:32:38 GMT  
		Size: 108.5 MB (108548655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1666c70ddc18677fd86d0edee21e09c2b26c30491b1f9697489a974de88b030a`  
		Last Modified: Tue, 17 Mar 2026 21:32:36 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:339c79ef74eeb43fda1f4cd1b883a14fbe8d9011ebecd01de9ed34dd4fbc69b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c987ecc354e8f90c2f9f9f10a3a28c87a7314d4297cd753ab86be2e43c9a7718`

```dockerfile
```

-	Layers:
	-	`sha256:1c48162f2732bdabfa3107e3796d3bfbde27963725722395f0093c661989b839`  
		Last Modified: Tue, 17 Mar 2026 21:32:33 GMT  
		Size: 36.8 KB (36804 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; riscv64

```console
$ docker pull redmine@sha256:a882ba0b42ff6736b8547852e14814cab109eb50c69c7ac097da35d99437e77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225051025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f5aed165ae5c173be2f19dfd56c8684b75def11fc408835f2dddcb57efd972`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 06:21:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 12 Mar 2026 08:25:01 GMT
ENV LANG=C.UTF-8
# Thu, 12 Mar 2026 08:25:01 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 12 Mar 2026 08:25:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 12 Mar 2026 08:25:01 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 12 Mar 2026 08:25:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 12 Mar 2026 08:25:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 Mar 2026 08:25:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 Mar 2026 08:25:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Mar 2026 08:25:02 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 12 Mar 2026 08:25:02 GMT
CMD ["irb"]
# Thu, 12 Mar 2026 12:33:33 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 12 Mar 2026 12:34:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 12 Mar 2026 12:34:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Mar 2026 12:34:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Mar 2026 12:34:21 GMT
ENV RAILS_ENV=production
# Thu, 12 Mar 2026 12:34:22 GMT
WORKDIR /usr/src/redmine
# Thu, 12 Mar 2026 12:34:22 GMT
ENV HOME=/home/redmine
# Thu, 12 Mar 2026 12:34:22 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 12 Mar 2026 12:34:22 GMT
ENV REDMINE_VERSION=6.1.1
# Thu, 12 Mar 2026 12:34:22 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.1.tar.gz
# Thu, 12 Mar 2026 12:34:22 GMT
ENV REDMINE_DOWNLOAD_SHA256=1f2e6dd0697062fc733701f88b5041dc0dfc6b536255eb7902f21fb0970e603e
# Thu, 12 Mar 2026 12:34:22 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 12 Mar 2026 12:34:27 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 12 Mar 2026 16:54:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 12 Mar 2026 16:54:28 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 12 Mar 2026 16:54:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 12 Mar 2026 16:54:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Mar 2026 16:54:29 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 12 Mar 2026 16:54:29 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a67a56f28f84edbf19075aea9793f9cb60a2c529c81387029f481c8d410177d`  
		Last Modified: Thu, 12 Mar 2026 08:26:09 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017db5421bb2e54843c4d73b22b9c09070d32f31171f7f71ac106976ee85fafb`  
		Last Modified: Thu, 12 Mar 2026 08:26:15 GMT  
		Size: 34.9 MB (34905653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12066bae17ecfdb31d70c167a52eec1f8fe2171b1e68af46b762fccdd60142b3`  
		Last Modified: Thu, 12 Mar 2026 08:26:09 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff56c03599bc2deacc92c7ccc9bf12717ffca23e58098eefb79609f800f44292`  
		Last Modified: Thu, 12 Mar 2026 16:56:55 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901a0b24bb4ab7ab30ec0d7825829983b0febbea73f757ca96f5d3e9a9812a8`  
		Last Modified: Thu, 12 Mar 2026 16:57:15 GMT  
		Size: 72.4 MB (72361126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42033541a48099dfc9b60cb5130c97c8f27fae351bd0f4f30cdc14d379d5c85`  
		Last Modified: Thu, 12 Mar 2026 16:56:55 GMT  
		Size: 915.2 KB (915168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0b8aa3a07e02f67a2c2c057bac9353055308088c57143954bca28f864369a0`  
		Last Modified: Thu, 12 Mar 2026 16:56:55 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ba2170dec4589f9ea14ca0496f044ee057aea29355b444ed45f716e75ece94`  
		Last Modified: Thu, 12 Mar 2026 16:56:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6ba848afc2e8427b708898d998548ee4c4f3206e96f3b92c67d9bcaf56130d`  
		Last Modified: Thu, 12 Mar 2026 16:56:58 GMT  
		Size: 4.1 MB (4146154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc2572b28d3715189d7251c5d719a80b17a134ecf6bd4511b90876431e401c`  
		Last Modified: Thu, 12 Mar 2026 16:57:22 GMT  
		Size: 109.2 MB (109201582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065cf13f426311d91f0eadea8c72a601c78c8e285ff8a1fb45299b6c86e95079`  
		Last Modified: Thu, 12 Mar 2026 16:56:59 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:7045d836af07ba975bfb9152bb897c84f64df32d148ab85740de07b2557fa447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aedfde80d8ab38ea02ab0fc36c68f1268a183bc78fc415096ec42272aaa6eca`

```dockerfile
```

-	Layers:
	-	`sha256:45c632fbe4a8f35034bafdbf71b3d79bb19f8f9eea232bb6027164f2445cdcd9`  
		Last Modified: Thu, 12 Mar 2026 16:56:55 GMT  
		Size: 36.8 KB (36803 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.22` - linux; s390x

```console
$ docker pull redmine@sha256:e3f23956db2553fd035f966812a768d27f15c0cd4fab4fb9f3b56aecee6afc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226885548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683946a63cb9b1359e15b57b778d9e9f23384a39c2907530a65631aaab17c6ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:34:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 11 Mar 2026 18:36:40 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:36:40 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 11 Mar 2026 18:36:40 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 11 Mar 2026 18:36:40 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 11 Mar 2026 18:36:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 11 Mar 2026 18:36:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 11 Mar 2026 18:36:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 11 Mar 2026 18:36:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:36:40 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 11 Mar 2026 18:36:40 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 16:35:16 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 17 Mar 2026 16:35:31 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 17 Mar 2026 16:35:38 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 16:35:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 16:35:38 GMT
ENV RAILS_ENV=production
# Tue, 17 Mar 2026 16:35:38 GMT
WORKDIR /usr/src/redmine
# Tue, 17 Mar 2026 16:35:38 GMT
ENV HOME=/home/redmine
# Tue, 17 Mar 2026 16:35:38 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 17 Mar 2026 16:35:38 GMT
ENV REDMINE_VERSION=6.1.2
# Tue, 17 Mar 2026 16:35:38 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.2.tar.gz
# Tue, 17 Mar 2026 16:35:38 GMT
ENV REDMINE_DOWNLOAD_SHA256=938e975e808ccfb4b0dcbad8b42f02aacf0ca9ef15491c38c5af4756740ccf08
# Tue, 17 Mar 2026 16:35:38 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 17 Mar 2026 16:35:41 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 17 Mar 2026 16:41:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 17 Mar 2026 16:41:08 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 17 Mar 2026 16:41:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 16:41:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 16:41:09 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 17 Mar 2026 16:41:09 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c50fa19510f6fad0fbef2edb4458a5d6c4651b0216139f66adfa4a1aa49e22`  
		Last Modified: Wed, 11 Mar 2026 18:36:52 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b558cc6ce1cc9bbd1c2b70605adac2509a528de55027a7bd78fc71b02c4cf511`  
		Last Modified: Wed, 11 Mar 2026 18:36:53 GMT  
		Size: 36.2 MB (36226733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0874966b16a7b74e7911167dba3229eb87dd333e60693da93f5f28569342b0d6`  
		Last Modified: Wed, 11 Mar 2026 18:36:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b6ff8b8becee44e2f8492b8ee41f84416cde9e1418806bc1b0f4608610805e`  
		Last Modified: Tue, 17 Mar 2026 16:41:44 GMT  
		Size: 914.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b365742a4c1c8bf370832182a34d02a82ae465234e79796bf76747e80d5626`  
		Last Modified: Tue, 17 Mar 2026 16:41:49 GMT  
		Size: 74.5 MB (74464526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed5227e02ddc9773a27748c82ab406a64d107b4c7dbec2abb688c03f1523379`  
		Last Modified: Tue, 17 Mar 2026 16:41:45 GMT  
		Size: 943.2 KB (943171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8798986170a4e1f4fc8df5321a17183890a592704453f4d77c95786eb30ad8c`  
		Last Modified: Tue, 17 Mar 2026 16:41:44 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb13be08a0e73213a89ac919c7d558297c6076fd69a9dc438f4c7dc85dd59614`  
		Last Modified: Tue, 17 Mar 2026 16:41:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ab672ce62f509856138ec95e173657b2c6c0874cec4b4c3891fd39ba1e4333`  
		Last Modified: Tue, 17 Mar 2026 16:41:47 GMT  
		Size: 4.1 MB (4149844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0176888a3ec2cff0ffedc979d6414f73fde99362b8b18bc345b00ce813ac49c`  
		Last Modified: Tue, 17 Mar 2026 16:41:51 GMT  
		Size: 107.4 MB (107446925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f5fd3754c5815242129333edc3dfe54802c21db21c9a45fc790c6a9b8172d8`  
		Last Modified: Tue, 17 Mar 2026 16:41:48 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:8d764466c7d58fb01a3995142d18fcc8bd62d1a03d85825940f04f9eb639a738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cef44e0f535546c16b2c7410f2f125613bb2a93cbc2ca824e6bc1f1d1434fe9`

```dockerfile
```

-	Layers:
	-	`sha256:70c6bddf414caa062ca9baccfafc22c700c26bfb110a166ff8acc5d275c26195`  
		Last Modified: Tue, 17 Mar 2026 16:41:44 GMT  
		Size: 36.8 KB (36750 bytes)  
		MIME: application/vnd.in-toto+json
