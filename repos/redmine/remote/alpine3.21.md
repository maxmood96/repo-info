## `redmine:alpine3.21`

```console
$ docker pull redmine@sha256:620022a44484ec5cb68a3e140dcf5f23e9496f26a0c8cd0e6ee4a09ad68cd260
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
$ docker pull redmine@sha256:b3a03ccc7e9d5da5f444f054a6ecf0121c8f90066b49b1e78e91760da2a70634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190139505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aeb1c0300a118c771dca864f564032bef92dc2bea74a5228d251d70c9c50d00`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e3c890bd0a98d9ddc8e0e3d0fe5dcb41d57054074a20859db8211db6081990`  
		Last Modified: Wed, 09 Apr 2025 18:34:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8687277ca13255b826908fde58e15c7fd03817c51bca8ba2ee7cf51a78d909b2`  
		Last Modified: Wed, 09 Apr 2025 18:34:22 GMT  
		Size: 35.6 MB (35600444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b73d908b0fc4fb026a775e19801b05f902d97119f08f95b947bf11de6abb7`  
		Last Modified: Wed, 09 Apr 2025 18:34:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474787b6694f9b61744b23dd26e4af319ab3a38c58134719cf88179028d95450`  
		Last Modified: Wed, 09 Apr 2025 19:07:18 GMT  
		Size: 907.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485d285576b443f8e351e2277cf9b575edf5328c282743cf0af43c6cc1cce1aa`  
		Last Modified: Wed, 09 Apr 2025 19:07:20 GMT  
		Size: 72.3 MB (72345972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c8966ff660123eff1cf9e5ec0eb1d80911c030319fc92ad0ba58f40957b24c`  
		Last Modified: Wed, 09 Apr 2025 19:07:18 GMT  
		Size: 1.2 MB (1168357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3c345a1db0cd22bb6f784e1c1b8343c80acdde76ee4ab360f8c3714592c6b1`  
		Last Modified: Wed, 09 Apr 2025 19:07:10 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44479f40a5abbb43023df2b1756c3d97ebeaa67c65de189ff43912020474eae4`  
		Last Modified: Wed, 09 Apr 2025 19:07:10 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f588f241d2c10e286f7387d5711ea7be4c3158d1c0de9990667b7424bf4ada2c`  
		Last Modified: Wed, 09 Apr 2025 19:07:19 GMT  
		Size: 4.1 MB (4057656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a89e8257ca9b64848c2bd6146053c13ead20a108b5c784656eec43f48077e`  
		Last Modified: Wed, 09 Apr 2025 19:07:21 GMT  
		Size: 73.3 MB (73321026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3c7124ff7ed0381ea6e7abf2e200cbc592c983c2cc76261d169c5c64a0d976`  
		Last Modified: Wed, 09 Apr 2025 19:07:20 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:a91a824a80195e5b5f1f1526980ac946b6f09a6aa3f6aecdab0542d7a8bea01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772440be0e97a4e32f6b585ac5354ded58f35fa7c3ae2b6a68cb15ee6a14f3d4`

```dockerfile
```

-	Layers:
	-	`sha256:74c2d244946b3b5eb3d47ef1b4c1ed3d2f35c2e54b7b010eef469a153f71e8e0`  
		Last Modified: Wed, 09 Apr 2025 19:07:18 GMT  
		Size: 38.0 KB (38015 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm variant v6

```console
$ docker pull redmine@sha256:424d9f464d3cb86403331b0197c97f21213e53d2a9bbbd560398269b7d152137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182088623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc7f7cc5076c46b6bb0ba9d977b56a52f54aa27fbcfc51d6661d835016403fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4026b00b6e21fbadf6a8a598214400acf92d3e7692e141b46a55ee0beb504ed5`  
		Last Modified: Sat, 15 Feb 2025 10:12:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6fe7f240d7c7fa4e073ea19c83100f4cda628c4113814d6f9a0f3c2f80b7cd`  
		Last Modified: Wed, 09 Apr 2025 18:44:21 GMT  
		Size: 32.1 MB (32073370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6e2a214dc0a9b750d9b345468ac5c15b4766c4e61692e521c9b362eb57dee1`  
		Last Modified: Wed, 09 Apr 2025 18:44:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f21c7a435e7987f899b520fe8e88d15324616f6a30217850b687711a0b78e1`  
		Last Modified: Wed, 09 Apr 2025 19:09:34 GMT  
		Size: 907.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb4ebd1be9a06e255d5d496ac75ea2eae0eb8b183c7092f9892fea5b0fde41`  
		Last Modified: Wed, 09 Apr 2025 19:09:36 GMT  
		Size: 69.0 MB (68970776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73df992e8d6ab178cc801ecf15e8edb7ef7eb9fdbcf06dd3e8ea5b36d6b66aa`  
		Last Modified: Wed, 09 Apr 2025 19:09:34 GMT  
		Size: 1.1 MB (1134882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fac8618c5f31ab607fc80b6cff48f050e5dd67111b772dce3896072dcad4bdd`  
		Last Modified: Wed, 09 Apr 2025 19:09:34 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f1f6614dcd87cab08151c6dbd961c9b8e0b0772f687941bdcb5617c320b87c`  
		Last Modified: Wed, 09 Apr 2025 19:09:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6fb774e2ad3801140b9cb0a42ddc0f07614823f0dba0353d0d064dfff223f9`  
		Last Modified: Wed, 09 Apr 2025 19:09:35 GMT  
		Size: 4.1 MB (4057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033de0f58c0e585883717187e1a1801a955e2d7181fe8f14771e4687bdbe688d`  
		Last Modified: Wed, 09 Apr 2025 19:09:38 GMT  
		Size: 72.5 MB (72483432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4066fda728b7357da61bf0107c2f7301bad0cdb53424f4daf32218082f3f2f`  
		Last Modified: Wed, 09 Apr 2025 19:09:36 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:2143d7ebb9b228dd7465425c696274fcbf86b257323a0aaffed23fc30899f17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02bf7d443cc5b66a62d10668a0339cb79a476767733cbc2ddf696a4595e314f`

```dockerfile
```

-	Layers:
	-	`sha256:ef0991234dd9bee0cf3746ef3380d1c13f83564b16550c81edc98d95a0bb66ea`  
		Last Modified: Wed, 09 Apr 2025 19:09:33 GMT  
		Size: 38.2 KB (38189 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm variant v7

```console
$ docker pull redmine@sha256:52c808a9e9e69624d805550834c3e8a51ca87ee562f89e205ce0d06f79ab472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177898390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ec0124096b75a65dd188fc8450746fb7e785858605b86ddc70625184d3c0bc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c428f51edf4e52635d4d3ad03cbb076c9509daee6cc3212c8ed31afd484d9e76`  
		Last Modified: Wed, 26 Mar 2025 16:41:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd135dac16709cf2f8071194b02e0003db1ca3eb9e4bff381f15c311e2c92b6`  
		Last Modified: Wed, 09 Apr 2025 21:28:36 GMT  
		Size: 31.9 MB (31916839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4624f71562828a1fae7648783b89e817e515d2df858a5be4a8fecddbe60bf2`  
		Last Modified: Wed, 09 Apr 2025 21:28:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1f0cb91f0aa08a8a0acfe9451767e9494f0e3a02d2edab04179b04de55164d`  
		Last Modified: Wed, 09 Apr 2025 22:15:48 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e389dabfd865bad9b73f1ddd42f4266542057faaaffc05a0657a78ed109a7b73`  
		Last Modified: Wed, 09 Apr 2025 22:15:51 GMT  
		Size: 66.1 MB (66147842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7f1184d4e0b2467524a53174032fd735bf95abdd7a5904fc76ce216eade872`  
		Last Modified: Wed, 09 Apr 2025 22:15:49 GMT  
		Size: 1.1 MB (1134848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277f96072d77d649f1a6005851da7126b3fbfd734b27c1f56807405fce9823ae`  
		Last Modified: Wed, 09 Apr 2025 22:15:49 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac9aa04db2fa4f4b5e02bfbc2409d72c59ebfea4610f4435d758a9b6a62a4c`  
		Last Modified: Wed, 09 Apr 2025 22:15:49 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d66851119a33c5539c050545db4b0e2855aff54fa161697a06de619067592`  
		Last Modified: Wed, 09 Apr 2025 22:15:50 GMT  
		Size: 4.1 MB (4057618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bfd441c48eb83df94cca12b4cde3fa0c239de0c281c7b36dcda1e110e7335e`  
		Last Modified: Wed, 09 Apr 2025 22:15:52 GMT  
		Size: 71.5 MB (71539317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffbf207624cbc17252ed2c430e86585a5f62b5860613509cfdbc717a52f4a13`  
		Last Modified: Wed, 09 Apr 2025 22:15:50 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:df5e952559152987ff64d8218a828ad74124711ca14a9764d2e259b0f90ba53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecd94b8feccf4f3ae06d2c5bb17970721806dbd2e61ae81be57d87d7945516a`

```dockerfile
```

-	Layers:
	-	`sha256:60e8b0238f5f98105edf1a19738efb8817223ee61b07305cce871d0e8745d432`  
		Last Modified: Wed, 09 Apr 2025 22:15:48 GMT  
		Size: 38.2 KB (38189 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:7ed33f9592d06efb8a4db7a2ef49fae8cd34789ed20843cba72702aabd81d8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190021404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d681b4f6a22e109d7336c422c9b413f6f751d2eeb6c221fc086668ec9f9f19a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92e2ad674fb8cdd1e5f317e0e6e8f806017f64b565349bf3b5bdd2bcd56a91e`  
		Last Modified: Wed, 09 Apr 2025 23:39:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a9e7280db7d81229bad7511012e75eb7f5c33921be4753dd6acf74c89433f9`  
		Last Modified: Wed, 09 Apr 2025 23:39:25 GMT  
		Size: 35.5 MB (35522614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c50551f7155bc490bbbd8b142e79ed015f49884747a249c7a16147b4beba744`  
		Last Modified: Wed, 09 Apr 2025 23:39:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1051af1bd296378376f21a5152d8bdf29d31615e1a70b6e21cfa933d258f0c`  
		Last Modified: Thu, 10 Apr 2025 01:56:20 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89015828483b56f02623c800f9e12af91b66a128ac524d3b3bcddc6d6b8c5575`  
		Last Modified: Thu, 10 Apr 2025 01:56:23 GMT  
		Size: 72.0 MB (72028138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7934493d91b838811dd0c3b38c69266b3fc0d8783cf8fafa930a08842cef7b78`  
		Last Modified: Thu, 10 Apr 2025 01:56:20 GMT  
		Size: 1.1 MB (1096495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddbc9ea1b447396eab6b6adc51db00f70674719a9ac7df6a4b821a18007a250`  
		Last Modified: Thu, 10 Apr 2025 01:56:20 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6ccd0d8b01abd56709ff324c3f70d83b7f5b0ac0fbe5cb3c818862f616de0b`  
		Last Modified: Thu, 10 Apr 2025 01:56:21 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c775040cdf28ea6927299712009e57e25e72e7c373b6c9a568a7de9b85a38`  
		Last Modified: Thu, 10 Apr 2025 01:56:22 GMT  
		Size: 4.1 MB (4057532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9db6353b5961e79cde2a42a1e805b783c33200a1799df167c1603b12eb95e9d`  
		Last Modified: Thu, 10 Apr 2025 01:56:25 GMT  
		Size: 73.3 MB (73319791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa052ce51a6dbb1139400738781a16365770ea83af043a244c6910294f84a198`  
		Last Modified: Thu, 10 Apr 2025 01:56:22 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:a9c54f297c128b2d60f180883e66568c26c518a00e9f317588732b63b50432ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f3920773a88789b51c177c2af7f785f242b2490372bb3a20b03cc29c8e23a3`

```dockerfile
```

-	Layers:
	-	`sha256:58161c0d9ab99c228535412e99585c516d97b30c15ee146c876ee2e592156915`  
		Last Modified: Thu, 10 Apr 2025 01:56:20 GMT  
		Size: 38.2 KB (38243 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; 386

```console
$ docker pull redmine@sha256:f405613dc2f2eace54fe8984d6da61fbf33d0c5e1995cdad82c89b34194fe1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187018330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfdc0edfd13593c1c260e1b244b5cfca863116866f126c709a2f25b91698ed8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ad0c10c6768e579e4bc1542e1a80ea0bcdb6fc01ac37ce6d842d64f95141c3`  
		Last Modified: Wed, 09 Apr 2025 18:34:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e936bfa3a90822feb19bc9397bb62032f3387e161879ff2ff3725e2e743c7e60`  
		Last Modified: Wed, 09 Apr 2025 18:34:08 GMT  
		Size: 31.9 MB (31931038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d99239978c24fa5890ae40e24ea55c0b264faaa95158beac2aef96abd11561`  
		Last Modified: Wed, 09 Apr 2025 18:34:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4f5330eead71a5473a6cafc0b7cacccb4f61a6e7a561aea702789cb01007e0`  
		Last Modified: Wed, 09 Apr 2025 19:07:30 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e1eea32aa06ba1db7f3a3dbe5bf002bf15c26e256d2f546d54a31ba95d55c6`  
		Last Modified: Wed, 09 Apr 2025 19:07:32 GMT  
		Size: 73.0 MB (73034152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51cbe09b46ec1917292e975989af7843cd577642b01c8b92e96f72870bb19f0`  
		Last Modified: Wed, 09 Apr 2025 19:07:30 GMT  
		Size: 1.1 MB (1143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d64a893e3d38f7589276675360fdc6b76cbe09fbfd2c3b429a8d2aa7e5dfe94`  
		Last Modified: Wed, 09 Apr 2025 19:07:30 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d29cbb5cbefb563d51dd8b79371c174b4badde40aafb28f07cfc8edc58fa973`  
		Last Modified: Wed, 09 Apr 2025 19:07:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e32d60789f6b986efa72e5650312946f1804a61437ce2f1796d20d60a8f466`  
		Last Modified: Wed, 09 Apr 2025 19:07:31 GMT  
		Size: 4.1 MB (4057612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a04d26d9fe14cedca27f64ddc569daabc3811d3a09cd2c7d1399738dc1877`  
		Last Modified: Wed, 09 Apr 2025 19:07:33 GMT  
		Size: 73.4 MB (73384493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccdd2e734e873064aafadf948a44962b2b3641523f89e4152caf502563794e4`  
		Last Modified: Wed, 09 Apr 2025 19:05:46 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:624681084d1a9875e7d2d0448c81fb9c6b322e1c7c21db049d743daa50ce5075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4319911af62b836a01f92f6e17ebac08b1290117e1ea462226127e0d4d74263`

```dockerfile
```

-	Layers:
	-	`sha256:51fc3a539a852eb22a82b7cb1e6537ccd171ebeda04ed0db389af243b9c27f23`  
		Last Modified: Wed, 09 Apr 2025 19:07:30 GMT  
		Size: 38.0 KB (37954 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; ppc64le

```console
$ docker pull redmine@sha256:016c50c8773d602c781824960c9561c30fce70bed411c8c8b6d65196a6f37845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191308337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c939c03cff14371d4d52dd90db6d330924c0a7da228d0d073269dc94893339ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea103dd62a4b750d38bb38e0e383e2052e1cbeab7d5be5f36cc336b8aa1537b`  
		Last Modified: Wed, 09 Apr 2025 20:05:13 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7620c79e2a7516596c15b0c49ec17d4a0975706220f5801ef182cd3c1eb1c`  
		Last Modified: Wed, 09 Apr 2025 20:05:15 GMT  
		Size: 33.4 MB (33437503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb58e3f03bd226772ca9e32dfc65aef98c5dea8989d7b9cdf371f763f9d5688`  
		Last Modified: Wed, 09 Apr 2025 20:05:14 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f68ad48ae9f1f87f83b7073b545f017f40bd4ea4d74d641f5d9563af6ad982`  
		Last Modified: Wed, 09 Apr 2025 20:34:40 GMT  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42d90ce40f5012647b9d1fa6534de03b2b1caae12167c27b63de8bcb15e510`  
		Last Modified: Wed, 09 Apr 2025 20:34:42 GMT  
		Size: 74.1 MB (74062016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55a20b3d4fe44dcc95a9ecbd0b51d0ce5b01b923a777d082f9e2cde794727c5`  
		Last Modified: Wed, 09 Apr 2025 20:34:40 GMT  
		Size: 1.1 MB (1087040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae3a48a30a3bda990957e1dee5747e865dc69857597c7b30b96273240f8028`  
		Last Modified: Wed, 09 Apr 2025 20:34:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ba78a8933840c227719e20511b3718589a6880555fa20ce2d80dc51529af3e`  
		Last Modified: Wed, 09 Apr 2025 20:34:41 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c039a0f3d6d3e506543ede1f7f263e59861cd0137b40b169fea496c417e64c`  
		Last Modified: Wed, 09 Apr 2025 20:34:42 GMT  
		Size: 4.1 MB (4057705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83b22a0b32b1bd60b20f8ced95026b747c722a3e56da3600663e56fd3786cda`  
		Last Modified: Wed, 09 Apr 2025 20:34:44 GMT  
		Size: 75.1 MB (75085926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4880d082189895e5a2a36fc04acc6787fd55239a70eff0bdf1144e17b1ff3669`  
		Last Modified: Wed, 09 Apr 2025 20:34:42 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:3557b37a7906b5871b4d8063fd98425a4544fc52a2ef886335457ada61592c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1b5b52987fe4507d17279f24b3adf2af421c290a2ea592c5ef858b0a28bad4`

```dockerfile
```

-	Layers:
	-	`sha256:e64cf169b301b158fb48d244d440cdef1406a07b6b5afff61780e4cd98c78693`  
		Last Modified: Wed, 09 Apr 2025 20:34:39 GMT  
		Size: 38.1 KB (38094 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; riscv64

```console
$ docker pull redmine@sha256:61db9220d450cc62eca88e5efa8699754be6972d4783f64c2ee75f4d66d7ee50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188071129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d868d38dd7dfd6ab086992c7328a88a49802cc2ae8eb86ea639711cd213978a6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54551e4382c55dde49be426f193ab43d68f0dc67bbd9d53e416b8b3ec8e530b4`  
		Last Modified: Mon, 17 Feb 2025 02:38:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10350217095e64d8360e35578cdc042053cbb49a0e2ed8c8525c75147d076342`  
		Last Modified: Thu, 10 Apr 2025 01:28:58 GMT  
		Size: 31.7 MB (31729361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e26865ee4f28da5d99b6624385a59deace5f1bdb4d03c841e968da084d8323`  
		Last Modified: Thu, 10 Apr 2025 01:28:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c17784c80d0643345ed8ec79d294fbc8771f2f51325f9d72654509c08135f1b`  
		Last Modified: Thu, 10 Apr 2025 04:54:00 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc4cab0389262240e5d21f08749de4d68d1739dc3989f9510f3f37f4138b2d4`  
		Last Modified: Thu, 10 Apr 2025 04:54:11 GMT  
		Size: 71.1 MB (71135328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13dcf34a2093c09cd0a7b2fcc513a552edb3fc8589ebbdd0bbec1b84580114e`  
		Last Modified: Thu, 10 Apr 2025 04:54:01 GMT  
		Size: 1.1 MB (1136822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890cdadb361dc68ba5ff531f4a2332196f57ce7f37c1335f80342c2e421ab277`  
		Last Modified: Thu, 10 Apr 2025 04:54:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754ecfe2ee943e405ccfb438a3401002cb6fe3240921e13d3e8de392c25b45db`  
		Last Modified: Thu, 10 Apr 2025 04:54:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c5393d3133e22415a5da827d05ab781be375f83a6e9948f89780c98208b08`  
		Last Modified: Thu, 10 Apr 2025 04:54:02 GMT  
		Size: 4.1 MB (4057737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f546701f21b811d2e91e6eb1aea850a00096c08e8a0713dc57131f831aadd099`  
		Last Modified: Thu, 10 Apr 2025 04:54:13 GMT  
		Size: 76.7 MB (76656634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b638c5c9a484adb3c7f75953db6197e7d058429503b46ba814d30d4362889f2c`  
		Last Modified: Thu, 10 Apr 2025 04:54:02 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:738614397738501ec3a0a2f1c3776a1278887ebeaf0440513f168499d495f235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1250eb7d6efb9bb3e6adf23bf97e8f84f145d4a45ce1dd9d75692b1262944241`

```dockerfile
```

-	Layers:
	-	`sha256:2b348b23b09b70d4cbea524bc439274856ff160c8f4f70f50fe483a201e555c1`  
		Last Modified: Thu, 10 Apr 2025 04:54:00 GMT  
		Size: 38.1 KB (38093 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; s390x

```console
$ docker pull redmine@sha256:85a18f14d86eb17b8be37685d6cc40669fda3721f0d3bafb85cf05f8559b8f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189467883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7231156646768ca294d0aae764f20e4b8014ef3384ab74b74ef6bd18214629`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV LANG=C.UTF-8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_VERSION=3.3.8
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 11 Mar 2025 02:53:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_ENV=production
# Tue, 11 Mar 2025 02:53:30 GMT
WORKDIR /usr/src/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
ENV HOME=/home/redmine
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_VERSION=6.0.4
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.4.tar.gz
# Tue, 11 Mar 2025 02:53:30 GMT
ENV REDMINE_DOWNLOAD_SHA256=bebf8acb4fd1843f88e5f4285ff0b497fab43320c33e780a5c34e1124c5e177a
# Tue, 11 Mar 2025 02:53:30 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 11 Mar 2025 02:53:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 02:53:30 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 11 Mar 2025 02:53:30 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10edf43bd954a9237182f66b0b699d1d003f903c1bef832c1852aca487e44816`  
		Last Modified: Wed, 09 Apr 2025 19:54:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d841041ea5e0db420f4846c5873abc07aed0bd5e183b82abdb323c55e3c3c0af`  
		Last Modified: Wed, 09 Apr 2025 19:54:21 GMT  
		Size: 33.2 MB (33224605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cc30f41bd0f01c2ba6bdcdaa76e067efb94ecad8561482e9d8a3619ea53517`  
		Last Modified: Wed, 09 Apr 2025 19:54:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caf2f3ffcf53add0895a8e3c3f9fc8d109f8f2584b624c89bd973cf3cd89244`  
		Last Modified: Wed, 09 Apr 2025 20:25:19 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194ef70a800b6cf67349023b2436cef00c4e2b2c9be6587ce6572b7aa0511527`  
		Last Modified: Wed, 09 Apr 2025 20:25:21 GMT  
		Size: 73.1 MB (73090453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ab8037b13b0e47ebdb99c948d3766a5a5995b0232291b591f3ec0ab38fb7c6`  
		Last Modified: Wed, 09 Apr 2025 20:25:19 GMT  
		Size: 1.1 MB (1131751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1955446863c27fe212f64a0b1759c155b378b3117e816352732bf24cbc7bae99`  
		Last Modified: Wed, 09 Apr 2025 20:25:19 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799355854326a223d9dab9d41ad8be8db6d3a48aba8c369e7da829f9b6730eb3`  
		Last Modified: Wed, 09 Apr 2025 20:25:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8c5754811a9506593b7b215f36c370902fe16959873e54aa75d5d32e547163`  
		Last Modified: Wed, 09 Apr 2025 20:25:20 GMT  
		Size: 4.1 MB (4057610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af667e87a553db813a167a54c70779418f32e24888d013328da2ab52ab287b91`  
		Last Modified: Wed, 09 Apr 2025 20:25:22 GMT  
		Size: 74.5 MB (74492093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa6a20dafdb496d972a6e08acb9e635a94226a6161379382d4941aeb403f934`  
		Last Modified: Wed, 09 Apr 2025 20:25:21 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:84962ff9c4277e67e07b318b128b5fe40154e1d40d30e33e74902fdc74879f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce197442cac6d20fed1585add2194052e80c3657cf5e45c32ba129b6eda19f3b`

```dockerfile
```

-	Layers:
	-	`sha256:bf8f442baa5e51716aa33232294bc040e2ab7afe2913244786f5e784845a515c`  
		Last Modified: Wed, 09 Apr 2025 20:25:19 GMT  
		Size: 38.0 KB (38016 bytes)  
		MIME: application/vnd.in-toto+json
