## `redmine:5-alpine3.23`

```console
$ docker pull redmine@sha256:7f55d83a11114bd7bd57c021bcd4e0f2a8cccf605ef2bd87304a58bdc31535bc
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

### `redmine:5-alpine3.23` - linux; amd64

```console
$ docker pull redmine@sha256:dfa1179e3e3941e937cf4099f54af85e0b52a002060e5e74542c41ab2946837d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192184572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5820e4a9ae493c745f49d561485618703e4a7f9ed83b5b8632fe9bf372c22bbc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:43:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 00:45:38 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:45:38 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 18 Dec 2025 00:45:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 18 Dec 2025 00:45:38 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 18 Dec 2025 00:45:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 00:45:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 00:45:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 00:45:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:45:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 00:45:38 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:29:03 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:29:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:29:09 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:29:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:29:09 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:29:09 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:29:09 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:29:09 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:29:09 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:29:09 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:29:09 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:29:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:29:09 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:29:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:29:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:30:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:30:49 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:30:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:30:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:30:49 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:30:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d987655edb42a0e6f7413d574559cb70dd7d1cbff7b569626db311b9b4170c`  
		Last Modified: Thu, 18 Dec 2025 00:45:51 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c384285ac9c942349e0d1f1315f4d6e4bb37b1998e543801d6a43d9eabc4f250`  
		Last Modified: Thu, 18 Dec 2025 00:46:00 GMT  
		Size: 33.8 MB (33830315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb9be094b89693600bd47abbb30d2a8e7337a393253eba2e7f32b0efced3689`  
		Last Modified: Thu, 18 Dec 2025 00:45:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d131b48fc0176e1a70ad82bb722faa494bf02176cdbf03e0bc4dffd960fe45`  
		Last Modified: Tue, 06 Jan 2026 18:31:22 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9c113c882bcf4832fa52b87ada762d87b9111e5977246f435610e1dbe36e48`  
		Last Modified: Tue, 06 Jan 2026 18:31:21 GMT  
		Size: 78.7 MB (78699414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9ab5c06798bfd15eba15295d4c1bb7b454e721b7c8d7276c8070b93bef532d`  
		Last Modified: Tue, 06 Jan 2026 18:31:12 GMT  
		Size: 976.0 KB (976046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0588f381e65ae1a29b7965b9f98a960c43b618a42d663b5bccbce430b7d4967`  
		Last Modified: Tue, 06 Jan 2026 18:31:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf771375d45b33cfd9276d055659108ba42a2abb3bc2a70a0a562b43d04731f`  
		Last Modified: Tue, 06 Jan 2026 18:31:12 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcfe0caff0db9aafc8fd2fae07ac2062ea4fdae4fcf04bd36624b07da0adbfc`  
		Last Modified: Tue, 06 Jan 2026 18:31:12 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70da52a2356a50f90aa6d79f050ffb2a96eeaffe4c2da3a14397fae9a64fc58`  
		Last Modified: Tue, 06 Jan 2026 18:31:13 GMT  
		Size: 3.3 MB (3254009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11601f1f339d97f4c133a61eb9d4188c7a0a1a978216d9795d52e9cc7c824810`  
		Last Modified: Tue, 06 Jan 2026 18:31:21 GMT  
		Size: 71.6 MB (71560598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1be52ee2e869132a7657c5cc749c862124bb9237231187297a0e16f830c0d`  
		Last Modified: Tue, 06 Jan 2026 18:31:07 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:c242ef18f34138bec5e10ca6b0c616e2be9da066932ac3fe5bd7b232e4f3c390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe92dd9f208f77d037176359b3986d56c0c340ef704f72eb8506d87d9ccf46a`

```dockerfile
```

-	Layers:
	-	`sha256:c07fcca2cc13f76a4ce7c35a9d47dba36b7bfbcb4bd2635340d598fcc9961de3`  
		Last Modified: Tue, 06 Jan 2026 20:50:15 GMT  
		Size: 40.8 KB (40773 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.23` - linux; arm variant v6

```console
$ docker pull redmine@sha256:0da1820a81da52ad74228070a58db5a06bdf04905acdba8f15b4824c802d36ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183688414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795f4da5206d2edb7cdb2fa32c8abf116dcef5415d9521166055a3428d99e6a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:04:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 01:08:52 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:08:52 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 18 Dec 2025 01:08:52 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 18 Dec 2025 01:08:52 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 18 Dec 2025 01:08:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 01:08:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 01:08:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 01:08:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:08:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 01:08:52 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:30:09 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:30:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:30:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:30:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:30:16 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:30:16 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:30:16 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:30:16 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:30:17 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:30:17 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:30:17 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:30:17 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:30:17 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:30:19 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:30:19 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:32:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:32:57 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:32:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:32:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:32:57 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:32:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b40dbf7ef156258591121279d8c54352bf16d532fe18c5bcbb446b6f21426`  
		Last Modified: Thu, 18 Dec 2025 01:06:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d146509eaff68734d7b0f393b93b4cb19805a56e29b6f4e80eac6175a66e9e`  
		Last Modified: Thu, 18 Dec 2025 01:09:10 GMT  
		Size: 30.0 MB (30020746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd00b6abe6e017dab4fd1cc3f0fe517cb7d8d8490d233f11df93ef0f9bef3179`  
		Last Modified: Thu, 18 Dec 2025 01:09:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dd419cce7d22bc2c48efdca31073b290f55c904a7e1605100db8360b558c18`  
		Last Modified: Tue, 06 Jan 2026 18:33:18 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5438db72349b2354ec811b9be09d7a412f8a7f2a91906056c18102b6ad6417`  
		Last Modified: Tue, 06 Jan 2026 18:33:26 GMT  
		Size: 75.1 MB (75128565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c850facd3836e097d77e864493503176a9c88cb032aac2f76ce191845ada33`  
		Last Modified: Tue, 06 Jan 2026 18:33:18 GMT  
		Size: 942.4 KB (942422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e79ffddfca332da5e3aa0134c3a0b22da79be7df53a5f3d68374c8c4e9d7f5a`  
		Last Modified: Tue, 06 Jan 2026 18:33:18 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828a36db01f1bd4e31d13a47ceefc87918a3ec96d6457e9e68701216b8848912`  
		Last Modified: Tue, 06 Jan 2026 18:33:18 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940f2589aafabe7926c9b398213744928aa731d876b7c26d6230f766ba61f0b`  
		Last Modified: Tue, 06 Jan 2026 18:33:18 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51feb8475eb432bdaef7e2d171e01ff79cb7fc4eb5d96852c854d973dea688f`  
		Last Modified: Tue, 06 Jan 2026 18:33:19 GMT  
		Size: 3.3 MB (3254000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775b468aed42125b85e77a3b5ea97abc49358a7c1b2f1911c3db69f6fddc6b9`  
		Last Modified: Tue, 06 Jan 2026 18:33:25 GMT  
		Size: 70.8 MB (70770162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072b0e5b3571b94bdb2072944d62822ac8d2fe9acaf6a4849b94c6e039b178c0`  
		Last Modified: Tue, 06 Jan 2026 18:33:18 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:935b3125e51d46d94a3818b2ab3d7d5219881f0dca37291face468ad5fdc3b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6330b692ca1c607e329c568040eb4c7a9f69cb83fd41e61634e3d18e1979f0fa`

```dockerfile
```

-	Layers:
	-	`sha256:5cc56323083d7dab16ee7434eb8925381a2115e20230427d7d66b257f2fa9c51`  
		Last Modified: Tue, 06 Jan 2026 20:50:18 GMT  
		Size: 40.9 KB (40947 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.23` - linux; arm variant v7

```console
$ docker pull redmine@sha256:6a18ecbca25db96bb8d0bd19b600cd91052682123703ee252a12d58d1572249e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178857063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2233ddc0d8409f66a689d53e91a315c47c2750e2525dae84fb06a46db70e9c44`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:07:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 01:10:00 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:10:00 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 18 Dec 2025 01:10:00 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 18 Dec 2025 01:10:00 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 18 Dec 2025 01:10:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 01:10:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 01:10:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 01:10:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:10:00 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 01:10:00 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:28:56 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:28:59 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:29:02 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:29:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:29:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:29:02 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:29:02 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:29:02 GMT
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
# Tue, 06 Jan 2026 18:31:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:31:41 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:31:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:31:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:31:41 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:31:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f48da55ab3b89d8d5f7b336bfa04ffd21568164c1ad54bef4e10e0e41a3c5c`  
		Last Modified: Thu, 18 Dec 2025 01:10:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104316b5b6e8511c1527892c2bdda434a9a2ab9a10fc8e864bddf8729d42dbd`  
		Last Modified: Thu, 18 Dec 2025 01:10:16 GMT  
		Size: 29.9 MB (29886328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ced44c024950e214d015890e26991d83fdc8f66a0b599afb93b43b5f00c17a`  
		Last Modified: Thu, 18 Dec 2025 01:10:14 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713699bb2b298844da7b610977120a818b6211b831a453e1c06bf05974426b55`  
		Last Modified: Tue, 06 Jan 2026 18:32:02 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d536cf5be2e267a64c22bdff982d4b89d21ed6a50b33ea5b576f08af6826c91b`  
		Last Modified: Tue, 06 Jan 2026 18:32:18 GMT  
		Size: 71.7 MB (71674661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf9833d63d04b01e4b0ffc0682146ac734f8f7b9fc1ab90949c1060406bfc3`  
		Last Modified: Tue, 06 Jan 2026 18:32:02 GMT  
		Size: 942.4 KB (942383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633f30844d26fef1e03bfd15cf3c1ad032707894b603f28421a48b14c924d26e`  
		Last Modified: Tue, 06 Jan 2026 18:32:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ce80b3da68960e4cf5bb2073afc923443344ce91f6b8d4e940ae06fdb67f8d`  
		Last Modified: Tue, 06 Jan 2026 18:32:02 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0497255d462b36b37be23aa344a2df2234314662c32d19e5708bd83743c405c5`  
		Last Modified: Tue, 06 Jan 2026 18:31:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65100c87521acaf767fbdc072785c83d22b6268113d9864293acb713c6c83702`  
		Last Modified: Tue, 06 Jan 2026 18:32:03 GMT  
		Size: 3.3 MB (3254009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928685342cb338cb6e19032caa6660bb2dd726fe3aa1cacfb5592a35ae95c86e`  
		Last Modified: Tue, 06 Jan 2026 18:32:09 GMT  
		Size: 69.8 MB (69816214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce1be52ee2e869132a7657c5cc749c862124bb9237231187297a0e16f830c0d`  
		Last Modified: Tue, 06 Jan 2026 18:31:07 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:59d667ec99aaaef702038d7cb9dcc2d1fecd6e37dac855d88ee1110287d3125c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 KB (40947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707cf6bd0dae039eafb0374beaf92ce9971843c65a6811e45fd6a0387117e34c`

```dockerfile
```

-	Layers:
	-	`sha256:f0d38988e29f650e2bd4a3d7849fd6fb8591b4696153a1ba66fda65b93c573c4`  
		Last Modified: Tue, 06 Jan 2026 20:50:21 GMT  
		Size: 40.9 KB (40947 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:5512f0cac9b2206fb6632665703fef81b337a52c64edc23055193d5f0ad16d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192066172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd1a3c0fcf56afcc2fe6125363abaaf1835f4b31697c00f5b2f7cacfd0b550a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:49:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 00:51:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:51:17 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 18 Dec 2025 00:51:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 18 Dec 2025 00:51:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 18 Dec 2025 00:51:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 00:51:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 00:51:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 00:51:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:51:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 00:51:17 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:29:16 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:29:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:29:22 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:29:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:29:22 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:29:22 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:29:22 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:29:22 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:29:22 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:29:22 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:29:22 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:29:22 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:29:22 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:29:25 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:29:25 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:31:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:31:41 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:31:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:31:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:31:41 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:31:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31607a2afb8a5e4e2884ab313f22e10ba89d0657d03953a075617f37d60e7bc`  
		Last Modified: Thu, 18 Dec 2025 00:51:33 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77308fcd70e438baab41b99b52eb44fcbca30879f3420addb379fae7d6aa32a4`  
		Last Modified: Thu, 18 Dec 2025 00:51:37 GMT  
		Size: 33.9 MB (33895934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cd7419e348b565a62d24c388b90790c0ee95dfb170d2a5d1560cddffde60b6`  
		Last Modified: Thu, 18 Dec 2025 00:51:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae0af019e168536b7eb1420cafff2673dd7d76317eec3236bad6f795ce509b`  
		Last Modified: Tue, 06 Jan 2026 18:32:01 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5c06576d3952cf7c982c28dd35bfaa11a781b97cded2baf25042b0732ca8b3`  
		Last Modified: Tue, 06 Jan 2026 18:32:10 GMT  
		Size: 78.2 MB (78215267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef2a148d0105d6271a8ff8ac327480f3770a7bbe6da4282be19087eb344bf0a`  
		Last Modified: Tue, 06 Jan 2026 18:32:01 GMT  
		Size: 929.5 KB (929454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15de63b62e8bf4c3dc6f38eeb17edd29f1cfcc7299765ded7f49b300f6e4f2b`  
		Last Modified: Tue, 06 Jan 2026 18:32:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f55cdfa00be463bcd28ee9ffbc77ded3b39adf1ee364b9f2e83a1e7c537715`  
		Last Modified: Tue, 06 Jan 2026 18:32:01 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3732e1b8521dd4db1f7ce17f2db09383ba135de2e72fb2aeebcc9867136efa`  
		Last Modified: Tue, 06 Jan 2026 18:32:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86dcf5ddbc1aa734411dac88811d58d2c27127d58afe31115b71abd993026f3b`  
		Last Modified: Tue, 06 Jan 2026 18:32:01 GMT  
		Size: 3.3 MB (3254006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b3e0e64e0549fde9f1a21257eeefbd5997799906b4d6e10ecc864c9d48345f`  
		Last Modified: Tue, 06 Jan 2026 18:32:07 GMT  
		Size: 71.6 MB (71571686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea90595f2c36159592bc5bd34a77606c4d9967cbf02ff93514c24ee86714f1c`  
		Last Modified: Tue, 06 Jan 2026 18:30:53 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:8566a0fb4ba7ebc904d18c89082bc9d97d2fccfbfbc1cf59f75f034de8aa8721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (40991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c777d9174b0322efb8302972294271a160d79df0f675bca5a74f95fe55cac721`

```dockerfile
```

-	Layers:
	-	`sha256:e4ce79b07241db162dc9d107c096daa7867a938decf8d194860c40bc077823a9`  
		Last Modified: Tue, 06 Jan 2026 20:50:24 GMT  
		Size: 41.0 KB (40991 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.23` - linux; 386

```console
$ docker pull redmine@sha256:8684701a6b64e8bc1f181e6aca1988c274f3bd5c11e337c510cf00f601a51e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188969507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a435168413135120c717317872082735675cce5bbd3e9d45701caecbce8e4872`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:41:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 00:45:50 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:45:50 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 18 Dec 2025 00:45:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 18 Dec 2025 00:45:50 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 18 Dec 2025 00:45:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 00:45:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 00:45:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 00:45:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:45:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 00:45:50 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:27:40 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:27:44 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:27:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:27:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:27:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:27:47 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:27:47 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:27:47 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:27:47 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:27:47 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:27:47 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:27:47 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:27:47 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:27:49 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:27:49 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:29:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:29:40 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:29:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:29:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:29:40 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:29:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5613ad268835a6963f2dadb2db55fcca1d027b626caec092e2d8d7c9face19`  
		Last Modified: Thu, 18 Dec 2025 00:43:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455e5c9ded61d97310f17fcbcc938ca662cab31930f645b62843b26879511e34`  
		Last Modified: Thu, 18 Dec 2025 00:46:09 GMT  
		Size: 29.8 MB (29846053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7654a32205e261ecd15b6eaf78fb0a3abc1ef0184d35108fc7789548461dff6`  
		Last Modified: Thu, 18 Dec 2025 00:46:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0d5c54cd3091062e4c3460055039a18b62bd9b1abd93d7dc7c58cdba8be9d4`  
		Last Modified: Tue, 06 Jan 2026 18:30:02 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1d2ddbe80176f0a2c3b0e6d0a62ca6789ed1cc8949f6790bb5caf6b6c6de0d`  
		Last Modified: Tue, 06 Jan 2026 18:30:07 GMT  
		Size: 79.7 MB (79736873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd7b207f6e081d16b0a31aefa5c961130ef357a615efc66394d9121bc9aee78`  
		Last Modified: Tue, 06 Jan 2026 18:30:02 GMT  
		Size: 946.0 KB (946001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0594c319628f6d913e57366dfb88e150d720ca57b36f2731a1a3afb0c9df5b`  
		Last Modified: Tue, 06 Jan 2026 18:30:02 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07e7a44b98de1a3b1f3db74fcd3e6e6bfdcdd28b0dd1115d2f8e4abb31819c9`  
		Last Modified: Tue, 06 Jan 2026 18:30:02 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7161c6262fe58b9c7d79858b2d1c96a80596da6cd84e75e72c2fdd3bfb606ca`  
		Last Modified: Tue, 06 Jan 2026 18:30:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4696fd7121f57faf6408bc8d4bf0ad2ceaa7a1ee4ff3b62813e86b2e4004f52e`  
		Last Modified: Tue, 06 Jan 2026 18:30:02 GMT  
		Size: 3.3 MB (3254029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4cf2d017db90c42ce74fbc7165dfb359035f9816bfabe23dd475eaa572b207`  
		Last Modified: Tue, 06 Jan 2026 18:30:11 GMT  
		Size: 71.5 MB (71496364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3404364a1d94106fbbf99aebeea6fb3693dc4ed8a7e64f37646342283f56ece`  
		Last Modified: Tue, 06 Jan 2026 18:30:02 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:26355a60122ebc620edbe39dc798f31cb88885b4536f2db713637eaee02d1683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 KB (40719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3915205b1dcab86d88ba7154262ac5adde64c30f979199f19e36619a8d27d58`

```dockerfile
```

-	Layers:
	-	`sha256:45c0518359fb893653a008e9d28bed22303abfa19a9e1769819bf0ca51949ead`  
		Last Modified: Tue, 06 Jan 2026 20:50:27 GMT  
		Size: 40.7 KB (40719 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.23` - linux; ppc64le

```console
$ docker pull redmine@sha256:231762b8eda92ddbb58759472728879593bcf23da64bd8b70afcc7a8cdae9eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194464992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e418abaf39cf7448fd44531218e66702907e957f74d992561b5e724c516990`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 02:15:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 02:22:51 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 02:22:51 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 18 Dec 2025 02:22:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 18 Dec 2025 02:22:51 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 18 Dec 2025 02:22:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 02:22:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 02:22:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 02:22:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 02:22:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 02:22:52 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:51:23 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:51:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:51:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:51:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:51:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:51:39 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:51:39 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:51:39 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:51:40 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:51:40 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:51:40 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:51:40 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:51:40 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:51:43 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:51:43 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:54:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:54:59 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:55:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:55:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:55:00 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:55:00 GMT
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
	-	`sha256:d9d1f2f67579ea1098dfed92c51cb00e92b135a60e0dfab65f157395c982a94e`  
		Last Modified: Thu, 18 Dec 2025 02:23:25 GMT  
		Size: 31.5 MB (31547546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ff6b0722ce6acd46be97754ecb3045a28a533feb071ae20b9dde6ab819010f`  
		Last Modified: Thu, 18 Dec 2025 02:23:21 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5691f6b02830782b55759574af4247fae3bea7aa0a81dcd10294eb8256719258`  
		Last Modified: Tue, 06 Jan 2026 18:55:37 GMT  
		Size: 909.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ce0df786a58bd3465163931f660a4ea326482633a4663fc0858bd5f0f9cc43`  
		Last Modified: Tue, 06 Jan 2026 18:55:46 GMT  
		Size: 81.3 MB (81282417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584e6b6406b9844136c3bcac8026b251e9b9ae5c47f290645ea345e17dc3bb2b`  
		Last Modified: Tue, 06 Jan 2026 18:55:38 GMT  
		Size: 934.5 KB (934537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8298c3f26df3b7cd7a06f4c8159a234c45756fe5f799b273d66b3847a35e26`  
		Last Modified: Tue, 06 Jan 2026 18:55:38 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fa07f17bc69b77940f7d2c8d3c0e4d399b56d95a2786417cc676ddfa68dcd`  
		Last Modified: Tue, 06 Jan 2026 18:55:41 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ef4f8628776636f91145ae770a68404a0d18facb92c3cc771b1bd25625f0e2`  
		Last Modified: Tue, 06 Jan 2026 18:55:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdde1c7c1c3dc3ccac8ac16fc76b9692ac0863f14853cbe97edceec523ea5b1`  
		Last Modified: Tue, 06 Jan 2026 18:55:38 GMT  
		Size: 3.3 MB (3254020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dd030cc4a92295596070eb57b436500d1c5269310c3043b586692e5b03d7e7`  
		Last Modified: Tue, 06 Jan 2026 18:55:45 GMT  
		Size: 73.6 MB (73614630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496f141ee7dd86d9740f776fb9279467d24191f178116392b73e2abb7d60aedb`  
		Last Modified: Tue, 06 Jan 2026 18:55:38 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:29a2610ac30ac000f9b22063e85fa814a8d2c2686b9c230f5abf2d8624baa1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f5292c3696f530f61927ddc11a9484999c4d49709ebc7fdc6c77b43eb4e516`

```dockerfile
```

-	Layers:
	-	`sha256:2c2c70f41fa16558432a2bb527418110a836ea230fbff8aa250b3f7491357289`  
		Last Modified: Tue, 06 Jan 2026 20:50:49 GMT  
		Size: 40.8 KB (40841 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.23` - linux; riscv64

```console
$ docker pull redmine@sha256:dcf39a04bb165d735d6fc3603ef4765a42e0c2b412e522d0d1ea455fd8f39e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198711406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008e3f1005edce75a5080668c6636280183a87116ad374c36a32fdb89a68ce3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 11:10:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 19 Dec 2025 16:32:06 GMT
ENV LANG=C.UTF-8
# Fri, 19 Dec 2025 16:32:06 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 19 Dec 2025 16:32:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 19 Dec 2025 16:32:06 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 19 Dec 2025 16:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 19 Dec 2025 16:32:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 19 Dec 2025 16:32:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 19 Dec 2025 16:32:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 16:32:07 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 19 Dec 2025 16:32:07 GMT
CMD ["irb"]
# Mon, 22 Dec 2025 02:19:47 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 22 Dec 2025 02:20:22 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Mon, 22 Dec 2025 02:20:33 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Dec 2025 02:20:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Dec 2025 02:20:33 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 22 Dec 2025 02:20:33 GMT
ENV RAILS_ENV=production
# Mon, 22 Dec 2025 02:20:33 GMT
WORKDIR /usr/src/redmine
# Mon, 22 Dec 2025 02:20:33 GMT
ENV HOME=/home/redmine
# Mon, 22 Dec 2025 02:20:34 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 22 Dec 2025 02:20:34 GMT
ENV REDMINE_VERSION=5.1.10
# Mon, 22 Dec 2025 02:20:34 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.10.tar.gz
# Mon, 22 Dec 2025 02:20:34 GMT
ENV REDMINE_DOWNLOAD_SHA256=0f187dcca0804f42faf7bbee1ad0a759291b026f707d86347bc14f34defa6f41
# Mon, 22 Dec 2025 02:20:34 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Mon, 22 Dec 2025 02:20:39 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 22 Dec 2025 02:20:39 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 22 Dec 2025 03:23:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 22 Dec 2025 03:23:38 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 22 Dec 2025 03:23:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 22 Dec 2025 03:23:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 22 Dec 2025 03:23:38 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 22 Dec 2025 03:23:38 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a698ec77791eae41a5ea71dbaf461740620a754436fee72224883fdf7fe1344`  
		Last Modified: Fri, 19 Dec 2025 13:37:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dc2e0642ed086f583c0772b3c619873d87185327c23d442664d6b1b989f6b7`  
		Last Modified: Fri, 19 Dec 2025 16:33:35 GMT  
		Size: 32.5 MB (32514949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45389ba19af81b6ac272157e334911d35a444f1409558afaf35cb153f3ea7113`  
		Last Modified: Fri, 19 Dec 2025 16:33:30 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12a91135b4df5133a9f5ab8bb4a998e04da8d239d42dd39ca6827d90b93be44`  
		Last Modified: Mon, 22 Dec 2025 03:26:10 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01888e7fdf601c7883f7407b6a4ef1f73ad2d1f192bb65e598865acc2d9a066`  
		Last Modified: Mon, 22 Dec 2025 03:26:15 GMT  
		Size: 76.9 MB (76941298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1426a39723cfe0e55d4bb1ae28d2dba036542068d0fa310aed9489ad3cf7fb1`  
		Last Modified: Mon, 22 Dec 2025 03:26:10 GMT  
		Size: 921.8 KB (921838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2b86b0403de4a3d4b822f8f81898e0716ef82f0badb2f3b8dc59bce61b7811`  
		Last Modified: Mon, 22 Dec 2025 03:26:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5bfc56f8e7ddd837019a48e19a79fef6d3f8249aa4431e70e7e8ee181ee4cd`  
		Last Modified: Mon, 22 Dec 2025 03:26:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b68a6a1d1f2926ad2f05a9a1bb365dbecd4f9023e374041290cfd58f181f47d`  
		Last Modified: Mon, 22 Dec 2025 03:26:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa29875bb452898199ea9a69cc026758a03dac2f08c052379b6e4fa81b95524`  
		Last Modified: Mon, 22 Dec 2025 03:26:10 GMT  
		Size: 3.3 MB (3252541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5ff44a684e0b90495c52f11a0a4df6c52d365ed6ae86aa67352e4a2c8fee32`  
		Last Modified: Mon, 22 Dec 2025 03:26:32 GMT  
		Size: 81.5 MB (81492756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf74568e08a8780cbff9aa2fbf3bc1ca5bf4d6cac16a890e0076e26bc3b3c32`  
		Last Modified: Mon, 22 Dec 2025 03:26:10 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:ca990e28924da1fa135bc105a0ff2ebf733b7c73c75b6c7242b84dead67d4868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047e8ed1332396940bdaf7c06920cff6fae52056bb82e4465a93b95c4326445`

```dockerfile
```

-	Layers:
	-	`sha256:dc20fa8a93be63a3dfe56c4465f6babe6b20cc00d0f8ea05ed87d939cf04a619`  
		Last Modified: Mon, 22 Dec 2025 05:49:42 GMT  
		Size: 40.8 KB (40841 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-alpine3.23` - linux; s390x

```console
$ docker pull redmine@sha256:b8d29feb7cc6d5e5c7d2a27f687a9c1c90b179207911a6504386e5dfc0ebc666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190650538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb185744fdaf96dc71a862e19be0fbdb98f2eebfbd7572e5a86f5a74e10ebbb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 03:34:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 18 Dec 2025 03:41:13 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 03:41:13 GMT
ENV RUBY_VERSION=3.2.9
# Thu, 18 Dec 2025 03:41:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Thu, 18 Dec 2025 03:41:13 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Thu, 18 Dec 2025 03:41:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 18 Dec 2025 03:41:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 18 Dec 2025 03:41:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 18 Dec 2025 03:41:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 03:41:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 18 Dec 2025 03:41:14 GMT
CMD ["irb"]
# Tue, 06 Jan 2026 18:32:37 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Tue, 06 Jan 2026 18:32:41 GMT
RUN set -eux; 	apk add --no-cache 		bash 		breezy 		ca-certificates 		findutils 		ghostscript 		ghostscript-fonts 		git 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		tzdata 		wget 	; # buildkit
# Tue, 06 Jan 2026 18:32:43 GMT
ENV GOSU_VERSION=1.19
# Tue, 06 Jan 2026 18:32:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 06 Jan 2026 18:32:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Tue, 06 Jan 2026 18:32:43 GMT
ENV RAILS_ENV=production
# Tue, 06 Jan 2026 18:32:43 GMT
WORKDIR /usr/src/redmine
# Tue, 06 Jan 2026 18:32:43 GMT
ENV HOME=/home/redmine
# Tue, 06 Jan 2026 18:32:44 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 06 Jan 2026 18:32:44 GMT
ENV REDMINE_VERSION=5.1.11
# Tue, 06 Jan 2026 18:32:44 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.11.tar.gz
# Tue, 06 Jan 2026 18:32:44 GMT
ENV REDMINE_DOWNLOAD_SHA256=5320bf7a35d3e9feb90c52d8bd018aa263dc77eb17c96001d8b3223c59549049
# Tue, 06 Jan 2026 18:32:44 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 06 Jan 2026 18:32:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 06 Jan 2026 18:32:45 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Tue, 06 Jan 2026 18:35:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		yaml-dev 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk ' 			system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } 			{ print "so:" $1 } 		' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 06 Jan 2026 18:35:11 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 06 Jan 2026 18:35:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 06 Jan 2026 18:35:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:35:11 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 06 Jan 2026 18:35:11 GMT
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
	-	`sha256:b98b40562aa2ff135aaebb24c662d0f31b89f17b7281873af46191a9d9386f9d`  
		Last Modified: Thu, 18 Dec 2025 03:41:35 GMT  
		Size: 31.1 MB (31131975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bb0b0edc20c548debcbbaceef88ae3fc4aa3f14a0e55cd8c1ad7046255cddf`  
		Last Modified: Thu, 18 Dec 2025 03:41:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132697e53fbba213e3910ef49e07d410cb553f58f87d0e35ac9c0bfd8b3d3056`  
		Last Modified: Tue, 06 Jan 2026 18:35:36 GMT  
		Size: 910.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10b3a7cbea3c99b5a2230e258c4e1b00eb8b0244d1d328c4389fd3d2bf2f625`  
		Last Modified: Tue, 06 Jan 2026 18:35:40 GMT  
		Size: 79.0 MB (78971224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddac0af219e649c4ac990877603163e6b5865546b5b548b1a9eeb1064305daba`  
		Last Modified: Tue, 06 Jan 2026 18:35:36 GMT  
		Size: 950.3 KB (950305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c69e30ec3fbd634834007db9a7269e0f9fe3a0a954f1f4530e2a1fc2d318e1`  
		Last Modified: Tue, 06 Jan 2026 18:35:36 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a6df43bace3feeb95da5789cd545669290fe19adc974045b2665fb540ccaee`  
		Last Modified: Tue, 06 Jan 2026 18:35:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acb0a117d56faade9ee3f8f3551aceb9dd425a27409d0786d425ebeee593617`  
		Last Modified: Tue, 06 Jan 2026 18:35:36 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e3a9a5322c561bc44640e525b46069bb68405694b771816e3195c0d3dafddc`  
		Last Modified: Tue, 06 Jan 2026 18:35:36 GMT  
		Size: 3.3 MB (3254013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62445b76e2ddd523dbc4951385ac566670443a0d2148dfc3f108388264496065`  
		Last Modified: Tue, 06 Jan 2026 18:35:40 GMT  
		Size: 72.6 MB (72614625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25535722cd48ef9dbb0269fc6bbc11cf43eac4cc3cd9b07327c50aeab7a85ad`  
		Last Modified: Tue, 06 Jan 2026 18:35:36 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-alpine3.23` - unknown; unknown

```console
$ docker pull redmine@sha256:59fbba16f6784f12bafdaa541d4b6fcbb01c0f3ef7f8154acaaaee2ef121984a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a723c6b94244903fcff855940032d4f7854ec9d6b7cdcdc7ca86e07369cfe85e`

```dockerfile
```

-	Layers:
	-	`sha256:2d82cb7898acd5a146ae061daab8f07bdc7e43bd2acefac1ab73f4914abf9a83`  
		Last Modified: Tue, 06 Jan 2026 20:50:54 GMT  
		Size: 40.8 KB (40773 bytes)  
		MIME: application/vnd.in-toto+json
