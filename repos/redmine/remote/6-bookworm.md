## `redmine:6-bookworm`

```console
$ docker pull redmine@sha256:329b45330030947c2832bafa1ef1ad3477441c08c0f916fad77cd86a4c6db1a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `redmine:6-bookworm` - linux; amd64

```console
$ docker pull redmine@sha256:5ab07af81f66b2d65a12329551ff50f0e6c726d67b0acb85f153a9fcc64d8d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268085488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37895e181da25c69fe7a3d4ac866f77f09f2514715dfab8ca6d918271de98482`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Wed, 17 Dec 2025 20:04:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:04:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:07:05 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:07:05 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:07:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:07:05 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:07:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:07:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:07:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:07:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:07:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:07:05 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:10:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 17 Dec 2025 21:10:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:10:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Dec 2025 21:10:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Dec 2025 21:10:56 GMT
ENV RAILS_ENV=production
# Wed, 17 Dec 2025 21:10:56 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Dec 2025 21:10:56 GMT
ENV HOME=/home/redmine
# Wed, 17 Dec 2025 21:10:56 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 17 Dec 2025 21:10:56 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 17 Dec 2025 21:10:56 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 17 Dec 2025 21:10:56 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 17 Dec 2025 21:10:56 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 17 Dec 2025 21:10:59 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 17 Dec 2025 21:11:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 17 Dec 2025 21:11:35 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Dec 2025 21:11:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 21:11:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:11:36 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 17 Dec 2025 21:11:36 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a965a9f93412cde0ce9b144523251fd5201cc48e9d563b473016cbfeb807861b`  
		Last Modified: Wed, 17 Dec 2025 20:07:23 GMT  
		Size: 3.5 MB (3509637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a07a60d9628c1a61cda7e61024ea9a0c04871b78714c528c87df1146020d9`  
		Last Modified: Wed, 17 Dec 2025 20:07:23 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffb5a285b97a3d05777093f2fee0c061e9996578b76c3332be9ec9c1543ebf5`  
		Last Modified: Wed, 17 Dec 2025 20:07:27 GMT  
		Size: 41.4 MB (41443832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f779815c03bf54b64c316fce22dfd62f63f0db4b6097a355d7dd9b9c231c68`  
		Last Modified: Wed, 17 Dec 2025 20:07:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5116ff0fc32ce0060e150e278a79a69c1000421a9e3e495f918ca2b57cc5ef24`  
		Last Modified: Wed, 17 Dec 2025 21:12:07 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df8c91e562ccc6977a89f016bff897b78514d6122984a2951d44b5a62b5e65d`  
		Last Modified: Wed, 17 Dec 2025 21:12:21 GMT  
		Size: 123.1 MB (123134448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eca1fc4dbbd88539fb6b1a0e306c219a4c7cc00b81f93c1799add3914f47fc`  
		Last Modified: Wed, 17 Dec 2025 21:12:08 GMT  
		Size: 946.3 KB (946343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b19ab4002ad3c37f525e3877e9016abefb28bca6cc5a00b605db3a37208b7f`  
		Last Modified: Wed, 17 Dec 2025 21:12:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5997de9416bc6ed13ea8eaae3c34f40d59acd000b4e4a3cc40a0a4e4adefe125`  
		Last Modified: Wed, 17 Dec 2025 21:12:08 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eca7b39594d4af139e57eb9051edefc13b155b277aaa9f6f33b7f5f252fac3`  
		Last Modified: Wed, 17 Dec 2025 21:12:08 GMT  
		Size: 4.1 MB (4139973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae266969d6990adc126400627206c8e996d9495c2fa370945ccad94c3939e15`  
		Last Modified: Wed, 17 Dec 2025 21:12:13 GMT  
		Size: 66.7 MB (66678720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c590e2f3df96d9cc4f26cdd32c703710bdb4cf9fae46b0425e4a8d56bc011`  
		Last Modified: Wed, 17 Dec 2025 21:12:08 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:394e7e40568de14b15ecbd66adb4b204a2cba6ea596fe24ee62a49deff3b027c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 KB (40573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383388a1bca54355a25e216a7794966593ba4be861a32e721dec11432b5deb57`

```dockerfile
```

-	Layers:
	-	`sha256:2f218258ea0c4034e4373a14d61fbbdd1f15154123d040bbbc9887e4908ced60`  
		Last Modified: Wed, 17 Dec 2025 23:51:32 GMT  
		Size: 40.6 KB (40573 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:aa3f77dba8d9365cc7905dbbd0dc6e2a9a92b62a7e8bdc7dec7e92ec0b2bc57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264902787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338ce20bb620f5685b03d8684d0d6fff774c61313b092e263ba01c9e12eb9692`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Wed, 17 Dec 2025 20:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:04:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:07:12 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:07:12 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:07:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:07:12 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:07:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:07:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:07:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:07:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:07:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:07:12 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:11:20 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Wed, 17 Dec 2025 21:11:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 21:11:52 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Dec 2025 21:11:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Dec 2025 21:11:52 GMT
ENV RAILS_ENV=production
# Wed, 17 Dec 2025 21:11:52 GMT
WORKDIR /usr/src/redmine
# Wed, 17 Dec 2025 21:11:52 GMT
ENV HOME=/home/redmine
# Wed, 17 Dec 2025 21:11:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Wed, 17 Dec 2025 21:11:52 GMT
ENV REDMINE_VERSION=6.1.0
# Wed, 17 Dec 2025 21:11:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-6.1.0.tar.gz
# Wed, 17 Dec 2025 21:11:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=bc483da195f2444491d870e40f7fc909ae750f7ba8d0e28831e6d6c478812b88
# Wed, 17 Dec 2025 21:11:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Wed, 17 Dec 2025 21:11:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Wed, 17 Dec 2025 21:12:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libclang-dev 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 17 Dec 2025 21:12:33 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 17 Dec 2025 21:12:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Dec 2025 21:12:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:12:33 GMT
EXPOSE map[3000/tcp:{}]
# Wed, 17 Dec 2025 21:12:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad422abcd8e8d21b87822e5fe1505d30aa217f8c12351f15c8a8fbb790f2bc5`  
		Last Modified: Wed, 17 Dec 2025 20:07:29 GMT  
		Size: 3.3 MB (3340667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e14228785f521833140d5d945fde586a15a4fd2b7cb841f6a55d5904852eae`  
		Last Modified: Wed, 17 Dec 2025 20:07:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeff4096472a851799536ef984aabbd8d6de81e7944bab36633f9d823b38249`  
		Last Modified: Wed, 17 Dec 2025 20:07:35 GMT  
		Size: 41.3 MB (41329919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c085a490b7cceb5713145af8005a5a7aaeffd151c23e9d77598f280ae34614c`  
		Last Modified: Wed, 17 Dec 2025 20:07:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d905f4d6cd790d5e74644313858debe60f568ac1d3c3b16e227944ae5e8be410`  
		Last Modified: Wed, 17 Dec 2025 21:13:10 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eb01532f692d9c6551b5b429974061e8f54f14bb79767ce7a940735d1728c6`  
		Last Modified: Wed, 17 Dec 2025 21:13:41 GMT  
		Size: 120.5 MB (120479832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abea06403229868ff4d66ec365bf3d18d3938a388a1d2524ebed28030ce48408`  
		Last Modified: Wed, 17 Dec 2025 21:13:10 GMT  
		Size: 900.0 KB (899969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d72cf36fe669f4723cad2580ee24d7c04cabaf95c8c85253a60f57938a7f768`  
		Last Modified: Wed, 17 Dec 2025 21:13:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b691207829fcf9ab53717823e153253deb9e5f1a4ffd6aee6b43235806e2e7`  
		Last Modified: Wed, 17 Dec 2025 21:13:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a04fc97a79dbe9480d71faba096c914abf78659a7a7f6b37bb3b0833780c47f`  
		Last Modified: Wed, 17 Dec 2025 21:13:11 GMT  
		Size: 4.1 MB (4139973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a522af86aa1a876c1f0d61c50eb5870101cd33d12c3281a66cfdf531d79fbeba`  
		Last Modified: Wed, 17 Dec 2025 21:13:15 GMT  
		Size: 66.6 MB (66606080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5554d5bb96ebe1316a1e49da51b1269d45bbb19a912dbf286a49a7d023220eae`  
		Last Modified: Wed, 17 Dec 2025 21:13:11 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:6-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:12f45693f9310add72f6b0b7e11d048f94214a596ea97bc59a25a6d8a0b4b84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 KB (40752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c9d7ea9918d179ef09fd0b4a8987ffb0ef9dd54cce345dffb3921f854be832`

```dockerfile
```

-	Layers:
	-	`sha256:9d2cf44bf60c24b39a36887664883b554535ddbc6e0c68b3a25128b81d10f71d`  
		Last Modified: Wed, 17 Dec 2025 23:51:36 GMT  
		Size: 40.8 KB (40752 bytes)  
		MIME: application/vnd.in-toto+json
