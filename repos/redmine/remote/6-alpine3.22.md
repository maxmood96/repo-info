## `redmine:6-alpine3.22`

```console
$ docker pull redmine@sha256:3c39ab9a03d9a78aba1bf315d3a58df26c2c1971b60dc840f4e27c9d0ef4337f
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

### `redmine:6-alpine3.22` - linux; amd64

```console
$ docker pull redmine@sha256:7cd0ab8e8d6d9a237221c453b83d3db4a4d902f0efe102698d01660f3835b526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196539599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c8c8c8c7fac783b49d1384b300b106a0dd75b8fd05ab0cbe725059ff26cab9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.3.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:15:35 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:15:35 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV REDMINE_VERSION=6.0.6
# Mon, 07 Jul 2025 22:15:35 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:15:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe3666bfe67f5923c3ce9e753c0a47cb0d52d4479566c9fedbbcdb29c8285e8`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb83df58407229f12cc7c6bf1f2e7504731f6ca7d6a2a5a87d94b2a6efec0331`  
		Last Modified: Tue, 03 Jun 2025 13:30:44 GMT  
		Size: 35.6 MB (35626446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b96e0bde314203f7c2e8598904d1acc64d128a992e7168a703e0c207a9c4dc`  
		Last Modified: Tue, 03 Jun 2025 13:30:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc54e0f5515176b0bd072408594921b2b1676eaf03a311ceb313bd623d21652`  
		Last Modified: Mon, 07 Jul 2025 23:03:27 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc5b0508f56aac2f3acafcd0df83d2bbbe8b785f966dcf6c73915be10a2ac5`  
		Last Modified: Tue, 08 Jul 2025 01:51:45 GMT  
		Size: 75.4 MB (75377498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f482dbbe627faf223bf8dc365e07120ed8fff97578fcb01ce25e4f1e470f2d41`  
		Last Modified: Mon, 07 Jul 2025 23:03:28 GMT  
		Size: 1.2 MB (1168529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd02822bfdb2cf53f5424a68693c40a870caba316c2d813fc290fb438ecdc90`  
		Last Modified: Mon, 07 Jul 2025 23:03:27 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce7f3ef4fbc23d102a209d67820e309c822f49fc0678cf8e3ffa2916229d560`  
		Last Modified: Mon, 07 Jul 2025 23:03:27 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6058bfdf4ad7bf29b215e1fcc2774fcbc655e2d2e941db562e9b0d9e2a32a975`  
		Last Modified: Mon, 07 Jul 2025 23:03:29 GMT  
		Size: 4.1 MB (4067100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68829aa275fdd9f901974f8923f03c100e56a1b5ca1d10fc884b43e39fefa8ff`  
		Last Modified: Mon, 07 Jul 2025 23:03:56 GMT  
		Size: 76.5 MB (76499380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f6047b05c4f8f868134673d45c61e50b7e5100b6a2f46747277f559a06b6d5`  
		Last Modified: Mon, 07 Jul 2025 23:01:49 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:24ec3071a30721af5489f94d5b085a345d6cb60a9e99f6e597a1272b085a7662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2326f77d9d277e5faa1a96c4a2d34febf8c8171ab731bc491afb6afa040fbbf3`

```dockerfile
```

-	Layers:
	-	`sha256:6395cc73f30d01b3ac5596dfc4081102130caab9552bae1282e07d13ef00e358`  
		Last Modified: Tue, 08 Jul 2025 01:51:04 GMT  
		Size: 38.0 KB (38016 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.22` - linux; arm variant v6

```console
$ docker pull redmine@sha256:11dda20b74eb4c45545dba893cafa121489e62aad0492b5799d620b4362f5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185999994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad99354de805caab3527611e2dae82265d429ab4e66a316280df5bfa0ccdafe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.3.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Fri, 30 May 2025 21:26:15 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_ENV=production
# Fri, 30 May 2025 21:26:15 GMT
WORKDIR /usr/src/redmine
# Fri, 30 May 2025 21:26:15 GMT
ENV HOME=/home/redmine
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_VERSION=6.0.5
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 30 May 2025 21:26:15 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 30 May 2025 21:26:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 May 2025 21:26:15 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 30 May 2025 21:26:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c91b400dce72b0b6821109c8cd8b30e2b7f0da467f2906fb512173d0c3b9770`  
		Last Modified: Tue, 03 Jun 2025 23:13:12 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646f0bd62870b6f85299afad929e8d52335e6309714d0f58b3a5c2bbe29d682d`  
		Last Modified: Wed, 04 Jun 2025 01:51:50 GMT  
		Size: 32.1 MB (32094508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357068a3e7b63a7969052d8377f1d172901cb2ccf2af215d619068ae496576dd`  
		Last Modified: Tue, 03 Jun 2025 23:13:18 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071d58efaeee4f9cf0a20485a41c9e0ecfaf1d18e354ce22944156a93345784e`  
		Last Modified: Tue, 03 Jun 2025 23:13:23 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e6b4ea64f72374248e1f3b13d353a51153503f8fa6887ddb56333277c472fe`  
		Last Modified: Wed, 04 Jun 2025 01:51:53 GMT  
		Size: 72.2 MB (72160880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e2cca58c4fe9e1ab4e742e24b807d505ccc6d47bdd8fc5da2cd59e6fd51a47`  
		Last Modified: Tue, 03 Jun 2025 23:13:26 GMT  
		Size: 1.1 MB (1135050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55c764b51d417a77a4b158b0a3c685c850d2fcc52d397c9325136aa26157e6a`  
		Last Modified: Tue, 03 Jun 2025 23:13:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dd350828ebc0e903a1592235389606a3f1067bfb67969951f0d29ebef8edc8`  
		Last Modified: Tue, 03 Jun 2025 23:13:35 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b678341db54e27057eb6d7c88f2d26dfda77045180a93102f17429ade12174`  
		Last Modified: Tue, 03 Jun 2025 23:13:40 GMT  
		Size: 4.1 MB (4063273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e140f6044da72510368842d123ecfc43128fb5550a04d2bb5dce4245488c7794`  
		Last Modified: Wed, 04 Jun 2025 01:51:53 GMT  
		Size: 73.0 MB (73041553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe79c60784f9f5787ee51322c73028c1ab5f4e2c11ed46d111d63bf5f38e658`  
		Last Modified: Tue, 03 Jun 2025 23:16:33 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:1de77d77706ef20dd50771809c9e82f0ad41c5972afd6c587c5eec7d9e905b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031cd60db44bd2ad0ef44b052c64dc8f1c4ec39ac5581b277b93ae2af658c005`

```dockerfile
```

-	Layers:
	-	`sha256:f7e099cc2da97f76c788073530ae21bb3d65f1ce20a4fcc4efd38e647bd37261`  
		Last Modified: Wed, 04 Jun 2025 01:50:50 GMT  
		Size: 38.2 KB (38189 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.22` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0be10899c370350a3927c495b6f825f6a847ef3d86c6831f25fdfdc3ffa9d648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181380290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c11622b9bc5dd490c5f3b72e5a5bcc5ac015591869e7f75867235e5380fcefa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.3.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Fri, 30 May 2025 21:26:15 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_ENV=production
# Fri, 30 May 2025 21:26:15 GMT
WORKDIR /usr/src/redmine
# Fri, 30 May 2025 21:26:15 GMT
ENV HOME=/home/redmine
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_VERSION=6.0.5
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 30 May 2025 21:26:15 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 30 May 2025 21:26:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 May 2025 21:26:15 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 30 May 2025 21:26:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515553b759e392d75aecb0e255f515eac2b780b60c7e96f356592aa5e3a6b63`  
		Last Modified: Tue, 03 Jun 2025 17:47:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2fba5a3feb0dfbd9aa874b9b1917aae5d40529d55c85d126dc041f6cc26acf`  
		Last Modified: Wed, 04 Jun 2025 01:51:50 GMT  
		Size: 31.9 MB (31938115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9376fcad872956b39dd86e9604dafc93a0205fce3edc8075cd4344e8a101ba`  
		Last Modified: Tue, 03 Jun 2025 23:12:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2522e12b0affe2f27404be677839bead204f8771718758d000f244992efc80c1`  
		Last Modified: Tue, 03 Jun 2025 23:07:24 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb66015e52bc48ab0ab63eeb97b16a8aeff5e9886b6fb1447915dbdcbc36eb7`  
		Last Modified: Tue, 03 Jun 2025 23:07:30 GMT  
		Size: 68.9 MB (68930644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90b32ff5fb02bc1d0f49a3e1fcdff278e92dee9581c88d8bbe0bd165fb57060`  
		Last Modified: Tue, 03 Jun 2025 23:07:26 GMT  
		Size: 1.1 MB (1135024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfab885235dedcd139203731dd27c082dd73378fab9ad179505e4997ad8ef7b`  
		Last Modified: Tue, 03 Jun 2025 23:07:26 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4478b9c65432714ad578b9bc5f717fb02d3b574c18b3af841043b1c9d6ea87f4`  
		Last Modified: Tue, 03 Jun 2025 23:07:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777e2f5fcb4ce8621a26f8503971ba84ffb45510f81631b816b9435d596b211a`  
		Last Modified: Tue, 03 Jun 2025 23:07:28 GMT  
		Size: 4.1 MB (4063269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23356c8bd348170383b79bff1c6aeb17f16a90de9d7f7fc6c3c9dcc360021181`  
		Last Modified: Tue, 03 Jun 2025 23:07:32 GMT  
		Size: 72.1 MB (72090256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e10341bf61da275b4b649f7e7322b8ebd60be9d758d96fe27c27b25e82fa215`  
		Last Modified: Tue, 03 Jun 2025 23:07:27 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:17330893866a25284e00283973abce9a3622155fa90bf6277f07d3ba492e05cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631edaa05918c0cc74cf5bd1f8c6a925dec93ac244c36520b3296c5460419f93`

```dockerfile
```

-	Layers:
	-	`sha256:9d3437134f204eafdfaf2da6198074ab7256239127bd8075df55c39c42932026`  
		Last Modified: Wed, 04 Jun 2025 01:50:54 GMT  
		Size: 38.2 KB (38189 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:834f5541d585dfd5e2430457880ea8f4627cd28c9ef3114086bc3f499efc75c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193730335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2020fbf3cfab8ef64dd41e737cd1297b845195beeaedc2aa4f6651a268a2c10e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.3.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Fri, 30 May 2025 21:26:15 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_ENV=production
# Fri, 30 May 2025 21:26:15 GMT
WORKDIR /usr/src/redmine
# Fri, 30 May 2025 21:26:15 GMT
ENV HOME=/home/redmine
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_VERSION=6.0.5
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 30 May 2025 21:26:15 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 30 May 2025 21:26:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 May 2025 21:26:15 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 30 May 2025 21:26:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa1406583f8460034b744a081db0fd06d6f3f1b350a17c5d5c2772f8fc1d5d9`  
		Last Modified: Tue, 03 Jun 2025 13:39:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b243d1f64c739ff9e7f837fc59f1c28e0b616d4f2520239880d794d7670c30`  
		Last Modified: Tue, 03 Jun 2025 14:35:52 GMT  
		Size: 35.5 MB (35544496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd2c1d03f306a7e18020514aeebe9a6c5c3ee3753fdb838a25f2699f59e446c`  
		Last Modified: Tue, 03 Jun 2025 14:35:47 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321f2e37a60a23b2cf173986e38103f58b7567a3533abea3a26c12dbcc3cfbcd`  
		Last Modified: Tue, 03 Jun 2025 23:06:55 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed62e9ae1bee3d13afb69772d146a40dd3a7ff8e1d800fac8caeff86e08a4344`  
		Last Modified: Tue, 03 Jun 2025 23:06:59 GMT  
		Size: 75.0 MB (75016259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e279b5c4d08add6464cf39c34b854cba1b268cafd1758b685f53169dd1dd6a46`  
		Last Modified: Tue, 03 Jun 2025 23:06:56 GMT  
		Size: 1.1 MB (1096884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0b5c264d402930409ea1756b77d1496212abcdfdeae487504ad2ed49eed7aa`  
		Last Modified: Tue, 03 Jun 2025 23:06:56 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03725f151447b6d55c9b84d7452ba920090d7f10206d9e4f43747f0611b7cfee`  
		Last Modified: Tue, 03 Jun 2025 23:06:57 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104a642e4efd6c6bff1ffb2047ac7cf11ac995854d280b4587b2bbf2bc3b0a7c`  
		Last Modified: Tue, 03 Jun 2025 23:06:58 GMT  
		Size: 4.1 MB (4063283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18aa2d383a2b03ea520257442412631d2b723af584d4b4a4c9e84e2832bcba`  
		Last Modified: Tue, 03 Jun 2025 23:07:03 GMT  
		Size: 73.9 MB (73869670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a6890312a196700f9f7506c27199005826acd676523ea96739a79fd9825f0d`  
		Last Modified: Tue, 03 Jun 2025 23:07:00 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:866da80e1dff82f69838d2bf1c30257a3397ba95601e2ee177cabce66a895799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee3f947c8ae00770d749a916d9c4ce221f71b048f6ab0072a83373a07e0bc6f`

```dockerfile
```

-	Layers:
	-	`sha256:08b18ac97197e77f240012b95da4aaa97d7525ac99978c1471b454d82f3fd966`  
		Last Modified: Wed, 04 Jun 2025 01:51:02 GMT  
		Size: 38.2 KB (38243 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.22` - linux; 386

```console
$ docker pull redmine@sha256:b1ebc15473b76c57fcf0ed383b18f3f82809729512d8e68f42eaf5ec8f0d0e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193305610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69413ac91dc263b5af3d72030d9cfe152c35af5bebd25e45ff3ae7394373762f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.3.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:15:35 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:15:35 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV REDMINE_VERSION=6.0.6
# Mon, 07 Jul 2025 22:15:35 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:15:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e287d912492dafed6e51c98339cde44656ca8fbb363b41cf13240d1895562b5`  
		Last Modified: Tue, 03 Jun 2025 23:04:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8c9bb081d6732d87097dffe0c42d442a08574b4e8cab055c1ffe0779894686`  
		Last Modified: Tue, 03 Jun 2025 23:04:12 GMT  
		Size: 32.0 MB (31957126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272d6887a3fbaea18caacb965ae326dcfb991c8a1950419f5481fd5d62bc0a66`  
		Last Modified: Tue, 03 Jun 2025 23:04:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f185feae4d153b7f03e9ed4780004ba79780bbd286c08ab1a24a2647f2f9550e`  
		Last Modified: Mon, 07 Jul 2025 23:03:21 GMT  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07589e038a379e7d3aef69137278faeb1a3b2a24106d3e61435c4d31664545fc`  
		Last Modified: Mon, 07 Jul 2025 23:03:33 GMT  
		Size: 76.2 MB (76154551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f9595eed47f6a77cc0ee614ae78cd5663f6e77d9ee8fbb4ebcb349a26785b`  
		Last Modified: Mon, 07 Jul 2025 23:03:22 GMT  
		Size: 1.1 MB (1143827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9d9765c08cee1bca9466311ed8fa6543a4f1c5d5ad948c934776e8b1fb93f8`  
		Last Modified: Mon, 07 Jul 2025 23:03:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbbee7a3482a595897c0f5c105393339e79442e94f2870e80b72a5a5c8e2f22`  
		Last Modified: Mon, 07 Jul 2025 23:03:22 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d1656cc1d8b4c8e909a8d24843227d520240e7e530c72ba988a46677f9d624`  
		Last Modified: Mon, 07 Jul 2025 23:03:22 GMT  
		Size: 4.1 MB (4067036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710709a0a6271cd08952de6f2391ca8d03e9ec6a3d94a0ab21be7f3cd0204610`  
		Last Modified: Mon, 07 Jul 2025 23:03:26 GMT  
		Size: 76.4 MB (76363241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a075ccca9d6490c76919c04a40f5dc1896b90a8a4dfaa13996d7990dcb727b9d`  
		Last Modified: Mon, 07 Jul 2025 23:02:59 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:4b93845493dfb01dbb375495662855b400ad3a322d0da7d9af77e62aa96299df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3bf8c2d67111e4d9c3cd584bfce4bc0119aa72281c57e7c6e706ac1a765534`

```dockerfile
```

-	Layers:
	-	`sha256:ab601bd755364c25702763cde14ddbfbb4b455b8ab7fff344cb97091e5ad3c7a`  
		Last Modified: Tue, 08 Jul 2025 01:51:18 GMT  
		Size: 38.0 KB (37954 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.22` - linux; ppc64le

```console
$ docker pull redmine@sha256:5093b5ce67e85ef406cd719f68fe0c0685f77fc6c10bffec8bf5cae9703c17d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197959279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5aee21ff4a409ba89d20139a3427ec254dbe8951b17f8a860c34083d41b765`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.3.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GOSU_VERSION=1.17
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RAILS_ENV=production
# Mon, 07 Jul 2025 22:15:35 GMT
WORKDIR /usr/src/redmine
# Mon, 07 Jul 2025 22:15:35 GMT
ENV HOME=/home/redmine
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV REDMINE_VERSION=6.0.6
# Mon, 07 Jul 2025 22:15:35 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.6.tar.gz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV REDMINE_DOWNLOAD_SHA256=b7ac2d28893806b8f4fbd1480b714be546614e830e2029d47a0bf26a352bb3fa
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 07 Jul 2025 22:15:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc492aa09ba6ba094b03567606500b7aa632647756572ee386cf287352e6e8c6`  
		Last Modified: Tue, 03 Jun 2025 23:12:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a72aea8ffd7c5e3c5416e5fca6a9e511c9fdb780717b25d152d11548a265d1`  
		Last Modified: Wed, 04 Jun 2025 01:51:44 GMT  
		Size: 33.5 MB (33462659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fcf79ae2da4c089755c9d8a46cf7dc2e05cec4e567cf68a674a7f81df91ba0`  
		Last Modified: Tue, 03 Jun 2025 23:12:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf944b13f2b68609f8205835e5342f4e25c0beb08d6f386dea9ebaf168bdd30e`  
		Last Modified: Tue, 08 Jul 2025 00:37:32 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb112befb7c335b4c22299bbec10b404f0c8ad9552445eba8c671899b3fa4ad`  
		Last Modified: Tue, 08 Jul 2025 00:37:35 GMT  
		Size: 77.5 MB (77505633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ca3793243d01331171b7ef21188092b546bb99a1b97a71c5550542767a24a0`  
		Last Modified: Tue, 08 Jul 2025 00:37:28 GMT  
		Size: 1.1 MB (1087397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422a2fd72f699e314fa786bdd8c1b54ead0870719765c4127c9ca26bc96e94e`  
		Last Modified: Tue, 08 Jul 2025 00:37:28 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d735c3ee5e876265fa934174a5b70d69f564b849617e8e60229b6afd75b019`  
		Last Modified: Tue, 08 Jul 2025 00:37:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d9a3cfdd9cc06ee02d12e0dc9a5c9fbe25bf6b52b369ff063d2cb5aa7b7eb9`  
		Last Modified: Tue, 08 Jul 2025 00:37:29 GMT  
		Size: 4.1 MB (4067043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69dce6a77e62d1939a85f8330d781abe69429c2c1500f5953726c53456eac0a`  
		Last Modified: Tue, 08 Jul 2025 00:37:37 GMT  
		Size: 78.1 MB (78102557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c16bfbaa590811c0111fb30dea9f6f3360a44bffe5032bf9481d47a1f04c23`  
		Last Modified: Tue, 08 Jul 2025 00:37:29 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:d7c95b927f2e1cdb6640df2ac2efcffcb402305b5de9f27b575e8363ef13371e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe5af16e89567bdadda2c9e3c9ae831999f1dff690eef680ed469eb78fe4a9b`

```dockerfile
```

-	Layers:
	-	`sha256:b9abdb99c0cdf00b3cf93002ea58c93afcbd1cca66b676a58e7cf3c90556280b`  
		Last Modified: Tue, 08 Jul 2025 01:51:22 GMT  
		Size: 38.1 KB (38092 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.22` - linux; riscv64

```console
$ docker pull redmine@sha256:b3c31a934b3cc9b810b5a7c822823078d29e5ad540dea30006866a2a3928f85c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189972861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0070c4fc216c2828a2c5a2108ebda92bca3056fd64c29e8d1447e290756ebf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.3.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Fri, 30 May 2025 21:26:15 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_ENV=production
# Fri, 30 May 2025 21:26:15 GMT
WORKDIR /usr/src/redmine
# Fri, 30 May 2025 21:26:15 GMT
ENV HOME=/home/redmine
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_VERSION=6.0.5
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 30 May 2025 21:26:15 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 30 May 2025 21:26:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 May 2025 21:26:15 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 30 May 2025 21:26:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b27f4dcb19381de3632bdf83ba047ff02e37c9fec5aa239238c22a48c3abba`  
		Last Modified: Wed, 04 Jun 2025 00:11:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c5552d7b6b64542203b178f5cd36efcdbe03cf0a05481f0c9a1583b97fbd5f`  
		Last Modified: Wed, 04 Jun 2025 01:51:43 GMT  
		Size: 31.8 MB (31758694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b24f0bad155a697942a113d82baa8082c31d48d245c7986a857e4973d14c83`  
		Last Modified: Wed, 04 Jun 2025 00:11:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67f1297bbd487e9c45dcb6bd4c39907359cb8ecbef793b52b36d1e91b45d8f`  
		Last Modified: Wed, 04 Jun 2025 00:06:43 GMT  
		Size: 916.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2506e8875b7ec922606ef1fb277762d2d5b69d3ac4f8e821dc46ac8b183034`  
		Last Modified: Wed, 04 Jun 2025 00:06:47 GMT  
		Size: 72.3 MB (72289203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36f7f0f58e873c9d971c59b4e38e5b450de5aee6151bf5e509c0dd890600153`  
		Last Modified: Wed, 04 Jun 2025 00:06:44 GMT  
		Size: 1.1 MB (1137240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372cff246293b6dce1b0c48b6d57abd459e04216412a064b947b7d7d59fa097`  
		Last Modified: Wed, 04 Jun 2025 00:06:44 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049263eac2c1a5a6465db9f5209c2b0be6257627aeed488478a6e2ed6dfe6627`  
		Last Modified: Wed, 04 Jun 2025 00:06:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b368af78f13766b964a3a66dc096fd4cc7034609083db949a9c735905b0b07e7`  
		Last Modified: Wed, 04 Jun 2025 00:06:45 GMT  
		Size: 4.1 MB (4063302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c41741839dbe6e8eaeac115d03518afc9c0cea3b956732607253e9302d26ec`  
		Last Modified: Wed, 04 Jun 2025 00:06:50 GMT  
		Size: 77.2 MB (77206801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af60b1cc8ef8a10591adf8c91efd64e82a9de62b7f08707e9482c88e911d5cd`  
		Last Modified: Wed, 04 Jun 2025 00:06:46 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:1782f4da44caa9799321e8a90df6f7dbab09a2ccb3e00649dfc32c432218d21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a86f3dfdbc10ac3cb059c51d671e9b8266e94c50824886aba8008c7db551fe5`

```dockerfile
```

-	Layers:
	-	`sha256:e9ed31eb79b5c43c26f3fac0287030f494cda5a7a5f9ee9c59cbe1e79c209fa2`  
		Last Modified: Wed, 04 Jun 2025 01:51:21 GMT  
		Size: 38.1 KB (38093 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.22` - linux; s390x

```console
$ docker pull redmine@sha256:f82b42465018f33052b2b227e6925f3700702f5245c20beb59dfc9e390a25242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191528245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90236e753934ae15033b1a30153d6b07a90b9d7dcbd89889557f7701faa39cb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.3.8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.8.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=44ae70fee043da3ce48289b7a52618ebe32dc083253993d486211c7e445c8642
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
# Fri, 30 May 2025 21:26:15 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_ENV=production
# Fri, 30 May 2025 21:26:15 GMT
WORKDIR /usr/src/redmine
# Fri, 30 May 2025 21:26:15 GMT
ENV HOME=/home/redmine
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_VERSION=6.0.5
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.0.5.tar.gz
# Fri, 30 May 2025 21:26:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=94dcc53115e0581ac46e60c3ed9318f1926ce464babbb385e5236217d1e6a64e
# Fri, 30 May 2025 21:26:15 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/assets public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Fri, 30 May 2025 21:26:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 30 May 2025 21:26:15 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 30 May 2025 21:26:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 30 May 2025 21:26:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 30 May 2025 21:26:15 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 30 May 2025 21:26:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0d9969f70d5a36f4277e7e9319832436722d175377dcf99975210c3a9b5eeb`  
		Last Modified: Tue, 03 Jun 2025 23:15:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea19575e8d8743912df3d07deec43874e4a9f175e5a2b4dbe8d3b525266fba7`  
		Last Modified: Wed, 04 Jun 2025 01:51:44 GMT  
		Size: 33.2 MB (33246913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745a9edf4a72cd71a17b85d0a3d86d6c835f7edcf57ea6ae001719cebb7f0ebf`  
		Last Modified: Tue, 03 Jun 2025 23:21:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5933fc92c8ef43566c1683243c607951a11b32be8f44dd557abfe678abe42f91`  
		Last Modified: Tue, 03 Jun 2025 23:08:09 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3c61abba2e119a1ff3b40336c96f9369d8386dfa62868c678af17e91b0e16b`  
		Last Modified: Tue, 03 Jun 2025 23:08:14 GMT  
		Size: 74.4 MB (74379015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa4b0789a1d043d9f13c144cb9023cdef8ace0a9af80aa28143fb98811a7d40`  
		Last Modified: Tue, 03 Jun 2025 23:08:10 GMT  
		Size: 1.1 MB (1131805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a52cdd05b0fc503eb4febe6d6808b6560c9b46df238812ee446e3173be9e3c6`  
		Last Modified: Tue, 03 Jun 2025 23:08:10 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56666a2866cfe3c792a0cb2419741e72604fa9d5b29f1c0cf654c2d36192251`  
		Last Modified: Tue, 03 Jun 2025 23:08:11 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4f74e3cc6fa04e18b462e155f5359681e58d5561ee051742ebfeea439d5fba`  
		Last Modified: Tue, 03 Jun 2025 23:08:13 GMT  
		Size: 4.1 MB (4063090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0789a94ea6d6fb1108549f1b885302488968a881e220e8eddaa90965473c83fe`  
		Last Modified: Tue, 03 Jun 2025 23:08:16 GMT  
		Size: 75.1 MB (75056087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936000a596b3314cfa81e2d1383a1854a539cb5a73ab98a06d9fe64442c1e4fd`  
		Last Modified: Tue, 03 Jun 2025 23:08:13 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.22` - unknown; unknown

```console
$ docker pull redmine@sha256:ceb65f31b7a55166b22fa7e7a4929fe5840c315a6b798421c74b127487c233c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (38016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9ada3d032b8b2b62a182bed6dd8421104c8901deccb0bee0169409c428fbb6`

```dockerfile
```

-	Layers:
	-	`sha256:0d80155a70e299d8b46c58c9c79a06498d8ce19569d24f34704ee34ffc016174`  
		Last Modified: Wed, 04 Jun 2025 01:51:30 GMT  
		Size: 38.0 KB (38016 bytes)  
		MIME: application/vnd.in-toto+json
