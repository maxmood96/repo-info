## `redmine:alpine3.19`

```console
$ docker pull redmine@sha256:20d2b31a6c1f0e5da14e981bdcf9d9f57e4c4c84f63a3cbcb7cceb28b97dd690
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

### `redmine:alpine3.19` - linux; amd64

```console
$ docker pull redmine@sha256:9fb4cc8da7b4da01aa7af978e733a2b7359303345f2caae55d4db7a37b12a927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190975646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cbe4607eebff2b17a8f1876be053beedd53f47fe563f45ced83ddca29a1a51`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7062511fdb98fd35f7d3e892117015591c56398cff03fc82ebb5491087934c`  
		Last Modified: Wed, 30 Oct 2024 18:06:32 GMT  
		Size: 6.7 MB (6676589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c80382226ec2ccca0ec2cabb10a7527e0e09d2ae456014d78585f4d17f1f482`  
		Last Modified: Wed, 30 Oct 2024 18:06:31 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0c2f40aef3717e2b5bb8133148ea12192e05c8e826a6a6c038a1237bb31d34`  
		Last Modified: Wed, 30 Oct 2024 18:06:32 GMT  
		Size: 35.0 MB (34957868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96899a3f8eb6120d05577aaa9487d4d78bd3757373e1d68b0049aceed9103997`  
		Last Modified: Wed, 30 Oct 2024 18:06:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e56ba7de14bce3d5185121050e91bd3a921fe0a950efe566acc94727fc2d3d`  
		Last Modified: Mon, 04 Nov 2024 22:07:19 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d6ac23d8a4daa4c4da9a5c869404442e6dcbee0d2fe73ef9561a5cf832c3c1`  
		Last Modified: Mon, 04 Nov 2024 22:07:22 GMT  
		Size: 71.2 MB (71199551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041107f366e1cfd3095191f4290c638fb312cf49878b2590af537905b19a3b28`  
		Last Modified: Mon, 04 Nov 2024 22:07:20 GMT  
		Size: 1.2 MB (1205519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769cf520c2c0630ac062525e1631749df5cc9969539a5f64496308a7b23b9892`  
		Last Modified: Mon, 04 Nov 2024 22:07:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e64ad84dd956814915f5179cdc63055f9ee7203d0597eabc9a6985dad76f39`  
		Last Modified: Mon, 04 Nov 2024 22:07:20 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10ff37c8caf7dc794b882eaca04da8d26548b67f6aa9ee4087e144131525f6a`  
		Last Modified: Mon, 04 Nov 2024 22:07:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47de325d35917c0dc22ee2ffff688728f430065fcf67f7cf0ce245141d5f56ff`  
		Last Modified: Mon, 04 Nov 2024 22:07:21 GMT  
		Size: 3.2 MB (3249011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964f97732cff6862bf32ed78f6bbcf7aa339d07666f81b7288b5196ae6f16d77`  
		Last Modified: Mon, 04 Nov 2024 22:07:24 GMT  
		Size: 70.3 MB (70263460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870cf36e3e6e4bf857754aee4862d151419d4343faa8792e14f705733685600d`  
		Last Modified: Mon, 04 Nov 2024 22:07:21 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:4b812cd824c9db2fc7fd9e085204ece9d79e3b324ff1e91d0740b481c8cc041a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da873ba219c87cdb71f747a92555461daba7e58db23768e004604234d63e97ca`

```dockerfile
```

-	Layers:
	-	`sha256:49d8b06e7e1357142f0e2cff798536f9958e6cf342fa961f94108a0914456664`  
		Last Modified: Mon, 04 Nov 2024 22:07:19 GMT  
		Size: 42.2 KB (42218 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; arm variant v6

```console
$ docker pull redmine@sha256:d2d1376e4b5ceea7939ab2c8c6a0fdfdf4b50356647c9b254052dc00fc22d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182999551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d796eebc96a43ee959772305fc2797f5f8404f9407055c6d839f66b5c2ce6d96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:26 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Fri, 06 Sep 2024 22:49:27 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69264444991b342a828e8440fda525f638e4bbb4bc687eaf979804cb78d232ac`  
		Last Modified: Sat, 07 Sep 2024 12:26:27 GMT  
		Size: 6.5 MB (6527548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a25efb42918eb84a2ead659f9ebe7eb5b3f1eda9c633cab3dd1e03427946e5`  
		Last Modified: Sat, 07 Sep 2024 12:26:26 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac1373416cea14177e5e538715f4c8f86feb078b02c28352d94dad71eb20898`  
		Last Modified: Wed, 30 Oct 2024 18:24:16 GMT  
		Size: 31.1 MB (31110676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebe35e54cc9c4c60b5703915f6cfaae838645071d7277d947b22033dbfc3741`  
		Last Modified: Wed, 30 Oct 2024 18:24:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95556030577fee34ddd0fb4ea0247a98371c3b445483805c6dd9ba686ad1292`  
		Last Modified: Wed, 30 Oct 2024 19:07:12 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40a3bfcd5ca491d01362e969db6da8a308c2e64e30a77ffb475e0458521e57f`  
		Last Modified: Wed, 30 Oct 2024 19:07:14 GMT  
		Size: 68.1 MB (68142355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3c472d84374cf36cea84f83cd124c9ac6cfc75ad31d21212859046be579121`  
		Last Modified: Wed, 30 Oct 2024 19:07:12 GMT  
		Size: 1.2 MB (1173542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdc6e22102902c061d580e7f2e3ae6e1b4508bfc1d69cb97a9651d1f63847d6`  
		Last Modified: Wed, 30 Oct 2024 19:07:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfcfb6a4b8f373b15c17d19de25781d4ce3a14be1a9ad8ffcaf5586b608fd54`  
		Last Modified: Wed, 30 Oct 2024 19:07:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08850d4fe4c1cfb9a62b0735d97f2f9b595ea45d94bd96d18dd0584589e63cbc`  
		Last Modified: Wed, 30 Oct 2024 19:07:13 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8fa175767083519389ec47e362ff8022d758931ab0e53b7e8143d5ed62ca07`  
		Last Modified: Mon, 04 Nov 2024 22:10:42 GMT  
		Size: 3.2 MB (3248988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bddc789c7e13cfd06cb7f454396aeb541a12e07a71cc323d6e6cfe99547c527`  
		Last Modified: Mon, 04 Nov 2024 22:10:44 GMT  
		Size: 69.6 MB (69616115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232efd72e3dad5ba6eae5ac62304026bd3ddf7e1875af652751462ae4e1a920a`  
		Last Modified: Mon, 04 Nov 2024 22:10:41 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:74956b9781ce4503c8680b3a5f443debefc524359024c86822479ac46c809259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 KB (42432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a165c6876ae0de55f604fae23ee506f4a12dbf5850656e5bead141b84a93c512`

```dockerfile
```

-	Layers:
	-	`sha256:0235e6ab385a8202576f5eb0a3f6fa1630e0a0ee257f9fd5dd1bc0fc4dc1deee`  
		Last Modified: Mon, 04 Nov 2024 22:10:41 GMT  
		Size: 42.4 KB (42432 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; arm variant v7

```console
$ docker pull redmine@sha256:a289b8fc0f7966b2f0972a1627aa4779d60d1728563f1fe1d39a3d62569194d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178662999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b473692d4d637183dff68e2c045d82e499c8ff7a5bf0032e9f10406a6d3da56`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3093f5b2118a5a61c5ee3bde062500b4bd4ac9704bcc527f1571e2f21c2067`  
		Last Modified: Wed, 30 Oct 2024 18:46:49 GMT  
		Size: 6.4 MB (6369605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f348eaee68aed3739a7727e2a6a4d63c6c9674c3e991f47151ce423c046b69`  
		Last Modified: Wed, 30 Oct 2024 18:46:48 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12447b4a0744fde7cd031aeb859938d7ce76d1beb07d8e46824a7c16037395`  
		Last Modified: Wed, 30 Oct 2024 19:18:50 GMT  
		Size: 30.9 MB (30862350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3202cfabb3eae9063e235136fc4ec77d0b655d43824afc73648396c1a7d4ce20`  
		Last Modified: Wed, 30 Oct 2024 19:18:49 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f36e3ead483e69b7b2762d688250e91b7235e5a76848f13191395b6cd20554`  
		Last Modified: Wed, 30 Oct 2024 20:02:39 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ab0c5d86f6831016f75db11a838bdb48e2f0f38561b83937e8cb0af846cd8f`  
		Last Modified: Wed, 30 Oct 2024 20:02:41 GMT  
		Size: 65.5 MB (65464173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d9c1b525cc57bddfb60c1f2969984208d9cc359ba59da82a75a19a4bb636df`  
		Last Modified: Wed, 30 Oct 2024 20:02:40 GMT  
		Size: 1.2 MB (1173513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d3c8d1e2baa472b078e2ad898b0a05828f16a3d857a2a779dfe363ca2f34cd`  
		Last Modified: Wed, 30 Oct 2024 20:02:40 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa57e14f6dfe07fd71c9b1177822b87f4ec70e73ce5770f813ea4bb57d36cde`  
		Last Modified: Wed, 30 Oct 2024 20:02:40 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fc2f6c067ff78b2f3448cd337060c6d4b9ece6cf56f354b01217dfe30c67c9`  
		Last Modified: Wed, 30 Oct 2024 20:02:41 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d9bd9df39a4a094b2809d77b4c3618d342e32ef183bf4e00086f68eb15cffa`  
		Last Modified: Mon, 04 Nov 2024 23:02:03 GMT  
		Size: 3.2 MB (3248973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3ae5600b142d7237d267ad5ae393c8f2558866f6b178ba3fd2f4b3f7e5eba5`  
		Last Modified: Mon, 04 Nov 2024 23:02:05 GMT  
		Size: 68.6 MB (68612781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d92d6c9481bbf66045aa217432ea7a80a0270626414282b9d91c2e02310a00b`  
		Last Modified: Mon, 04 Nov 2024 23:02:03 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:0bc276de3e695e27e457dc54c3705ca9d442ae9d2c5b2dcaab0de58af474b69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 KB (42432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f241de0816d871b1a11e99cd9b24f3337fb8fc19542bba8c08d81c5a8a5d45`

```dockerfile
```

-	Layers:
	-	`sha256:904d8f4b88cb3a897ae169df5ec589bb3f63bbf9eaf74ce4da0823644182000e`  
		Last Modified: Mon, 04 Nov 2024 23:02:02 GMT  
		Size: 42.4 KB (42432 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:435e0f823ed7f477b56aba57916b8c32b97f064bc2133635ac5f4dc7ae77063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191377752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9555b7b2eafa942432ace9ef88f20fa28e00cbf5e533c6c378cb257a7f2133a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7efc944d69e6404f26aa744e23684069d48549113032101e05e551014e1244`  
		Last Modified: Wed, 30 Oct 2024 19:48:17 GMT  
		Size: 6.7 MB (6741399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11970cb63611b818e2f817008e7f4ca12e6e042259a6b931c02874f1638e3118`  
		Last Modified: Wed, 30 Oct 2024 19:48:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5908004a939ea80aa2faf5ea1d845d26f54bf2000843939b13fd8c7f874d87bc`  
		Last Modified: Wed, 30 Oct 2024 19:48:18 GMT  
		Size: 34.9 MB (34856728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377802820f92ea7b3951239751f54aff170feef85c38e54135f2d68b310a0607`  
		Last Modified: Wed, 30 Oct 2024 19:48:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8432592d1ab278e97f40c76608a0063fb10cc677d2bb4716bf47c1fce5196`  
		Last Modified: Mon, 04 Nov 2024 23:20:17 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d712f3016f782f0d2f6750dc8bc969ff4d53d3e06bc99b794b79013a4702dbc1`  
		Last Modified: Mon, 04 Nov 2024 23:20:20 GMT  
		Size: 71.7 MB (71683972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f81603bcd6a1ac14e85826234ed5c42e41909d04b0c14dfea0780795f8da71`  
		Last Modified: Mon, 04 Nov 2024 23:20:18 GMT  
		Size: 1.1 MB (1135606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4d14a9988d5dc20440b2e16f6b3a9da5d929fe4b9c9f4789102ab6ef7a539a`  
		Last Modified: Mon, 04 Nov 2024 23:20:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a69f0669acb4bdf2e4dbc72a60754700c2f6fbd8dd3a4c0c5bb29d433027e1`  
		Last Modified: Mon, 04 Nov 2024 23:20:18 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6b3280b09a215afd69176ad2ec3ea3ba1c7e8edb581657d594213f11ba74af`  
		Last Modified: Mon, 04 Nov 2024 23:20:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8cec043c8d92a475c06074624eacc053d116c5ffcd2812245ca68b2150850f`  
		Last Modified: Mon, 04 Nov 2024 23:20:19 GMT  
		Size: 3.2 MB (3248975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a69150473fd93dad881eca7887faaf0579959824040a833d9ced9a52c8e5cb`  
		Last Modified: Mon, 04 Nov 2024 23:20:22 GMT  
		Size: 70.3 MB (70348032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f7588bb4e51edd52d86760a5821550460671de79dd6cd41fb804b28bebd013`  
		Last Modified: Mon, 04 Nov 2024 23:20:20 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:5024480aecde2c1182b60c9c83d7be1c5f5ab8b08d79377d0096059e419c9778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 KB (42472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c10ca589a78e291122561cf3699077ac577283a86a8215bf03f8e0f0ae61d0`

```dockerfile
```

-	Layers:
	-	`sha256:5066c509071672f5dc466a05624f45d5a253c76cd5e6187446789fbb5bcc98bd`  
		Last Modified: Mon, 04 Nov 2024 23:20:17 GMT  
		Size: 42.5 KB (42472 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; 386

```console
$ docker pull redmine@sha256:4aee56e802b7486b4beafaa3e11a0a7fc21b69d90360bcd3bb263f739de6e99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187657614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2946a278ffde63bfb9505e14a043a008c6259c0ba9cfe707bca1b6830e0f089d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e612476124f6bc697657ddb6b253b022b5faaf3df1f458ef5657cbed5a6843f7`  
		Last Modified: Wed, 30 Oct 2024 18:06:17 GMT  
		Size: 6.7 MB (6743125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59be62dfa74b29bab5980b32e50752d3a104042d964ae082cf9c0a0ed64ce77d`  
		Last Modified: Wed, 30 Oct 2024 18:06:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233d7b4cd95125286a98e8234d1766f2d0d3cdd5214008758fb506d37020b113`  
		Last Modified: Wed, 30 Oct 2024 18:06:18 GMT  
		Size: 31.1 MB (31125375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840611c4faec59920a9e867b22687b9e555c641d6e8db348ed541d01ab15be71`  
		Last Modified: Wed, 30 Oct 2024 18:06:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bc607739f5e5d828bc3d38a9c55d83edef55e36ff16ad7bfddc4d9206ff066`  
		Last Modified: Mon, 04 Nov 2024 22:07:20 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b225787f845a9fe279d43ed2df37f0e3474ee31eb6e7180f95217441a8c87f72`  
		Last Modified: Mon, 04 Nov 2024 22:07:22 GMT  
		Size: 71.7 MB (71701690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302f5a4ee70bbf9b851d3b83b9fccc53fe1e02e0705dfb6b154df9b5bd5d4247`  
		Last Modified: Mon, 04 Nov 2024 22:07:20 GMT  
		Size: 1.2 MB (1182472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f653effb09a707c4bc9006bc87974ae203d2046f464971b19ed08091079df3`  
		Last Modified: Mon, 04 Nov 2024 22:07:20 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979a640f65cea8b8b575c7c57ec18d88bcc6a0cb6947c1dbfbe26e46cb647151`  
		Last Modified: Mon, 04 Nov 2024 22:07:20 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b5150ca6f4c2f241ab44ecc6b353c8070274277de1824c04480f397ac425f3`  
		Last Modified: Mon, 04 Nov 2024 22:07:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e55ac3e8fdec446a3a73105fcbf458c3ece08d6d2fc6e237e1738f8f728e34`  
		Last Modified: Mon, 04 Nov 2024 22:07:21 GMT  
		Size: 3.2 MB (3248977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807ac719a8099d7a66ea3be05b6f6f278c5c01299c44dba96b90340093ff7398`  
		Last Modified: Mon, 04 Nov 2024 22:07:23 GMT  
		Size: 70.4 MB (70398426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c867802d223420dc56a2396d8ca9ec47c380285089216e3dc230e6ee5a8ede`  
		Last Modified: Mon, 04 Nov 2024 22:07:21 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:a9e34d6e0512786c257795303045bb9bc504d10948f2e6527896472e47b66256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44f55410a6cb79a646793056ee28ed6331a9df852fffddb96a0de5269cfe0dd`

```dockerfile
```

-	Layers:
	-	`sha256:ed4f77f30ac93d3dab7ab61d5f617145b6b8c63f9a914c242f8b6dcebaba85cc`  
		Last Modified: Mon, 04 Nov 2024 22:07:20 GMT  
		Size: 42.2 KB (42174 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; ppc64le

```console
$ docker pull redmine@sha256:05ec714ab0e266dd9e55acb37d21a30490750663ec744fa0ed38f4ded33ae4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192194802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f0981ea6c7d5c7a296760710df66f2d50f95c2dab9606a36072deffc1b38cc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6331ab697e4f5f4d9d5b11fc59a326abe5becee150a17a07fedcdf12b17f86a`  
		Last Modified: Wed, 30 Oct 2024 18:36:10 GMT  
		Size: 6.9 MB (6903386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474b601c722591b310b79a24a75b36810c3633b9cac1715ce84a0697bf770d48`  
		Last Modified: Wed, 30 Oct 2024 18:36:09 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd1751961b94574edb78fd96c7f9ba9367df601b8f5cd43f18460b59708ed6`  
		Last Modified: Wed, 30 Oct 2024 19:00:30 GMT  
		Size: 32.5 MB (32538748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54497a396e46ca1920c5ec1e1727fca91b5f506a7d672c096f156c3087fe284a`  
		Last Modified: Wed, 30 Oct 2024 19:00:29 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9887bf9dd8b445f5a57aace40f70a2d8e0cdcc4f0e12245cbd02191058b56b`  
		Last Modified: Mon, 04 Nov 2024 23:40:42 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfb3fdad3ab78c067c78c59e3e5bb07ad8c0dd1bacb564b8893d8d323fec464`  
		Last Modified: Mon, 04 Nov 2024 23:40:45 GMT  
		Size: 72.8 MB (72816459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98377baa9f32665476537e835d109cc70abb107e7f3fd832f53a4bd196641935`  
		Last Modified: Mon, 04 Nov 2024 23:40:43 GMT  
		Size: 1.1 MB (1123268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a86ba08f4bfd0f69f0c32c0cf4286a0cb2a726644fb9267f3f104fd8cbd123`  
		Last Modified: Mon, 04 Nov 2024 23:40:42 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a258d21d944774a53ef60216147b3567034b0850ad5aa4463ec3a32ec0adb8`  
		Last Modified: Mon, 04 Nov 2024 23:40:43 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5414b9621b474a6c25566f480c0ee1b18a4d92a1561b4192813020378dca9a0d`  
		Last Modified: Mon, 04 Nov 2024 23:40:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695a03ca4af117461df490b57e0e2a4d70af9acc6081462e1aadfbd02f949396`  
		Last Modified: Mon, 04 Nov 2024 23:40:44 GMT  
		Size: 3.2 MB (3249013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7dcbe1def2f9a1153821f26ed4a5f501fda83771140b0eb0ec84f4689a78c1`  
		Last Modified: Mon, 04 Nov 2024 23:40:47 GMT  
		Size: 72.2 MB (72195519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8200f474c20865f916c053844abf68378a456eeed927f2afe3d112aafa8ca`  
		Last Modified: Mon, 04 Nov 2024 23:40:44 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:aa2baf881f5050da4ad9bfa5d9ee0b3a27e21b6bbe1b88c209e903f5eb42c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 KB (42334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c423e940a25b60c571cb494452c0e55d407b0f100e18e8dcef6eb0dfb1b93417`

```dockerfile
```

-	Layers:
	-	`sha256:6a7c94786452803838f594f4c512c8ff083bebb31b6cb689b523b10baa528c62`  
		Last Modified: Mon, 04 Nov 2024 23:40:42 GMT  
		Size: 42.3 KB (42334 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:alpine3.19` - linux; s390x

```console
$ docker pull redmine@sha256:ccc833f3607ae4f73754fb26b38af71d89c1900cc1a76147fdc97d5c8e43e7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190529610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe67a1772f52b8e5be996fa061ce6cdec8869d2ae101e9c56026f1d42891975`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV LANG=C.UTF-8
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_VERSION=3.2.6
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.6.tar.xz
# Wed, 30 Oct 2024 11:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=671134022238c2c4a9d79dc7d1e58c909634197617901d25863642f735a27ecb
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 30 Oct 2024 11:03:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 11:03:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 30 Oct 2024 11:03:14 GMT
CMD ["irb"]
# Mon, 04 Nov 2024 03:38:11 GMT
RUN addgroup -S -g 1000 redmine && adduser -S -H -G redmine -u 999 redmine # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ca-certificates 		findutils 		tini 		tzdata 		wget 				breezy 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		ghostscript-fonts 		imagemagick 	; # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in Redmine 5.2+) # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV RAILS_ENV=production
# Mon, 04 Nov 2024 03:38:11 GMT
WORKDIR /usr/src/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
ENV HOME=/home/redmine
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_VERSION=5.1.4
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.4.tar.gz
# Mon, 04 Nov 2024 03:38:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=f5738d6a107f231b8f4b0ae5410e0c45742d75e0ef30c4b31a27c0ac9dafd51c
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENV BUNDLE_FORCE_RUBY_PLATFORM=1
# Mon, 04 Nov 2024 03:38:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetds-dev 		gcc 		make 		mariadb-dev 		musl-dev 		patch 		postgresql-dev 		sqlite-dev 		ttf2ufm 		zlib-dev 	; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		rm /usr/local/bundle/gems/rbpdf-font-1.19.*/lib/fonts/ttf2ufm/ttf2ufm; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/bundle/gems 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redmine-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
VOLUME [/usr/src/redmine/files]
# Mon, 04 Nov 2024 03:38:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 04 Nov 2024 03:38:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Nov 2024 03:38:11 GMT
EXPOSE map[3000/tcp:{}]
# Mon, 04 Nov 2024 03:38:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6799a9649d3cda9821aa55fa6db8802a8e4bd99fec48ccc0f3d5931333ba2616`  
		Last Modified: Wed, 30 Oct 2024 18:44:31 GMT  
		Size: 7.1 MB (7051981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf3334cf4016e7dbebc5fa3803ee374b8d985649b8ab3bcc1a89ba334ec3c10`  
		Last Modified: Wed, 30 Oct 2024 18:44:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce635c1d3a269ca35f60cb0a0a551b6b2c613165472d0abaaee6e3d1b15aebe7`  
		Last Modified: Wed, 30 Oct 2024 19:36:48 GMT  
		Size: 32.3 MB (32284479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818f38a0c79a0c51c2eeb916b8f2de0bc72f7ccce17ccf664356aa94e07d497d`  
		Last Modified: Wed, 30 Oct 2024 19:36:48 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59cea4acec6b27d16c21c2bcd770f467dee47da26d94eec48968086be58e9bb`  
		Last Modified: Mon, 04 Nov 2024 23:23:02 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05da617f7cd401698f4aad565d3f20c67452097675a43a8119b3fa96bd6bc37a`  
		Last Modified: Mon, 04 Nov 2024 23:23:04 GMT  
		Size: 72.1 MB (72061131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228eb181ffd4faf8a9094dd78cc1519b3c0568149e9e43e2251e4f8791abf6c`  
		Last Modified: Mon, 04 Nov 2024 23:23:02 GMT  
		Size: 1.2 MB (1172765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553c371c0df9b7beb11b7d1edb9be5787a712afaababa5d84c67d8f6d49a52a8`  
		Last Modified: Mon, 04 Nov 2024 23:23:03 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c6cdf7af60b30224bb8455b014ceec7e9c66f5410c37fca82e54fae79bfacf`  
		Last Modified: Mon, 04 Nov 2024 23:23:03 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc65af23ea1adb75547234f601981174af06d59130dd858626e91f554d1f2614`  
		Last Modified: Mon, 04 Nov 2024 23:23:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2bcac8f9ef01c9647c02932afd8e5be74cc22efbea51cb1db897be3701ff8d`  
		Last Modified: Mon, 04 Nov 2024 23:23:04 GMT  
		Size: 3.2 MB (3248961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bd1abd200a3d462e33387689119fb81c010b7d619fadf1e88e9e5eb6f4a250`  
		Last Modified: Mon, 04 Nov 2024 23:23:06 GMT  
		Size: 71.5 MB (71452996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768dace4489891daf88d441b25c20b0193dd55288410b7f811f95eb87fc9a4aa`  
		Last Modified: Mon, 04 Nov 2024 23:23:04 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:alpine3.19` - unknown; unknown

```console
$ docker pull redmine@sha256:6525cbdc525547a2ccdc8bd6abbd4dad56bce8c752fd3d06dac7c7e46debc37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 KB (42278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c173c6786c2616509cf8ad0d548f2480b7a7e84116d473574569a380622deb3`

```dockerfile
```

-	Layers:
	-	`sha256:d4dad668bc3ae4e6e543d7c1e248c07f52f9fe3ff486d115c0425751a050d340`  
		Last Modified: Mon, 04 Nov 2024 23:23:02 GMT  
		Size: 42.3 KB (42278 bytes)  
		MIME: application/vnd.in-toto+json
