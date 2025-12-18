## `redmine:6-alpine3.23`

```console
$ docker pull redmine@sha256:c109c7c97cf3ccabc853dc605e6c13b7d1c82ed775add6835ee3bd7df0a31968
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

### `redmine:6-alpine3.23` - linux; amd64

```console
$ docker pull redmine@sha256:b2d9e15a77fe99522855c393836a2202f0658981ac1e5e9062200962fdba46c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198518831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7201c42b8a2b5cbbfbcea1d2d6e2dccdfd5b6cae3fbbe0b943f9f8a4a7e2fce6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:42:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 00:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:44:38 GMT
ENV RUBY_VERSION=3.4.8
# Thu, 18 Dec 2025 00:44:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Thu, 18 Dec 2025 00:44:38 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Thu, 18 Dec 2025 00:44:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 00:44:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 00:44:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 00:44:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:44:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 00:44:38 GMT
CMD ["irb"]
# Thu, 18 Dec 2025 01:24:50 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 18 Dec 2025 01:24:53 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 18 Dec 2025 01:24:56 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:24:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:24:56 GMT
ENV RAILS_ENV=production
# Thu, 18 Dec 2025 01:24:56 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Dec 2025 01:24:56 GMT
ENV HOME=/home/redmine
# Thu, 18 Dec 2025 01:24:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 18 Dec 2025 01:24:56 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 18 Dec 2025 01:24:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 18 Dec 2025 01:24:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 18 Dec 2025 01:24:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 18 Dec 2025 01:24:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 18 Dec 2025 01:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:25:34 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Dec 2025 01:25:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:25:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:25:34 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 18 Dec 2025 01:25:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dee478813cad31569e4d69199ad015affc3f1cac05aeeedd7cf45fb500d5d8`  
		Last Modified: Thu, 18 Dec 2025 00:44:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a172f940b4a127f04d73f2276a1707d8a7fb8b816f3e61662df936867c2853af`  
		Last Modified: Thu, 18 Dec 2025 00:44:56 GMT  
		Size: 39.2 MB (39186975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55926069c974cad8dde8fca4c52ab0262f5ea5c4e3fe31c6e44066103da43d36`  
		Last Modified: Thu, 18 Dec 2025 00:44:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd10f19b78938ee06629767dad82cf07267d94032620a57b134631e95507cf38`  
		Last Modified: Thu, 18 Dec 2025 01:25:54 GMT  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1970d2e325e926cc0b49937a458c1889990d722f2f913654db2dd19ff04764`  
		Last Modified: Thu, 18 Dec 2025 01:26:01 GMT  
		Size: 79.0 MB (79019114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42042bdec23591f8a51c5c377cc939d4726c3394a818463726289f714b4891a6`  
		Last Modified: Thu, 18 Dec 2025 01:25:54 GMT  
		Size: 976.0 KB (975973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a0b8f5e486aa90033ab3c8893b4477b5408d87f93f0199123d4fae38808ad1`  
		Last Modified: Thu, 18 Dec 2025 01:25:54 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b324aeb00501aa674765526fbffe38761d401d0581d79849d1d0ffd16a0db754`  
		Last Modified: Thu, 18 Dec 2025 01:25:54 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80810f7f9ee0958ed46ba6ba2c5c49a69078309c7d44ca842d0e84a5d4d6048c`  
		Last Modified: Thu, 18 Dec 2025 01:25:55 GMT  
		Size: 4.1 MB (4140879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c0168c9c4f391e4ca0b8d5789e618b879dc11a3c505ef98dab108d7c12f2b2`  
		Last Modified: Thu, 18 Dec 2025 01:26:01 GMT  
		Size: 71.3 MB (71331877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59294667ff264e8408d4fd514272672c72ff4418e5c9f5b4b93aab68f1971f9d`  
		Last Modified: Thu, 18 Dec 2025 01:25:54 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:0d8e39c698ab5e0e0dad8aa8d57a6c978d1cbf8af72fd707627866bb7ddd5f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200d331d34658961e2b4ac5a553d507dba9413760f1d11433a098f46c0110afd`

```dockerfile
```

-	Layers:
	-	`sha256:f4f2335a430f4879b924442b838865ae1eaff28645bb5e218fe858e09d884ba3`  
		Last Modified: Thu, 18 Dec 2025 02:50:35 GMT  
		Size: 38.0 KB (37972 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.23` - linux; arm variant v7

```console
$ docker pull redmine@sha256:4f75e72e959ef12261dcdb2ff95862fb675dd4cf3fe9de95f3088eaba58421bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201841749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0201ce4ac14c12b9b93b358e71afaed46c8d8d471a71722f469cdf856c5f8302`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:06:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 01:08:39 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:08:39 GMT
ENV RUBY_VERSION=3.4.8
# Thu, 18 Dec 2025 01:08:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Thu, 18 Dec 2025 01:08:39 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Thu, 18 Dec 2025 01:08:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 01:08:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 01:08:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 01:08:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:08:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 01:08:39 GMT
CMD ["irb"]
# Thu, 18 Dec 2025 01:45:49 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 18 Dec 2025 01:45:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 18 Dec 2025 01:45:55 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:45:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:45:55 GMT
ENV RAILS_ENV=production
# Thu, 18 Dec 2025 01:45:55 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Dec 2025 01:45:55 GMT
ENV HOME=/home/redmine
# Thu, 18 Dec 2025 01:45:55 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 18 Dec 2025 01:45:55 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 18 Dec 2025 01:45:55 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 18 Dec 2025 01:45:55 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 18 Dec 2025 01:45:55 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 18 Dec 2025 01:45:58 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 18 Dec 2025 01:47:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:47:11 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Dec 2025 01:47:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:47:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:47:11 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 18 Dec 2025 01:47:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272dcc4e0d1564280edf75c6ea2b75b947ebea95603652bf67e47decf243cf74`  
		Last Modified: Thu, 18 Dec 2025 01:08:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1a95143ff5da4f4450c38afe21fa5a43fdc20554e27991efb761785565b338`  
		Last Modified: Thu, 18 Dec 2025 01:08:59 GMT  
		Size: 34.7 MB (34691206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5459737b6ddd6a5390d299a0b9f554141581ee5d28dba38083d2b9f347f05946`  
		Last Modified: Thu, 18 Dec 2025 01:08:53 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec936ab5fed6f4c4c8174bc548ec0ff94eabcea036b5bebc364968f5b1f9d083`  
		Last Modified: Thu, 18 Dec 2025 01:47:31 GMT  
		Size: 907.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c843bc63e134220825bdc2e929d9f05283dcc0c05de9b7d6a10a93531ee76118`  
		Last Modified: Thu, 18 Dec 2025 01:47:43 GMT  
		Size: 71.9 MB (71946309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c5be9bcce9948887d6adbc9a170cefaf1772517073bca000a60c38ab139482`  
		Last Modified: Thu, 18 Dec 2025 01:47:31 GMT  
		Size: 942.3 KB (942326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31263bdface628778eaa4fd371250011a47e02c7aa46ba05cf227e22685214f`  
		Last Modified: Thu, 18 Dec 2025 01:47:31 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07841916047c2c9ea411e34caea325b213fba84179f407b59daf7447c7d74bb6`  
		Last Modified: Thu, 18 Dec 2025 01:47:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb468b955564c8b04a9df8ceeb327b59aab2c5e494f596d13b9fb05968fa6e9`  
		Last Modified: Thu, 18 Dec 2025 01:47:31 GMT  
		Size: 4.1 MB (4140876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595e3ca11363e0d0231bcb9c6fad269f15d9ba0c9a8891c32f2d8ac89b4fb058`  
		Last Modified: Thu, 18 Dec 2025 01:47:37 GMT  
		Size: 86.8 MB (86837734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b560d78c93b38ec29998ad3d9a93c6cde7ffc4d969efaa2d6ff384ed1791c049`  
		Last Modified: Thu, 18 Dec 2025 01:47:31 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:95ed2df33b58d15beced79b8bf61a7b6f9330641080556659e39ef9d0f85971d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62efdeccb94b79671308d96fec854c07c3fc62e9162d40d60bbb7cb80736ab8`

```dockerfile
```

-	Layers:
	-	`sha256:31bc5167c1ecdd929fa1d792c414d4106a36dc0b37033c8b64f588d123b9496c`  
		Last Modified: Thu, 18 Dec 2025 02:50:38 GMT  
		Size: 38.1 KB (38149 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:01aed093ff5b875a3764f80ace97524f531bd4b8f7841b6929eb459129815b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198187339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1c6f42cbab8add0cba97c1c4082876c8fe1bf6dc8ddbc61b16710c4aa8d28d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 00:50:21 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:50:21 GMT
ENV RUBY_VERSION=3.4.8
# Thu, 18 Dec 2025 00:50:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Thu, 18 Dec 2025 00:50:21 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Thu, 18 Dec 2025 00:50:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 00:50:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 00:50:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 00:50:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:50:21 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 00:50:21 GMT
CMD ["irb"]
# Thu, 18 Dec 2025 01:34:42 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 18 Dec 2025 01:34:46 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 18 Dec 2025 01:34:48 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:34:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:34:48 GMT
ENV RAILS_ENV=production
# Thu, 18 Dec 2025 01:34:48 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Dec 2025 01:34:48 GMT
ENV HOME=/home/redmine
# Thu, 18 Dec 2025 01:34:48 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 18 Dec 2025 01:34:48 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 18 Dec 2025 01:34:48 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 18 Dec 2025 01:34:48 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 18 Dec 2025 01:34:48 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 18 Dec 2025 01:34:51 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 18 Dec 2025 01:35:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:35:50 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Dec 2025 01:35:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:35:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:35:50 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 18 Dec 2025 01:35:50 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01602b49444121722965904689e3e1d54456c2c79ff93e1056574caafa558deb`  
		Last Modified: Thu, 18 Dec 2025 00:50:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323ad24c22442dedd73fbb6ddc0fd996530d3b221d08c5e623b489e3c38fe180`  
		Last Modified: Thu, 18 Dec 2025 00:50:41 GMT  
		Size: 39.3 MB (39250531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f76048f00bc1a655d522a168484d81a8d66ef631a8fbf45576877132b47d836`  
		Last Modified: Thu, 18 Dec 2025 00:50:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a81ed1817bb9487224b24d0ce802a7c17e623ed06ead566eb452e851ffc6325`  
		Last Modified: Thu, 18 Dec 2025 01:36:19 GMT  
		Size: 907.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d436545ce0287ea9d76c14f5f9bc8ac5ff771f0873caed5be8946cebaa8e6c1`  
		Last Modified: Thu, 18 Dec 2025 01:36:27 GMT  
		Size: 78.5 MB (78528821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498e4c14ee2a93b3a3f2eb1941eab11af53c47569b56e6d49f639758dbb6ca2c`  
		Last Modified: Thu, 18 Dec 2025 01:36:19 GMT  
		Size: 929.4 KB (929396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcc529545d1f4052e3be0e2fe46007ce5be82a9f39ab41c72e071d0c3af507`  
		Last Modified: Thu, 18 Dec 2025 01:36:19 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a09632378a21eb7404aac3cd843f57c529c9b68e4c4898691eef61388e73958`  
		Last Modified: Thu, 18 Dec 2025 01:36:19 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f76c575ef8c8e90ccbf6b602bb1ecfdc68ecd3ffe55af8d80d40b070af333c`  
		Last Modified: Thu, 18 Dec 2025 01:36:20 GMT  
		Size: 4.1 MB (4140886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4923f31c78df5445011a1ee4a6f078b892b37b52f734165cc485de7495e99dae`  
		Last Modified: Thu, 18 Dec 2025 01:36:40 GMT  
		Size: 71.1 MB (71138058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d5c0da38ef13e992a1baf7aa6f84c66094f998d6b4cf639b90128a9f3a3e25`  
		Last Modified: Thu, 18 Dec 2025 01:36:19 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:058e06725e0814304db57fd03b93d6f7a2b7358c3974f44818188e2afc3702ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f941e2dafb96157bb49e76ee416716ac300369c28e0bf00b3ee73e356365f7a3`

```dockerfile
```

-	Layers:
	-	`sha256:09a37886a8a6b83d7d5cd9cfb49d27cb718760ae4119da4d6f9daf74f68ed01a`  
		Last Modified: Thu, 18 Dec 2025 02:50:42 GMT  
		Size: 38.2 KB (38199 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.23` - linux; 386

```console
$ docker pull redmine@sha256:e2aade3e8ce2f6badf84d9dfc069c023c47953fbc96d8b38bc1a7c57dce6a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216397850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f6179c7d729f15091a47813e9a832e050665068679571ce0920555078bfa83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:41:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 00:43:55 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:43:55 GMT
ENV RUBY_VERSION=3.4.8
# Thu, 18 Dec 2025 00:43:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Thu, 18 Dec 2025 00:43:55 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Thu, 18 Dec 2025 00:43:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 00:43:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 00:43:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 00:43:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:43:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 00:43:56 GMT
CMD ["irb"]
# Thu, 18 Dec 2025 01:20:16 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 18 Dec 2025 01:20:19 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 18 Dec 2025 01:20:22 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:20:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:20:22 GMT
ENV RAILS_ENV=production
# Thu, 18 Dec 2025 01:20:22 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Dec 2025 01:20:22 GMT
ENV HOME=/home/redmine
# Thu, 18 Dec 2025 01:20:22 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 18 Dec 2025 01:20:22 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 18 Dec 2025 01:20:22 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 18 Dec 2025 01:20:22 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 18 Dec 2025 01:20:22 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 18 Dec 2025 01:20:24 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 18 Dec 2025 01:22:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 01:22:17 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Dec 2025 01:22:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:22:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:22:17 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 18 Dec 2025 01:22:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a7bb8d64a668c3f8a290660f3dcb54c013d83027e08e2e9e1f0ed94ce71a5c`  
		Last Modified: Thu, 18 Dec 2025 00:44:10 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8b0bcb1062f4665890a01abf432d1ec6297f0e67208e2af10c9ec08fb99bd5`  
		Last Modified: Thu, 18 Dec 2025 00:44:14 GMT  
		Size: 34.7 MB (34663151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6c07b76037f4527c5b484f276ec51f0f36217f142556034668a49d88cdaeae`  
		Last Modified: Thu, 18 Dec 2025 00:44:10 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2367d5de3370b485d3753c5861f4d22e11f593d95853ddaeae5a3c3d27a77a4`  
		Last Modified: Thu, 18 Dec 2025 01:22:40 GMT  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accfa57196a735e6a87baee73c6b4a684c53dd6f935b1a2b43ec7fac03d507ec`  
		Last Modified: Thu, 18 Dec 2025 01:22:47 GMT  
		Size: 80.1 MB (80050453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476f5f45366c39abe16eb7e368cbf5a4cd949d9f461adbc9489485ae2b5de5a7`  
		Last Modified: Thu, 18 Dec 2025 01:22:40 GMT  
		Size: 945.9 KB (945926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c44b284ae8acc7192201ea42ba9eeadf1e1ce4a17bd9045432992bc3d2a578`  
		Last Modified: Thu, 18 Dec 2025 02:04:09 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8795cae1f4453ea1d41bc7e6c09909f6969544102ef526683a87480182d1e24`  
		Last Modified: Thu, 18 Dec 2025 01:22:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d1eebfe1b1a3c4cd0ba4b425e15daec9db4798c4c84e39e669e21d8ca0e8`  
		Last Modified: Thu, 18 Dec 2025 01:22:40 GMT  
		Size: 4.1 MB (4140882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f0f4ece49b0bf7b66d270680ae5561471c4ecce642e5039b66d74ebd0d27aa`  
		Last Modified: Thu, 18 Dec 2025 01:22:50 GMT  
		Size: 92.9 MB (92907429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf0d8fa805c5c6d78e59023c837972a924ff7df01a470a4087844c44ba7950a`  
		Last Modified: Thu, 18 Dec 2025 01:22:39 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:59d192c90eb6c452b89a1ec9dfdc9d6f300351b446decc769d1c99eb372bcaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2852571fa915531357e6a97b31bd166dbf3e89ffda8de3670f72bb30dcfcdc6c`

```dockerfile
```

-	Layers:
	-	`sha256:c43e56e5a51308f641f518ed5e612e609cd389a824b60880e8049f480c6f4a5a`  
		Last Modified: Thu, 18 Dec 2025 02:50:45 GMT  
		Size: 37.9 KB (37909 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.23` - linux; ppc64le

```console
$ docker pull redmine@sha256:36cf9ab43ec224848ce380b85a1ee7b0e626de1ca33a899cf4ad508d2215ebab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235545071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e430bb2cac184a22d8c8237ba09390f383683e9dff3d3cc9cb4c0e5e96fa3a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 02:15:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 02:19:28 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 02:19:28 GMT
ENV RUBY_VERSION=3.4.8
# Thu, 18 Dec 2025 02:19:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Thu, 18 Dec 2025 02:19:28 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Thu, 18 Dec 2025 02:19:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 02:19:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 02:19:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 02:19:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:19:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 02:19:28 GMT
CMD ["irb"]
# Thu, 18 Dec 2025 03:43:36 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 18 Dec 2025 03:43:44 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 18 Dec 2025 03:43:49 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 03:43:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 03:43:49 GMT
ENV RAILS_ENV=production
# Thu, 18 Dec 2025 03:43:49 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Dec 2025 03:43:49 GMT
ENV HOME=/home/redmine
# Thu, 18 Dec 2025 03:43:50 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 18 Dec 2025 03:43:50 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 18 Dec 2025 03:43:50 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 18 Dec 2025 03:43:50 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 18 Dec 2025 03:43:50 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 18 Dec 2025 03:43:54 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 18 Dec 2025 03:47:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 03:47:45 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Dec 2025 03:47:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 03:47:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 03:47:45 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 18 Dec 2025 03:47:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88abe07392db9c99b7985917f40fed1c93e02a070b1b6bb385e5d989f194b364`  
		Last Modified: Thu, 18 Dec 2025 02:19:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd35f802aa8491fbfdb85d54ca27016cad72806a95b88b8edae2109ec9fe0d25`  
		Last Modified: Thu, 18 Dec 2025 02:19:58 GMT  
		Size: 36.6 MB (36559995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c03de85e50bd0d5b6342e844497eaaea47eec8bf74d2cce4dbb12cfe5f8664`  
		Last Modified: Thu, 18 Dec 2025 02:19:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f809dfd8f958651556ce7a72879e4b97acebd9666fc5419268cd03c8cff9aa4`  
		Last Modified: Thu, 18 Dec 2025 03:48:21 GMT  
		Size: 907.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134e8b75e7e0b9d41e3edec551d6dc117c5eed739693d7d8fe0ab9b2dbc22997`  
		Last Modified: Thu, 18 Dec 2025 03:48:31 GMT  
		Size: 81.6 MB (81631498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78af5d87185befde8c553078d7ed63c508ae7b4774968bd3877bb1f815f5dd6`  
		Last Modified: Thu, 18 Dec 2025 03:48:22 GMT  
		Size: 934.5 KB (934450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a5ab061bd8ef31007f36b0f13aebb49aefb319763dd3308f696916d67da5d0`  
		Last Modified: Thu, 18 Dec 2025 03:48:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67e141f62844e1943b369cefbfe4cacefd14ccf38faaa1794ed24a0f00e4cb0`  
		Last Modified: Thu, 18 Dec 2025 03:48:21 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fa8fbb95c3b74baecdf2dff91fce05a3d801db8a49318ac92fe0aaf12a844b`  
		Last Modified: Thu, 18 Dec 2025 03:48:22 GMT  
		Size: 4.1 MB (4140873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1da25feb3045221834e56f5c2bd85054a91a6396527577d77cb2d8f6bd5bdcb`  
		Last Modified: Thu, 18 Dec 2025 03:48:31 GMT  
		Size: 108.4 MB (108446592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f69ee9be9a6e8e94607c755d05b95a22fa790a85284ef280ce9e9fc90103ec0`  
		Last Modified: Thu, 18 Dec 2025 03:48:21 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:868e6c86eeed505704b2c4daf57e1a96b19630864bd3e05f736a47289bc9d06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e111b53e9511e58d06fc6bd96437798dce1c8b9869963ec1a4d977ce7cd25368`

```dockerfile
```

-	Layers:
	-	`sha256:e4e1a4d6f52611e9070a880170b64112da9082bd1619101c8543b9af6bff1230`  
		Last Modified: Thu, 18 Dec 2025 05:50:25 GMT  
		Size: 38.1 KB (38052 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.23` - linux; riscv64

```console
$ docker pull redmine@sha256:74faa18f08a86b35e0b69865775aa9e7e7cc7c8efbc68e67684400cfa67a79c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230647197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca0824dd2af82e70575acab403c56b5ea03800ab0ffa439ebad56feada66c70`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Fri, 05 Dec 2025 11:47:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 13 Dec 2025 08:17:23 GMT
ENV LANG=C.UTF-8
# Sat, 13 Dec 2025 08:17:23 GMT
ENV RUBY_VERSION=3.4.7
# Sat, 13 Dec 2025 08:17:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Sat, 13 Dec 2025 08:17:23 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Sat, 13 Dec 2025 08:17:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 13 Dec 2025 08:17:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 13 Dec 2025 08:17:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 13 Dec 2025 08:17:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 08:17:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 13 Dec 2025 08:17:23 GMT
CMD ["irb"]
# Sun, 14 Dec 2025 18:30:23 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Sun, 14 Dec 2025 18:30:55 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Sun, 14 Dec 2025 18:31:05 GMT
ENV GOSU_VERSION=1.19
# Sun, 14 Dec 2025 18:31:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 14 Dec 2025 18:31:05 GMT
ENV RAILS_ENV=production
# Sun, 14 Dec 2025 18:31:06 GMT
WORKDIR /usr/src/redmine
# Sun, 14 Dec 2025 18:31:06 GMT
ENV HOME=/home/redmine
# Sun, 14 Dec 2025 18:31:06 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sun, 14 Dec 2025 18:31:06 GMT
ENV REDMINE_VERSION=6.1.0
# Sun, 14 Dec 2025 18:31:06 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Sun, 14 Dec 2025 18:31:06 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Sun, 14 Dec 2025 18:31:06 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Sun, 14 Dec 2025 18:31:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Sun, 14 Dec 2025 19:50:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sun, 14 Dec 2025 19:50:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 14 Dec 2025 19:50:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Sun, 14 Dec 2025 19:50:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 14 Dec 2025 19:50:07 GMT
EXPOSE map[3000/tcp:{}]
# Sun, 14 Dec 2025 19:50:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d6d4a2098480dce5e09584f8cb661c8870cb4aaae9283038b1bc4b94f4bd51`  
		Last Modified: Fri, 05 Dec 2025 14:01:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb708ddfc2eb045b363df6f155be5bb5d7e398dcf44dd12e21cbbd4d0099189`  
		Last Modified: Sat, 13 Dec 2025 08:18:59 GMT  
		Size: 38.3 MB (38266398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5dec898fa817e7efeba5dcb729e6811105f74b60364b932528611097d8f72a`  
		Last Modified: Sat, 13 Dec 2025 08:18:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed49f3b3589c92ab39d9de99f6c1aa60401d20a9262fabdc24f14519474d8d87`  
		Last Modified: Sun, 14 Dec 2025 19:53:11 GMT  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d22dfb4e36694cce1fbe60bc956af0769a4cd2c9efc8e4ad1764a9a836b46d`  
		Last Modified: Sun, 14 Dec 2025 19:53:18 GMT  
		Size: 77.2 MB (77246730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403481ffe83b09f9c610de46ac6bcf2b5d3cd78a372d2030c07bef475a8913be`  
		Last Modified: Sun, 14 Dec 2025 19:53:11 GMT  
		Size: 921.7 KB (921726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c173b0896ad80b8bf6a2462e953d9361883bf38caa9f4a69609c751b096399ba`  
		Last Modified: Sun, 14 Dec 2025 19:53:11 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1730fab24a1f442dd3e24855cd4c7b17e3d105d3a9f7ea8acce2d58b140682d7`  
		Last Modified: Sun, 14 Dec 2025 19:53:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd309194c871fde0ee7d07dfd390d5a50dfe1818191b3844977b87568bdbcaa`  
		Last Modified: Sun, 14 Dec 2025 19:53:11 GMT  
		Size: 4.1 MB (4140848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a63172281e02a913c3cddcac45e0c61ba566e820568ca1b25594bb7bff1122`  
		Last Modified: Sun, 14 Dec 2025 19:53:21 GMT  
		Size: 106.5 MB (106484067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89c4a30f1ec62abfccc93629c0b77cc8d6a68eb0ef350586c81a5b207619827`  
		Last Modified: Sun, 14 Dec 2025 19:53:11 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:d1164a4c994bf862468952fbf32917207a17070bdb6536be857164d84d22ec54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3e5bdd5f5fab004237ed0ee701841833629c227c09d7c417436bd9ed30b189`

```dockerfile
```

-	Layers:
	-	`sha256:b6c5c91c67223f050ab9001d8dffff27e6cfe26e852b79e0181dca67db1ac0c9`  
		Last Modified: Sun, 14 Dec 2025 20:50:04 GMT  
		Size: 38.1 KB (38051 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-alpine3.23` - linux; s390x

```console
$ docker pull redmine@sha256:28473a657811abd67518d35415a244d54665bf8f9fae6cec15598050c7122917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231360398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2be79aeb1bac7b2dc30d5c53177ce1833107ace7eed774061de17ccfabe629`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 03:34:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 03:39:25 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 03:39:25 GMT
ENV RUBY_VERSION=3.4.8
# Thu, 18 Dec 2025 03:39:25 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Thu, 18 Dec 2025 03:39:25 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Thu, 18 Dec 2025 03:39:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 03:39:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 03:39:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 03:39:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 03:39:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 03:39:26 GMT
CMD ["irb"]
# Thu, 18 Dec 2025 04:22:07 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Thu, 18 Dec 2025 04:22:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Thu, 18 Dec 2025 04:22:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 04:22:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 04:22:14 GMT
ENV RAILS_ENV=production
# Thu, 18 Dec 2025 04:22:14 GMT
WORKDIR /usr/src/redmine
# Thu, 18 Dec 2025 04:22:14 GMT
ENV HOME=/home/redmine
# Thu, 18 Dec 2025 04:22:14 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Thu, 18 Dec 2025 04:22:14 GMT
ENV REDMINE_VERSION=6.1.0
# Thu, 18 Dec 2025 04:22:14 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Thu, 18 Dec 2025 04:22:14 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Thu, 18 Dec 2025 04:22:14 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Thu, 18 Dec 2025 04:22:16 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Thu, 18 Dec 2025 04:24:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		cargo 		clang19-dev 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		yaml-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			$1 == "libc.so" { next } 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 18 Dec 2025 04:24:49 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 18 Dec 2025 04:24:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 04:24:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 04:24:49 GMT
EXPOSE map[3000/tcp:{}]
# Thu, 18 Dec 2025 04:24:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493c0efcfee1ea79256cd7e7e57a29232fa88c4b2ea4b51a962fa8dfc804b935`  
		Last Modified: Thu, 18 Dec 2025 03:38:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f10b504f28a1bc5f24b9291de65ab19bc4eb396a5287f9bb7ebc411adc22f1`  
		Last Modified: Thu, 18 Dec 2025 03:39:49 GMT  
		Size: 36.1 MB (36054584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f9169ad6b76c862222fa83fc4d9e9f40a0a6d7b17d5b6e7226e240a86b020`  
		Last Modified: Thu, 18 Dec 2025 03:39:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e0d6f65f7de8558c62479aff8ef6420bde7d47ab94df6d69ce6f426b4388a4`  
		Last Modified: Thu, 18 Dec 2025 04:25:14 GMT  
		Size: 908.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cf07f74c3a5d8a75f8079923ee42d169883d863c504c5ce5d7382fff03df42`  
		Last Modified: Thu, 18 Dec 2025 04:25:21 GMT  
		Size: 79.3 MB (79316655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa06d4fcc60ee7e947034d63c560029659fabfd7d387060e33053de551b685`  
		Last Modified: Thu, 18 Dec 2025 04:25:14 GMT  
		Size: 950.2 KB (950223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b326324416aee4346cc37de6fffaef9d193ef75e614d16f3c177c548614996`  
		Last Modified: Thu, 18 Dec 2025 04:25:14 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf4ef466a7ff7ed747f63eafbdab40a7ffe55bce0b3cd4ee3eb4e986abb1869`  
		Last Modified: Thu, 18 Dec 2025 04:25:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e33a228412d865e1cbb01401d11678a5a52de574e73e1e8887e646f6b46ff`  
		Last Modified: Thu, 18 Dec 2025 04:25:15 GMT  
		Size: 4.1 MB (4140919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23f93d1f5652f7b0aa729bfc9c96b6324e29719e584873e28b26360a39ceb87`  
		Last Modified: Thu, 18 Dec 2025 04:25:37 GMT  
		Size: 107.2 MB (107169800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e373576f9ffd321cb6bca9419551efadd53337352ced94cfe2224a8af83abe7`  
		Last Modified: Thu, 18 Dec 2025 04:25:14 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:08af47d058a6727d5653c7147f8c766e245c84934e8ea8ab6fe2c7445b988955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db537428915940cd8466bd96e667e70297c356e58c22a2e45ca1b1fffdcfe7e2`

```dockerfile
```

-	Layers:
	-	`sha256:a223e1ecb7e6c4e547a65818d728d1b17f4fa189a9828543fe5b32ddefb71ca4`  
		Last Modified: Thu, 18 Dec 2025 05:50:29 GMT  
		Size: 38.0 KB (37974 bytes)  
		MIME: application/vnd.in-toto+json
