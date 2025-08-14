## `redmine:alpine3.21`

```console
$ docker pull redmine@sha256:37addafb0c06bd2b12244f8d251b0a1fb801ef5ac96fe108b21b62c0200c0347
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
$ docker pull redmine@sha256:8fff5cd8b8ca51a4f14d7f790a00135dabd113be552c8b5be4eebb3988cc4ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191057872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ee7751471bdee5021db06ffc8ca858352f40690e2244a22cc748ae34d91037`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 07 Jul 2025 22:15:35 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV LANG=C.UTF-8
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_VERSION=3.3.9
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072e3e4ea5c913a8dae03862632bcceaa9122bb0351a8b1562e276de1cc1ed0`  
		Last Modified: Thu, 24 Jul 2025 18:45:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203353491163f797e096e74e92c164a8132e0412753837bbfe30abd3c336c296`  
		Last Modified: Thu, 24 Jul 2025 18:46:10 GMT  
		Size: 35.6 MB (35615628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6debf1a7124e3a62068eca8fe54dd40cce6ab977d7091f99a086fbcee3403de0`  
		Last Modified: Thu, 24 Jul 2025 18:46:05 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78be2fded392a7cc9280a45c352c54c6ff845368a845fb119068d0e2f2bd746`  
		Last Modified: Thu, 24 Jul 2025 18:55:06 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365fdf1e7c79e7c276f7205827275592f7d77f82e0958769c5aac037da04c1a7`  
		Last Modified: Thu, 24 Jul 2025 19:52:08 GMT  
		Size: 72.7 MB (72679350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4712cd7e7176d0338e800c038cc62d137bba349ea184d8b3f26f86c84318c5b9`  
		Last Modified: Thu, 24 Jul 2025 18:55:10 GMT  
		Size: 1.2 MB (1168498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f35f45ebb02c6d687078caa7e86617ebc06fc676172d93619c9b0fe11dcebe`  
		Last Modified: Thu, 24 Jul 2025 18:55:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b51cdacf4b790dd617d9db4baa453d6f1d514fa82c2513ebc7ae73d7921396b`  
		Last Modified: Thu, 24 Jul 2025 18:55:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920ecef60e93c546cb6084a509fd2a35bdfd93aa336784fcbddd54c36fef53c0`  
		Last Modified: Thu, 24 Jul 2025 18:55:22 GMT  
		Size: 4.1 MB (4067299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd834b68b32a5bb1c6bb7180a592eb134bf4e5c1a5b416c2f2a168821a0583e7`  
		Last Modified: Thu, 24 Jul 2025 19:52:07 GMT  
		Size: 73.9 MB (73885721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fb8abadfb767c6485e15dc8e0ad752082e67b9b8b3bac35e94009bda140f38`  
		Last Modified: Thu, 24 Jul 2025 18:55:51 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:704df0adcc71866ce43eab004ae6225affccefe8e0e29876c5385576d5c5613f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dac47828736d550fcaf8a23208183ee2d040075b02b4cdc9bb9d0df504995d5`

```dockerfile
```

-	Layers:
	-	`sha256:7a198bdc1ce2ab58c8ff1f047e1f7eb1e66cfbc866c601fd1f327e1b08840ef6`  
		Last Modified: Thu, 24 Jul 2025 19:51:28 GMT  
		Size: 36.8 KB (36792 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm variant v6

```console
$ docker pull redmine@sha256:9e11578411e43952421fefcd35c542bd5299405f9b4521e9c0701911ab5d8f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182950790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ffa2ba1c05301c4ffb8c3c717b9f4f232cc29983ce6979c15a3a14d980cae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 07 Jul 2025 22:15:35 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV LANG=C.UTF-8
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_VERSION=3.3.9
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
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
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd2aade873422152cd38c54790f33c3043c235216377097742a4ec943cea10`  
		Last Modified: Wed, 16 Jul 2025 03:14:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4d3b39d485fe37d5d05f0240313ddfdcc1f39833a914ef28acde83dd2d9085`  
		Last Modified: Thu, 24 Jul 2025 19:52:09 GMT  
		Size: 32.1 MB (32071821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bda74ee7a6784522652a758995e54717ecca24ed5692b58b4c4c1b65b35df8`  
		Last Modified: Thu, 24 Jul 2025 18:45:55 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca081111fe48ac0811d636684f01b28d9f9cf475b0fde8109d99ad77701b561`  
		Last Modified: Thu, 24 Jul 2025 18:53:56 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ccf4376ec7fb753ef33eae6ac537d03fb06cd7feb30e8a7eaf6460527f0b58`  
		Last Modified: Thu, 24 Jul 2025 18:54:07 GMT  
		Size: 69.3 MB (69252007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f219472bcbf0db91083ee025f3be36fd56c01e5afe1ad0fc1631022bf59343c9`  
		Last Modified: Thu, 24 Jul 2025 18:53:56 GMT  
		Size: 1.1 MB (1134973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95421a52fa68e39fbd7256674a0018f180ac24e0b4fab4d24667c27d0baaea2e`  
		Last Modified: Thu, 24 Jul 2025 18:53:56 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474c95c9b153c79988607608ed903cd41a75eb2ecbe24056196ed064220adad7`  
		Last Modified: Thu, 24 Jul 2025 18:53:56 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8c7ba7dc20d85e7917415e765714202e6d83c51aaf67e9f667ce774130f65a`  
		Last Modified: Thu, 24 Jul 2025 18:53:56 GMT  
		Size: 4.1 MB (4067228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0680beed0c69561f6307be5353ef7e48c7420df4b3aa36ffae423ee80b234`  
		Last Modified: Thu, 24 Jul 2025 18:54:08 GMT  
		Size: 73.1 MB (73057145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be7264a466b1ea1f2eabeb8ad27aafc421b7c7aae530a6ca8838b2112bc39b`  
		Last Modified: Wed, 16 Jul 2025 06:54:27 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:e4a855cac34b5fa725e8c361672ef32b0859bcedfb1c03ec78dff004e987ee52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dc060565873c1e1e40c474927d7a561caef33e6aa32d93deb31fbf73fd4fb6`

```dockerfile
```

-	Layers:
	-	`sha256:2af935bccd77aa95e5a45eda7c14bf207d93ea8485698724845e06b8bfb1a9f2`  
		Last Modified: Thu, 24 Jul 2025 19:51:32 GMT  
		Size: 36.9 KB (36933 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm variant v7

```console
$ docker pull redmine@sha256:bc2400cb6c6f452213e72870f42146d5d68efe373088a12b5fd18fb9e8cbd2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178742482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf9d56a6b83ab5dce4fef27a49a40fc53ab685d9b490153ff005795c311c6c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 07 Jul 2025 22:15:35 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV LANG=C.UTF-8
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_VERSION=3.3.9
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
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
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770f1267e885ebdd245469ced631a975128a2c04584309a18a73b137ebc67293`  
		Last Modified: Wed, 16 Jul 2025 03:21:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a012e992f71f58404b2fdf681c56e004d9232fb46f6c13da8fffc3b6197f3031`  
		Last Modified: Thu, 24 Jul 2025 18:44:28 GMT  
		Size: 31.9 MB (31940083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ca87e750f691d8434671a63c5d33fc91364fc16d93f947291a4b06152de84b`  
		Last Modified: Thu, 24 Jul 2025 18:44:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d9d41c9bfb654656eaac1dcbab70115b7367fcef30ca1530c335fa6c79ad5`  
		Last Modified: Thu, 24 Jul 2025 19:11:04 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a5da48b70e526135de254d21a2e4e3adafa939ce5ae63bf59e0a9be96886db`  
		Last Modified: Thu, 24 Jul 2025 19:11:15 GMT  
		Size: 66.4 MB (66402697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1bfbcdf0e9814c272b96611ea99ca9c8a920c9fb23872f2941a22ea837f9b5`  
		Last Modified: Thu, 24 Jul 2025 19:11:06 GMT  
		Size: 1.1 MB (1134972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005728250a4439b23c8d0795dd9506c348db22cc17afc88c8356f0523746d807`  
		Last Modified: Thu, 24 Jul 2025 19:11:04 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa34dd5b58092aba4a8b6d1400f2629f484509b2dbe2a0200232d622585cd3e5`  
		Last Modified: Thu, 24 Jul 2025 19:11:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce81cbee87e458a1bc8cf3a16ebd23c8ed6a8d4bb48242c5d8e93065c5473d4`  
		Last Modified: Thu, 24 Jul 2025 19:11:03 GMT  
		Size: 4.1 MB (4067229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9449c592a19eba04fb261cc4e7da346da46a5de197469d2457f2b9d6e593ef`  
		Last Modified: Thu, 24 Jul 2025 19:11:19 GMT  
		Size: 72.1 MB (72096826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bbe4191e99cac3c6fc2332aaa2b68daff1befe8e5f53fbd0a16e009d9a4f1a`  
		Last Modified: Thu, 24 Jul 2025 19:11:00 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:f1b15de42c465ee9135d6016804a9db0b3cffa72c87372dadf949f8b7de824ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 KB (36932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ce7745c6f2faa301e75a22bd0cd2acf3778044175ee85af3038b30b6d99d94`

```dockerfile
```

-	Layers:
	-	`sha256:c8745d37ad691784cee9dbde784bf42873ed195d74e92341efb7bac822d30460`  
		Last Modified: Thu, 24 Jul 2025 22:51:27 GMT  
		Size: 36.9 KB (36932 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:39f5561cb34003db5e0170d2d73704cd748b7fd82ad18288630660393063ac64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190935351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4689819a042087c255f38b3b1a9fc97966b05ac76864feeb18343ea44bd975`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 07 Jul 2025 22:15:35 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV LANG=C.UTF-8
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_VERSION=3.3.9
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
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
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88a67af6e61884f81e8aedb5d643f2b423edf30698d9d9bc7288cda191cbf86`  
		Last Modified: Thu, 24 Jul 2025 18:37:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d27753b78f787827728c2071fe55f26c6bcc73df36f87f22aa332e586477f5`  
		Last Modified: Thu, 24 Jul 2025 18:37:34 GMT  
		Size: 35.5 MB (35538489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9681ddb3a23aa1504e2a6638408b60fdf418de7eb55437715a86b576d27e87d1`  
		Last Modified: Thu, 24 Jul 2025 18:37:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb78f062b670dde35d3facadb568ba09cdd5ba86426628fff2c99246c8febdc`  
		Last Modified: Thu, 24 Jul 2025 19:08:10 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc67dce61fc279cb391dbb726b68bb5e4b2587d3833429891c9c0e82645f48cb`  
		Last Modified: Thu, 24 Jul 2025 19:08:22 GMT  
		Size: 72.4 MB (72359716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ef8ee9a5be8e96f75627ab6f547bbafaa099262606868682aff6400bad8215`  
		Last Modified: Thu, 24 Jul 2025 19:08:10 GMT  
		Size: 1.1 MB (1096851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9296cf44b3a58207c4e0a46c8f6c2fd418170d3fba829bfc173e94eca313f0a9`  
		Last Modified: Thu, 24 Jul 2025 19:08:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c629f937414fb27aa2cdcedae28fe9889be402104f4cff60197643d242b72`  
		Last Modified: Thu, 24 Jul 2025 19:08:10 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2ab00998369a03ffa60d1bc7324a9df561a180d4d123fac4d8faa083089f01`  
		Last Modified: Thu, 24 Jul 2025 19:08:12 GMT  
		Size: 4.1 MB (4067313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d55e3697218c12b0caa70ab7914683995f42a42b17a9f9cfa97666f7b357d7b`  
		Last Modified: Thu, 24 Jul 2025 19:08:24 GMT  
		Size: 73.9 MB (73882241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f14553a5e3ceb8ee9a04ab8a562f3c8f1f24db121d9d8062d13c65264e6fd9`  
		Last Modified: Thu, 24 Jul 2025 19:08:11 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:f7af9be57ca2565788d1de195a83b3674586dacff187faff1d3acd38a6fa9843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7591d9f9a929b96a3cdf9e0fa5fc4920bbe3f5255d32addf29aa5cd0e9f1b5f1`

```dockerfile
```

-	Layers:
	-	`sha256:af98823651bf42f78cd7f489a1faa7e79252b25023df518c8f8b98fd58d4956c`  
		Last Modified: Thu, 24 Jul 2025 22:51:34 GMT  
		Size: 37.0 KB (36971 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; 386

```console
$ docker pull redmine@sha256:3a059f46f5133812bbc3c2709ecc3e11d23bc9daca69a3441cca18bd55064c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187953065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94f0587f8b34f20882b3bb60d337248a4f0ace6907e9f4fb570973aa68dd8fa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 07 Jul 2025 22:15:35 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV LANG=C.UTF-8
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_VERSION=3.3.9
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
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
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3748b85f9c1210995838145e6f8169922d062f6375fb07ce372c3a05ab89fde4`  
		Last Modified: Thu, 24 Jul 2025 18:30:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e01c4485ee7ec68e4f000ce7a4758a03345860b3e84cb29c0db67ce607ddc5`  
		Last Modified: Thu, 24 Jul 2025 18:30:07 GMT  
		Size: 32.0 MB (31957554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afba70ebeaafeafd7f195c817c2fbee88a9e478ce37161dff65bad07561d93a2`  
		Last Modified: Thu, 24 Jul 2025 18:30:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8eee81369d1dabc08c5470d8cae192de2594c08327f55e35614d2cefa6485`  
		Last Modified: Thu, 24 Jul 2025 19:12:57 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0113d64d6a740d01834e3b5cffbebb3e274ea1a916e2d60b42003b2ca33a7b`  
		Last Modified: Thu, 24 Jul 2025 19:52:13 GMT  
		Size: 73.4 MB (73365393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406f24c57d0128c4546bbf7419c00520a55f37a709828502bf54e0e3fff3cb6e`  
		Last Modified: Thu, 24 Jul 2025 19:13:00 GMT  
		Size: 1.1 MB (1143788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20959ff187834d15332264774d70a0ad8e087d48a8856824f9e6f0774e0dbbd`  
		Last Modified: Thu, 24 Jul 2025 19:13:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c832bd264e0150235a77c2d69237eab05bcee81ee2dd014c6d5e28cb47d5ff5`  
		Last Modified: Thu, 24 Jul 2025 19:13:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba75179146ede3c0b769cb95fed23d07807d6a0f0f1e09ac2305390383be0800`  
		Last Modified: Thu, 24 Jul 2025 19:13:15 GMT  
		Size: 4.1 MB (4067242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec154d3b77d233f577cdedebb462d9759cd7f957ccf52cfa62e5d5bef3d935a9`  
		Last Modified: Thu, 24 Jul 2025 19:52:08 GMT  
		Size: 74.0 MB (73954558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1713596d80e0acb1f4ad218efde976f59358d97219ac7fe79e3f42850a91f2e7`  
		Last Modified: Thu, 24 Jul 2025 19:14:09 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:4790c98590269cca16081bec7b22f5fb0700a392115a1c790c5f18c4f31ca1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e064f86fb1a514e331576e566b19b83977415b3f84414cc759320eeb6cb958a6`

```dockerfile
```

-	Layers:
	-	`sha256:619921f152bf7da4ca996f8ff9d78984607eb5d075e29b0cdfb5424fea62a012`  
		Last Modified: Thu, 24 Jul 2025 19:51:42 GMT  
		Size: 36.8 KB (36750 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; ppc64le

```console
$ docker pull redmine@sha256:2a99414b52e6c96baa551cdb2f93ddd74cfff1588cd3d4fe0a63fb13b79add76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192246527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544c3cd5d1eb4434108d11788637d393780a8ff44dbce45295d099c76bbdde0d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 07 Jul 2025 22:15:35 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV LANG=C.UTF-8
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_VERSION=3.3.9
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
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
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f46416c566ecc9d89cb5bee95fc09aa21f865554af8f4134eb062779a2f237`  
		Last Modified: Wed, 16 Jul 2025 00:59:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f34485f0a02542f6d3f0071e2b20b14784febfa7e6900cda5a89c870d097b3e`  
		Last Modified: Thu, 24 Jul 2025 18:37:09 GMT  
		Size: 33.5 MB (33453818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cc80e746f49edd232e415595c252265c3fce90bcc1aaeeccbd81827f3b4a2d`  
		Last Modified: Thu, 24 Jul 2025 18:37:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b446d94cea299a418634a93b12adda62090fbcea51d6210512c570f13afe8b`  
		Last Modified: Thu, 24 Jul 2025 19:13:54 GMT  
		Size: 913.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a712241caf71e05298b7bcba92f8c2a033c429479b47347f166f0a7018bbacee`  
		Last Modified: Thu, 24 Jul 2025 19:14:15 GMT  
		Size: 74.4 MB (74406461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f24890a0238c26b37d5da5b806d6a04ec6f81d105e131c0c5ca57821c0a8d9a`  
		Last Modified: Thu, 24 Jul 2025 19:13:55 GMT  
		Size: 1.1 MB (1087344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a0c588fbf295fd2a6e34d1f0dfd8800955e79b6c88cabe9798f19e5f5ef2cd`  
		Last Modified: Thu, 24 Jul 2025 19:13:54 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4fbee14918681447ea95bf0bbba91475f85088378e0d26cbc33d3a2001e759`  
		Last Modified: Thu, 24 Jul 2025 19:13:54 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7adeb8df785c5c1c2183066588b6ac78309bb482dcd99f4a823dca7c0c4883b`  
		Last Modified: Thu, 24 Jul 2025 19:13:56 GMT  
		Size: 4.1 MB (4067268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57230bda85674116975d54ce544dd140ca33cd750d60b110b2ac5be801dfd99`  
		Last Modified: Thu, 24 Jul 2025 19:14:00 GMT  
		Size: 75.7 MB (75658706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a5076e8ff9b27808d45d3a390c30a59b51c577f9cc4501ce764664a6ca79b0`  
		Last Modified: Thu, 24 Jul 2025 19:13:54 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:f674903031a04feccb0cee9487d0f0f87a846841522b223d13369e0c3ca1dd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef703735152056776044205ba81392333b816d90fe9dd338faedf8e6e11a525b`

```dockerfile
```

-	Layers:
	-	`sha256:b24c62307bc220df64e2918ddde59b279ce711774986d413282e83998b9a29a9`  
		Last Modified: Thu, 24 Jul 2025 22:51:40 GMT  
		Size: 36.8 KB (36846 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; riscv64

```console
$ docker pull redmine@sha256:e739c45354150cb6b63a37abf532a76a23e1a4cc4d08512aca78b84876a6c5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188981457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32872580a40474687f243e00a4dd72a6f1964fbd66116bdd493caf8194c25cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 07 Jul 2025 22:15:35 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV LANG=C.UTF-8
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_VERSION=3.3.9
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
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
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c4be3fb7c48ca84ee50be475d7d4a527212bb75b64469ee7eb6e6f0a98941f`  
		Last Modified: Fri, 18 Jul 2025 03:36:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af990bad08aaf772d4ffcb9f06a602319d08aef90e9237bbb8ee4e99946120f`  
		Last Modified: Thu, 24 Jul 2025 21:22:31 GMT  
		Size: 31.7 MB (31746901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590aa49d68bcc0b2b953b8aeb5192dc3617a732a168b59d588c9d1d2ecffdace`  
		Last Modified: Thu, 24 Jul 2025 21:22:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10a5aa1b987b600d33ac038061247e4c60e0409689b3c8fa26443369456e3ea`  
		Last Modified: Fri, 25 Jul 2025 02:30:08 GMT  
		Size: 911.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86d426a92deca2fd2fdb718faf46569fee1e6fbe89f183cf9e23b1cef255193`  
		Last Modified: Fri, 25 Jul 2025 02:30:15 GMT  
		Size: 71.5 MB (71468471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521ecc7680f6379658bd90dc4339e3a174b2c0f22adf0f712d89cf564716e59d`  
		Last Modified: Fri, 25 Jul 2025 02:30:08 GMT  
		Size: 1.1 MB (1137192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6939c88e9203bf2eccad8f6dbd88dc9e3c1207a71e9825f757847d07fea77a`  
		Last Modified: Fri, 25 Jul 2025 02:30:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b754a22593eef94a2f3559ee2186e31f10e6c1c87c28ff31bab55ed0d7c973b0`  
		Last Modified: Fri, 25 Jul 2025 02:30:08 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776a7b4cbe18d155e1c6fa8820b41f52e7ea67d459b86bcfd676ffa17cd424c`  
		Last Modified: Fri, 25 Jul 2025 02:30:10 GMT  
		Size: 4.1 MB (4067295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa7a408918750819d58e7586fd37557021baeddd914e61b936e205a613418e4`  
		Last Modified: Fri, 25 Jul 2025 02:30:15 GMT  
		Size: 77.2 MB (77208706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b01433301a887158232b0c9b46c379bd02311aa3e07c654304f91388984a838`  
		Last Modified: Fri, 25 Jul 2025 02:30:08 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:da1d227e8f187de7cf890bb4a3bf6123661fa65086e327c798617d4f2775eff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fd377b0c7358d833a1d51e50b7c3e866a810218e6d2f805a69d39d0c366b9a`

```dockerfile
```

-	Layers:
	-	`sha256:944eb6b1eb5c1c98c9e3c8644b72f0c2c16514672c6088c1af025af75f399345`  
		Last Modified: Fri, 25 Jul 2025 04:50:11 GMT  
		Size: 36.8 KB (36846 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.21` - linux; s390x

```console
$ docker pull redmine@sha256:fc05b8f86b1098927c0779087f3403b05e72d7b739551a95636852fe454d7529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190414463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0135b55b8f083e988f387e1076e76bc267bc64ed5eaf2fa13d1a36a5a6331d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 07 Jul 2025 22:15:35 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV LANG=C.UTF-8
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_VERSION=3.3.9
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.9.tar.xz
# Mon, 07 Jul 2025 22:15:35 GMT
ENV RUBY_DOWNLOAD_SHA256=2b24a2180a2f7f63c099851a1d01e6928cf56d515d136a91bd2075423a7a76bb
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 07 Jul 2025 22:15:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 22:15:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 07 Jul 2025 22:15:35 GMT
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
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f70e23950b298583307250026bf211e6e69f1f04bf424c27ce5cf1cd1fad65`  
		Last Modified: Wed, 16 Jul 2025 04:44:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc5994e3e7f2ba57e4e98b07425316eb455c49533613b82fe3cf226bce501d7`  
		Last Modified: Thu, 24 Jul 2025 21:56:21 GMT  
		Size: 33.2 MB (33245157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a3915b37178951f6bf6db0323dd06587ba7079824f4956c6845fede9501d0e`  
		Last Modified: Thu, 24 Jul 2025 18:46:19 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b068c6a721c31f2404b7d9b93a254e2345c2ef38d96d8b85e07696ecc8a700`  
		Last Modified: Thu, 24 Jul 2025 19:07:56 GMT  
		Size: 912.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fe5abdcab656c1fd99b1c53736ffd55ae839afe4db150af91df13d92c39462`  
		Last Modified: Thu, 24 Jul 2025 19:08:09 GMT  
		Size: 73.4 MB (73439961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f28a7654c042d4f9da43af557d728e9cc117b545119337dd2245d38e9fd15dc`  
		Last Modified: Thu, 24 Jul 2025 19:07:57 GMT  
		Size: 1.1 MB (1131697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556f3bb8c400ed333c7bcbe765c8e77b06271188eb08733a13612a415404a086`  
		Last Modified: Thu, 24 Jul 2025 19:07:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad76bef802f98b61c343d4ec7ea06fab354154dc70a56fe89f04bab6c442cf8c`  
		Last Modified: Thu, 24 Jul 2025 19:07:56 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bc396cc0e8d8430ca98a15a565b3f7bdb0ef26c5b0c146a30270fb89765243`  
		Last Modified: Thu, 24 Jul 2025 19:07:58 GMT  
		Size: 4.1 MB (4067230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b16dd8cc00580a661727b62784a93632f20550f34ab3f30da7b4ff8c01cf0b1`  
		Last Modified: Thu, 24 Jul 2025 22:51:59 GMT  
		Size: 75.1 MB (75064515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5a53be99c3e377cc6bc0b493f8106df5d0b07f3b3158a979ce09181b45ea67`  
		Last Modified: Thu, 24 Jul 2025 19:08:00 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.21` - unknown; unknown

```console
$ docker pull redmine@sha256:40549451179ed2554c0b6c60ac16a72a8ed476df11c1b78cecd9ff23f7be984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1393057d999e4796284832ef6507db9f33930aff368bf9c9d6f9b59899f8cdf`

```dockerfile
```

-	Layers:
	-	`sha256:69db1421d5bc3bfdf1190b95efd477b3c51bccfdfa4af49087eefcc1389fed38`  
		Last Modified: Thu, 24 Jul 2025 22:51:45 GMT  
		Size: 36.8 KB (36792 bytes)  
		MIME: application/vnd.in-toto+json
