## `redmine:5-bookworm`

```console
$ docker pull redmine@sha256:19f5423b11cf25b642c737d374621fdc2ae534d2575fa3457643717465409e6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redmine:5-bookworm` - linux; amd64

```console
$ docker pull redmine@sha256:8164697cc120c6563d3cafa7923477ac3536db1669cd28c02860f3f7becff8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249316069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7566eb9573a31d1b50b912a8b0e5102526e557ee0a4bdbbc2af27a76b9734b2e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:30:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:32:54 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:32:54 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 02:32:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 02:32:54 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 02:32:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:32:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:32:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:32:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:32:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:32:54 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:36:27 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 07 Apr 2026 03:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:36:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 03:36:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 03:36:58 GMT
ENV RAILS_ENV=production
# Tue, 07 Apr 2026 03:36:58 GMT
WORKDIR /usr/src/redmine
# Tue, 07 Apr 2026 03:36:58 GMT
ENV HOME=/home/redmine
# Tue, 07 Apr 2026 03:36:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 07 Apr 2026 03:36:58 GMT
ENV REDMINE_VERSION=5.1.12
# Tue, 07 Apr 2026 03:36:58 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Tue, 07 Apr 2026 03:36:58 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Tue, 07 Apr 2026 03:36:58 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 07 Apr 2026 03:37:00 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 07 Apr 2026 03:37:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 03:37:33 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 07 Apr 2026 03:37:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 03:37:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:37:33 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 07 Apr 2026 03:37:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a2f62ccbdd4f96866ec34d9038e30a7e3e2032812b0d14dc0b72d6c32839bb`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 3.5 MB (3510220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488e98f61afb008694e765a3e3cd336997f6441617c72b14f054323676671a3`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bc7dd9050b32d5189edd6dc83aafeeab67823832bc0cf9f88dbfdbe36f1de8`  
		Last Modified: Tue, 07 Apr 2026 02:33:05 GMT  
		Size: 35.8 MB (35781374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428046dab03b578219772e5157ba6906f54d3bbe6f50c55c2bd97a4a92733340`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514dea002c425c88496e1b619a1ea7afddab05ea89c6a7a8aea73cfd8a07cc42`  
		Last Modified: Tue, 07 Apr 2026 03:37:48 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fb95047fb480323de884c6b4b3ee76fd4547b9b6df190605069cfde6b20242`  
		Last Modified: Tue, 07 Apr 2026 03:37:52 GMT  
		Size: 123.0 MB (122951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9b24e366a3807e897a1be0d99dc0d67885473be4566cf86683695edd297a91`  
		Last Modified: Tue, 07 Apr 2026 03:37:49 GMT  
		Size: 947.2 KB (947195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eef54af160a6aa672965b50b8fcfddb10bf94c1a19be2194ade7398d1f60413`  
		Last Modified: Tue, 07 Apr 2026 03:37:49 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b015c2c75eece451cc9c5b068f500e6eb7b7087134f8793872823c46748af7e`  
		Last Modified: Tue, 07 Apr 2026 03:37:50 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b8888a913e8009dc378a7a4f478125106b18bdd257a0e978fa697f16ac8ce`  
		Last Modified: Tue, 07 Apr 2026 03:37:50 GMT  
		Size: 3.3 MB (3253566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5281a54e55d45593d7b5f9135a6c39a7aed7eb6c19b5857626078d43150120d`  
		Last Modified: Tue, 07 Apr 2026 03:37:52 GMT  
		Size: 54.6 MB (54631676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f7816cff7a6914187bc5a30d55aab63e7a4fca7af8213755d54c8ad7bcd294`  
		Last Modified: Tue, 07 Apr 2026 03:37:51 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:0f588eb36b5c0cc89f1fbb35a8c5d0bcf3f8dedbeb4f44aa9f12cfbf71ba0918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddad00bf592aa14a035af5ad310fcc266e5146cf59a87543d86f274ade7d380d`

```dockerfile
```

-	Layers:
	-	`sha256:9908015623b56df07da95df2e82f22c820b8ab6ad781891298deb8daaeb127fd`  
		Last Modified: Tue, 07 Apr 2026 03:37:48 GMT  
		Size: 40.2 KB (40158 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:e292cfe7a24929854695bc03aae050ec2176cc27430d0db3091321d8fbde5aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233536810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace78709a3573dca0ddef46956a800993c86420f4cc7ffa1318bd8150db174d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:42:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:45:23 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:45:23 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 03:45:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 03:45:23 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 03:45:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:45:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:45:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:45:23 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:38:40 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 07 Apr 2026 04:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:39:23 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 04:39:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 04:39:23 GMT
ENV RAILS_ENV=production
# Tue, 07 Apr 2026 04:39:23 GMT
WORKDIR /usr/src/redmine
# Tue, 07 Apr 2026 04:39:23 GMT
ENV HOME=/home/redmine
# Tue, 07 Apr 2026 04:39:24 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 07 Apr 2026 04:39:24 GMT
ENV REDMINE_VERSION=5.1.12
# Tue, 07 Apr 2026 04:39:24 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Tue, 07 Apr 2026 04:39:24 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Tue, 07 Apr 2026 04:39:24 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 07 Apr 2026 04:39:26 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 07 Apr 2026 04:40:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 04:40:07 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 07 Apr 2026 04:40:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 04:40:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 04:40:07 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 07 Apr 2026 04:40:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4748d6bbb5a5b9e671dcabe2f909bdd7514f760a5cfdcd37d5b04627424120f2`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 25.8 MB (25765667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b4426e57bea0b833df8594d2540044d7a21e1274e68bf45fa3cdf2e8fa0ac8`  
		Last Modified: Tue, 07 Apr 2026 03:45:31 GMT  
		Size: 3.1 MB (3081038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f153981f06f92b8d22f8da0e634bf0fe6714689fb7ab0bcfc1baf1b9c2b621f1`  
		Last Modified: Tue, 07 Apr 2026 03:45:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8b2805588972951a4fbc43a40b26713ce4e2f5ac1b697daa21190108858763`  
		Last Modified: Tue, 07 Apr 2026 03:45:33 GMT  
		Size: 32.1 MB (32079179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c367451fbd7179ee48ece11d1e1dc60497b8a415cf2e9a0f8ec2befab82ebcb7`  
		Last Modified: Tue, 07 Apr 2026 03:45:31 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91a46f7f4d44001a1302e65e9f3756295a1f0c498c61b8ef968927d2ea7d046`  
		Last Modified: Tue, 07 Apr 2026 04:40:23 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de621ae5d9c101ed9429f7211f300b6a0be4a53e0f69629a2a17032b00858e1`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 116.6 MB (116632958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a63e4ae0955bf69b13b686dd4f05ee331229d50aa9d26fd741b54b7146579d`  
		Last Modified: Tue, 07 Apr 2026 04:40:23 GMT  
		Size: 916.8 KB (916823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363f72ba8d84461d7c2a9b60534eff55958bc6d9095713a8ca437682548337d1`  
		Last Modified: Tue, 07 Apr 2026 04:40:23 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf6e3021d5b1ca198ff2648b7924fe7b1017db4737d7283e0f128d68718694b`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71caf5b6ed949b41af00913ffa1c6c848a717b44e46c794126606211956ff6f6`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 3.3 MB (3253560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9921cfda1e37d7b45d5f05589dcdf25605d3b714cea7edfb1e4dcc4c2f87b3a7`  
		Last Modified: Tue, 07 Apr 2026 04:40:26 GMT  
		Size: 51.8 MB (51803466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431fe91c01ed9469424cd31935182d81fca41805cc7ebbf68bca9209dae04ab2`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:e6a08c91b9882458f89f2fe60c55788ed13eddf0eead8839caf437514b413126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837bd44f0b850a0aa7370ffb113f0eb38fb724064f8c92cad5c16c6a96a5f147`

```dockerfile
```

-	Layers:
	-	`sha256:ec8a5b8969b522d834b5e47fceacb4e67791859c931f1a5f26d02ff0795362df`  
		Last Modified: Tue, 07 Apr 2026 04:40:22 GMT  
		Size: 40.3 KB (40296 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:05e128c9708796d162347ce2c040549883fc522503b845dbc36d231a84eb70d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226598712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4560d47e88310c9ce1add684b8ad83b5e29d4d98b3ef6495bd9e54e831e65f67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:16:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:16:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:23:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:23:53 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 03:23:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 03:23:53 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 03:23:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:23:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:23:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:23:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:23:53 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:36:40 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 07 Apr 2026 04:37:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:37:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 04:37:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 04:37:15 GMT
ENV RAILS_ENV=production
# Tue, 07 Apr 2026 04:37:15 GMT
WORKDIR /usr/src/redmine
# Tue, 07 Apr 2026 04:37:15 GMT
ENV HOME=/home/redmine
# Tue, 07 Apr 2026 04:37:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 07 Apr 2026 04:37:15 GMT
ENV REDMINE_VERSION=5.1.12
# Tue, 07 Apr 2026 04:37:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Tue, 07 Apr 2026 04:37:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Tue, 07 Apr 2026 04:37:15 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 07 Apr 2026 04:37:18 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 07 Apr 2026 04:37:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 04:37:55 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 07 Apr 2026 04:37:55 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 04:37:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 04:37:55 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 07 Apr 2026 04:37:55 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44696ece9e073f10315496957fbd053f03d988a2cbc41378207739fc6f1fece4`  
		Last Modified: Tue, 07 Apr 2026 03:18:45 GMT  
		Size: 2.9 MB (2913806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044da362ff6c56b57b64acec7e2f7c31e3b9912f6f4e987e7c71d8df1e19b944`  
		Last Modified: Tue, 07 Apr 2026 03:18:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc8e815d6ae2ee8db531fc723385404da3e1ac706e43ab27101a062226208f`  
		Last Modified: Tue, 07 Apr 2026 03:24:02 GMT  
		Size: 31.9 MB (31910112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e36dd7e1aae93f70026fae2e3b261cfccc10cafa167c64166ddfb699c13f2`  
		Last Modified: Tue, 07 Apr 2026 03:24:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2f2232b26973ec0f3fe050eea6f83c65c2c7c640be5839489407affe91c013`  
		Last Modified: Tue, 07 Apr 2026 04:38:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f43794e03ce4bc75e0bb5c5b0f910864160507d85bdd8547cf1f78963dd0fb`  
		Last Modified: Tue, 07 Apr 2026 04:38:12 GMT  
		Size: 112.0 MB (112025911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c729e7c63c6b5ea51e9033206bbf8a13f0521b493ab88417c6234b9c48d87a33`  
		Last Modified: Tue, 07 Apr 2026 04:38:09 GMT  
		Size: 912.4 KB (912372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9cad8826d6a4a1856be6ed67e65e7079a815e6c2f399c5091ab9d1ec7c10b9`  
		Last Modified: Tue, 07 Apr 2026 04:38:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d88f6de8055947a8b87eee442a3a02a56f03d4a80741e8de2ecca6e734f53e`  
		Last Modified: Tue, 07 Apr 2026 04:38:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d125b861cb60bb55a30b47d9aa12cfdfb37c888136ea5330b6a897fb34fbc0aa`  
		Last Modified: Tue, 07 Apr 2026 04:38:11 GMT  
		Size: 3.3 MB (3253559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333e29f0ff77b2c27685ead7ccb8f37a7ba0dba54d347b9a15277acf9610c09a`  
		Last Modified: Tue, 07 Apr 2026 04:38:12 GMT  
		Size: 51.6 MB (51637372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb844277822d7f4b58aa8733831986b7a51ce90b5fa6f9fd3608d7e1b6b4738`  
		Last Modified: Tue, 07 Apr 2026 04:38:12 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:6b3576424b587843a386880d06faa4e807c1b7e7d2c1e66817d0269630e8e817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8100eff4abe2416785ad520c6bca82b7e2a4c7f6f25170cbde7d37d2a72a3e4a`

```dockerfile
```

-	Layers:
	-	`sha256:b1623976253672f22e03c68ad61bba12f556eeab209e47a148d903543feec388`  
		Last Modified: Tue, 07 Apr 2026 04:38:09 GMT  
		Size: 40.3 KB (40296 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:caa1f7301133ff1c676cea043a5082e665c3e821cc95791d16bd23c8ade881b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 MB (245740504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ac3dd771ff5dbdb31a1c9cddeeeab2bd890bf4b42eb105afa7f14de9b6cb5f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:36:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:38:34 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:38:34 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 02:38:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 02:38:34 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 02:38:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:38:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:38:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:38:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:38:34 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:38:34 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:44:35 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 07 Apr 2026 03:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:45:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 03:45:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 03:45:06 GMT
ENV RAILS_ENV=production
# Tue, 07 Apr 2026 03:45:06 GMT
WORKDIR /usr/src/redmine
# Tue, 07 Apr 2026 03:45:06 GMT
ENV HOME=/home/redmine
# Tue, 07 Apr 2026 03:45:06 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 07 Apr 2026 03:45:06 GMT
ENV REDMINE_VERSION=5.1.12
# Tue, 07 Apr 2026 03:45:06 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Tue, 07 Apr 2026 03:45:06 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Tue, 07 Apr 2026 03:45:06 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 07 Apr 2026 03:45:08 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 07 Apr 2026 03:45:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 03:45:40 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 07 Apr 2026 03:45:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 03:45:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:45:40 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 07 Apr 2026 03:45:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4b814341080ea0669ffdb8c1e02e5c2a116c4608d198a3d08f3c029924756b`  
		Last Modified: Tue, 07 Apr 2026 02:38:44 GMT  
		Size: 3.3 MB (3341530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46ba08e757dcafac0ac5f396798db88ed260293c5ee020748674a9f8f514b0`  
		Last Modified: Tue, 07 Apr 2026 02:38:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b295af23ac90626d176903210387bff25716d874ba37ab991dc39f79e83bd0a`  
		Last Modified: Tue, 07 Apr 2026 02:38:45 GMT  
		Size: 35.7 MB (35687819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a722297e2a7d7c8ca69099b282161bb3a9e93ee8805c99b7812a8929cd4fb64`  
		Last Modified: Tue, 07 Apr 2026 02:38:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b930021b3ebe9970a75799003944ab45362ac0663a91cbe9e5c6f37b579f5f21`  
		Last Modified: Tue, 07 Apr 2026 03:45:56 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677dbfcf3268a597e7bcff55ee1770760c30ee8aa3b7cca19cd47547d39a73f`  
		Last Modified: Tue, 07 Apr 2026 03:45:59 GMT  
		Size: 120.4 MB (120413862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db99bee3f5c7ac38733ce3bfbce2fe632439203a064058cbd02123b73427e4c`  
		Last Modified: Tue, 07 Apr 2026 03:45:56 GMT  
		Size: 900.8 KB (900797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0628ba5ba55a2493b4e2c788cde2cf3979068e88404de993086497fe5d6e0c`  
		Last Modified: Tue, 07 Apr 2026 03:45:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cffd5a3d0a0b4b596a5935245e69b8553c644126d668e1ab82a3de7cbb7ba53`  
		Last Modified: Tue, 07 Apr 2026 03:45:57 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864a2ebee39b26f16e969e2a9defb0f736f828a125c1de3f72216cf9416a5835`  
		Last Modified: Tue, 07 Apr 2026 03:45:58 GMT  
		Size: 3.3 MB (3253565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9af88a986d39ecffd2656880c2ad1402ffcf48c67758accfcc59c6ac79d0883`  
		Last Modified: Tue, 07 Apr 2026 03:46:00 GMT  
		Size: 54.0 MB (54022649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3661938861118efdf6af8d330c7b1f174929e1c7bd3911492112ae7d64fe044`  
		Last Modified: Tue, 07 Apr 2026 03:45:58 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:8f3b281bf1bab52061dac1adf74d990f0edff6511f82774146fbd96b5c85bccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 KB (40326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e048d371f62bad08094c607f46b3d8d67954640861cd6a70d0797eec32d6865e`

```dockerfile
```

-	Layers:
	-	`sha256:00f86b027c79a8e34178500a3c45862e2c8ccc460bfe5c578a2fd18516587e97`  
		Last Modified: Tue, 07 Apr 2026 03:45:56 GMT  
		Size: 40.3 KB (40326 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; 386

```console
$ docker pull redmine@sha256:25f1ab7da2c6bb55afcb265868cf358cfcac1a14aabc61efe49704f6ec69f0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247523591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78995afd76a088b55a3796278000468cc8ae8c5f3af789403cb161b462bf506`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:11:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:16:31 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:16:31 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 02:16:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 02:16:31 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 02:16:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:16:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:16:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:16:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:16:31 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:16:31 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 02:57:04 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 07 Apr 2026 02:57:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:57:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 02:57:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:57:37 GMT
ENV RAILS_ENV=production
# Tue, 07 Apr 2026 02:57:37 GMT
WORKDIR /usr/src/redmine
# Tue, 07 Apr 2026 02:57:37 GMT
ENV HOME=/home/redmine
# Tue, 07 Apr 2026 02:57:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 07 Apr 2026 02:57:37 GMT
ENV REDMINE_VERSION=5.1.12
# Tue, 07 Apr 2026 02:57:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Tue, 07 Apr 2026 02:57:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Tue, 07 Apr 2026 02:57:37 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 07 Apr 2026 02:57:40 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 07 Apr 2026 02:58:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 02:58:21 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 07 Apr 2026 02:58:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:58:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:21 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 07 Apr 2026 02:58:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e032c0f3018bbbf4f40485135f2cdb496ef1c7813c589d6503b9798b4a9ef61`  
		Last Modified: Tue, 07 Apr 2026 02:14:18 GMT  
		Size: 3.5 MB (3512891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eea1bf52869be0bf678d06b5ef1ca88485cd974a173eba58f4be09f4a8d932a`  
		Last Modified: Tue, 07 Apr 2026 02:14:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17324062944fc9aa65bedba6ba0dc9ffcd23437f3b33c19adcb829274c4e2f25`  
		Last Modified: Tue, 07 Apr 2026 02:16:42 GMT  
		Size: 31.9 MB (31884179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065f640d820cc19feaef5f4a079b4e65e99e443f96cfb20daf61a6fdaff1b086`  
		Last Modified: Tue, 07 Apr 2026 02:16:39 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbfbc6611ef3dc7ce9d0f600edf41964eb2904a8918792889e80a66b90fc09`  
		Last Modified: Tue, 07 Apr 2026 02:58:37 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d371fd5595f4329a139b6c93144f3167122ab798d1b2e0df00d837717b341458`  
		Last Modified: Tue, 07 Apr 2026 02:58:41 GMT  
		Size: 124.8 MB (124832534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9c0680c6a9d6f5360af0441edbc28097db74ec184aa93817c256a380ee39b`  
		Last Modified: Tue, 07 Apr 2026 02:58:37 GMT  
		Size: 915.8 KB (915752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959c9644e975045bb70bba20f5547868ec5569c9d638b8ad65350cd90bba473a`  
		Last Modified: Tue, 07 Apr 2026 02:58:37 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd4e42bc4d994327520d2fde4228e6029a0c105c701cad88ef377af5bbeb38f`  
		Last Modified: Tue, 07 Apr 2026 02:58:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10cc2d8beb547495139d370fcef6fc25e6d75a41bc4e303d69e7aa0e286cd3a`  
		Last Modified: Tue, 07 Apr 2026 02:58:38 GMT  
		Size: 3.3 MB (3253551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ba8715a271d675a9940790c590908f41783dfc206e873aa85c4dbfdc5f112f`  
		Last Modified: Tue, 07 Apr 2026 02:58:41 GMT  
		Size: 53.9 MB (53898801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb43bc846d65a4b87bed4f8229cd529a0a472628bef715a4b093a458b351753e`  
		Last Modified: Tue, 07 Apr 2026 02:58:40 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:5a8362b7d3fd5ea06c5fabced9a92f97fc03cc22af5da17dd240f9c16a175a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1222ffedb2e6f77eca9aa886d1c1a1baf0ab5e4814a1f4e5768b611fa5bf661b`

```dockerfile
```

-	Layers:
	-	`sha256:05c13f91aa26a4d2ab92fc78e0188bf0f1923190979be390a44c76b4a18b8eff`  
		Last Modified: Tue, 07 Apr 2026 02:58:37 GMT  
		Size: 40.1 KB (40122 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; mips64le

```console
$ docker pull redmine@sha256:e951d1b1d5f641046043ef24891e95ada88c3286bf41030edb4bfc5b661e730d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253163933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a4eaf7d60594129e3057ec9109836acde350a1861d98b4a2bba1a7bfd70c75`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 13:49:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 13:49:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:54:31 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:54:31 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:54:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:54:31 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:54:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:54:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:54:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:54:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:54:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:54:33 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 20:13:50 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 20:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 20:17:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 20:17:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 20:17:38 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 20:17:39 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 20:17:39 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 20:17:40 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 20:17:40 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 20:17:40 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 20:17:40 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 20:17:40 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 20:17:45 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 20:28:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Mar 2026 20:28:18 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 20:28:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 20:28:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 20:28:20 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 20:28:20 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:036b690c37cf2dc49974818e200658ce29b93c4d917171332d28ada375e6f68b`  
		Last Modified: Mon, 16 Mar 2026 21:51:40 GMT  
		Size: 28.5 MB (28526147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5901c5b4b386661d4ce2f3c81157de4436091432a87e38987901d3ff0e6b4666`  
		Last Modified: Tue, 17 Mar 2026 14:21:15 GMT  
		Size: 2.9 MB (2901270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e17e07076a73b2c5b3a253b5365c50280aa824aef788c8c57ca584268f3e8`  
		Last Modified: Tue, 17 Mar 2026 14:21:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce269f098f7cbc734809e992b1848564e979a5207a3e0bc5a34526a629d2c70`  
		Last Modified: Fri, 27 Mar 2026 18:55:10 GMT  
		Size: 33.1 MB (33127381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533bb941a5dd81b9f8484cc6fa7ed4e4b81a67cfe05ed57d277733aee3bb27b3`  
		Last Modified: Fri, 27 Mar 2026 18:55:06 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50710aaeae0ef41fe4d169823a0b8ae0027093938018a4683786a72af7a3ba3`  
		Last Modified: Fri, 27 Mar 2026 20:30:32 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f750eb136835a880b51e31c7532eb83609010b3180ba5bd7b0599e1d625287`  
		Last Modified: Fri, 27 Mar 2026 20:30:51 GMT  
		Size: 118.5 MB (118453006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10634d08de44db1e05fce5bc063a9846ac0b8267be1e9506a2f6e8a7838bcfeb`  
		Last Modified: Fri, 27 Mar 2026 20:30:32 GMT  
		Size: 857.3 KB (857326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ba7616c443abc5ff5e8fda6efb49d5002707d56a5b0e2cc108ebfe012469ef`  
		Last Modified: Fri, 27 Mar 2026 20:30:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342fa6d1c27555473862707c471d42151081b440ee1de8c03634a9dbdabd3423`  
		Last Modified: Fri, 27 Mar 2026 20:30:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0969c643b73ec185825bf379eaaf1b98621b958ebbbddebef7fa9252dd575f25`  
		Last Modified: Fri, 27 Mar 2026 20:30:35 GMT  
		Size: 3.3 MB (3253554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc30559a38a44ecefab8643237b22fecb249353fe7adb7e14b76e7adfa9080b`  
		Last Modified: Fri, 27 Mar 2026 20:30:48 GMT  
		Size: 66.0 MB (66041131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a085a6225f3a21528f31a5279e6c2e2956e9e231beee4947c9cd06b34b0f74ff`  
		Last Modified: Fri, 27 Mar 2026 20:30:35 GMT  
		Size: 2.4 KB (2415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:be85e739f1ea60edb6ee0435f1e47d6fa60b023e7c2d3272068563705078e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d747448d2b711caeb0113ba943dda34e0d1a52b64684385a7e6c8ce46f2b7bb7`

```dockerfile
```

-	Layers:
	-	`sha256:b405b5939c29ea274d74336b4b92ef25c8e62dec888290c653945aa8095de66b`  
		Last Modified: Fri, 27 Mar 2026 20:30:32 GMT  
		Size: 40.2 KB (40231 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:d17c66a9a3fda620cfee75953247c62947e79063946e1de1819d09d29f5a119b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270378325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacfd199246da4d45e5b92533032b03590ab509bb185187e1092e492ef09d73f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Thu, 26 Mar 2026 18:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Mar 2026 18:31:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:37:54 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:37:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:37:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:37:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:37:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:37:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:37:55 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:39:26 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Fri, 27 Mar 2026 19:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Mar 2026 19:40:50 GMT
ENV GOSU_VERSION=1.19
# Fri, 27 Mar 2026 19:40:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 27 Mar 2026 19:40:50 GMT
ENV RAILS_ENV=production
# Fri, 27 Mar 2026 19:40:51 GMT
WORKDIR /usr/src/redmine
# Fri, 27 Mar 2026 19:40:51 GMT
ENV HOME=/home/redmine
# Fri, 27 Mar 2026 19:40:52 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Fri, 27 Mar 2026 19:40:52 GMT
ENV REDMINE_VERSION=5.1.12
# Fri, 27 Mar 2026 19:40:52 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Fri, 27 Mar 2026 19:40:52 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Fri, 27 Mar 2026 19:40:52 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Fri, 27 Mar 2026 19:40:55 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Fri, 27 Mar 2026 19:44:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Mar 2026 19:44:32 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 27 Mar 2026 19:44:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 27 Mar 2026 19:44:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Mar 2026 19:44:33 GMT
EXPOSE map[3000/tcp:{}]
# Fri, 27 Mar 2026 19:44:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6dd432af990aeed0dd4fd76d6d1fe507bfd33f78826731a1300e5c6f93423f`  
		Last Modified: Thu, 26 Mar 2026 18:35:43 GMT  
		Size: 3.7 MB (3710764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73847511305cedc00f17cc76877ca78c47c8d883a71664a7a3430ea3065709fa`  
		Last Modified: Thu, 26 Mar 2026 18:35:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec79745a4682555cfd3bbd00deced64e2558785bed015802f59239a475cc4c3`  
		Last Modified: Fri, 27 Mar 2026 18:38:14 GMT  
		Size: 33.6 MB (33627300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaf3905224c31d262cdb12adc36066b5968e6248de1c9d70415996c492692f0`  
		Last Modified: Fri, 27 Mar 2026 18:38:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536374234d930a73eca536f7194b62f1899a96c3d57fb9bece0e191e635cfa57`  
		Last Modified: Fri, 27 Mar 2026 19:45:08 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8b73f7e119c7480d302e9f8af0c6f70bb4b2be6dff87aae64929d285d23c1e`  
		Last Modified: Fri, 27 Mar 2026 19:45:13 GMT  
		Size: 129.9 MB (129931076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c46042c669a051a382bb83656455fe153ae86ffef1ac0c07d6f1f076361ee0a`  
		Last Modified: Fri, 27 Mar 2026 19:45:09 GMT  
		Size: 906.6 KB (906573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81aa3b68250673c4f39e4e36eb3357f7bfddc07d9ef98a47e9f864268798a867`  
		Last Modified: Fri, 27 Mar 2026 19:45:09 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9640d01e9408d06f3456b7230e5d965844a59c10c4d37c17e2cbf2ada5b51255`  
		Last Modified: Fri, 27 Mar 2026 19:45:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee04f1d1d0ed991eede72a70db8edc54a72b573855ac7a4573ea5fad508b37c`  
		Last Modified: Fri, 27 Mar 2026 19:45:10 GMT  
		Size: 3.3 MB (3253562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc35c376155e887ebdf02ffa181e61c54b8b8027e2caa2b82c4195ecff9979db`  
		Last Modified: Fri, 27 Mar 2026 19:45:13 GMT  
		Size: 66.9 MB (66866568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a43cc73757bb3efad015777b368c660284babe49db59a1158709f0a7e8a5ac9`  
		Last Modified: Fri, 27 Mar 2026 19:45:11 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:35997d6b7407e1b773cf3e17a7aa43ad9fd4b32af70c7845fae6d8f677b2a781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5369b8606aeb76017588b872c47570dec2060c026f9b03b0de194360112d200c`

```dockerfile
```

-	Layers:
	-	`sha256:829f0fdbb351036aa9684e8e043df79ee69b01e98203d2e143ff8cce30a25322`  
		Last Modified: Fri, 27 Mar 2026 19:45:08 GMT  
		Size: 40.2 KB (40205 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:5-bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:2c750e1b09ddc09e4792cdddc11bd26b794e6e669380f6ca735f9165e0aa2521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250668641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9712c34818eede6870d067c800bcdb1749576497d88455b49f03394b0a7525`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:36:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 04:42:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:42:32 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 04:42:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 04:42:32 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 04:42:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 04:42:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 04:42:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 04:42:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:42:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 04:42:33 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 06:10:51 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 07 Apr 2026 06:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 06:11:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 06:11:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 06:11:21 GMT
ENV RAILS_ENV=production
# Tue, 07 Apr 2026 06:11:21 GMT
WORKDIR /usr/src/redmine
# Tue, 07 Apr 2026 06:11:21 GMT
ENV HOME=/home/redmine
# Tue, 07 Apr 2026 06:11:21 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Tue, 07 Apr 2026 06:11:21 GMT
ENV REDMINE_VERSION=5.1.12
# Tue, 07 Apr 2026 06:11:21 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.1.12.tar.gz
# Tue, 07 Apr 2026 06:11:21 GMT
ENV REDMINE_DOWNLOAD_SHA256=686a9508a5df438728f03f4f930005349ed14571fadc7a365a1426a797fa0056
# Tue, 07 Apr 2026 06:11:21 GMT
ENV RAILS_LOG_TO_STDOUT=true
# Tue, 07 Apr 2026 06:11:22 GMT
RUN set -eux; 	wget -O redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	set -- 'config' 'db' 'log' 'public/plugin_assets' 'sqlite' 'tmp' 'tmp/pdf' 'tmp/pids'; 	mkdir -p "$@"; 	chown -R redmine:redmine ./; 	chmod -R ugo=rwX "$@"; 	find "$@" -type d -exec chmod 1777 '{}' + # buildkit
# Tue, 07 Apr 2026 06:13:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 06:13:19 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 07 Apr 2026 06:13:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 06:13:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 06:13:19 GMT
EXPOSE map[3000/tcp:{}]
# Tue, 07 Apr 2026 06:13:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c644c009cfb244ea86a1dd8f34039561e8c632c7ea9de18b7b84dda34374e973`  
		Last Modified: Tue, 07 Apr 2026 04:39:57 GMT  
		Size: 3.2 MB (3171201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e626e8e24686904fb217e122f4ad73975d089b96576c84e8dd4904151e7b`  
		Last Modified: Tue, 07 Apr 2026 04:39:57 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcc7a4af710710def677b25912742abb4fd1f37371b39f72f60d402321739d5`  
		Last Modified: Tue, 07 Apr 2026 04:42:46 GMT  
		Size: 32.9 MB (32875073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f6cee55d8c5d810d030694681a087d227079477d66536d54c121d6fc586091`  
		Last Modified: Tue, 07 Apr 2026 04:42:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b3dba9a7b352a7d71efc7bc302298fec670173722370e873ee23ca55ba460a`  
		Last Modified: Tue, 07 Apr 2026 06:13:42 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2147d0bc2c2b6b1ae82dd7444e1eb6a99b6ca7f3d67a4cd01b96b71cbd44c5dd`  
		Last Modified: Tue, 07 Apr 2026 06:13:44 GMT  
		Size: 118.6 MB (118628122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889ea384c9db39d5e58611072d2c79386eaf5bb2e31459c241a1c2d83f85d993`  
		Last Modified: Tue, 07 Apr 2026 06:13:42 GMT  
		Size: 919.3 KB (919268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1589bc8162fbe64d72a97bf823904411fe37625e298de072397bae0d06663c`  
		Last Modified: Tue, 07 Apr 2026 06:13:41 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a000bdc81e9e0afde664fff84725bd61de9f2fdfc3cffb68759b9226e8dd32d8`  
		Last Modified: Tue, 07 Apr 2026 06:13:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969a43a2fbdac889d0717869adbb511174a94f332298d05a4daff9f58998e91d`  
		Last Modified: Tue, 07 Apr 2026 06:13:43 GMT  
		Size: 3.3 MB (3253549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4c68df41bfd845df54edc685ac41a707a89a617da1c9b40acaecfad22f4279`  
		Last Modified: Tue, 07 Apr 2026 06:13:44 GMT  
		Size: 64.9 MB (64925677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbb199c748c5e406f020c34fff79a0b7124f9be5d76d122bdd884472719bd0d`  
		Last Modified: Tue, 07 Apr 2026 06:13:43 GMT  
		Size: 2.4 KB (2413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:5-bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:0592d869d5ade7403164b538e7f567150743f56468e5fa29c292ab1741746757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 KB (40159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef67fab18f440b9d0978162065e539509eb2eed0bdd4c42f5d18dfcffde3deb`

```dockerfile
```

-	Layers:
	-	`sha256:a81bba8bff6db06fd3bde19e9d93b0316b2b95c33e1632e2a004448a8ba9f051`  
		Last Modified: Tue, 07 Apr 2026 06:13:42 GMT  
		Size: 40.2 KB (40159 bytes)  
		MIME: application/vnd.in-toto+json
