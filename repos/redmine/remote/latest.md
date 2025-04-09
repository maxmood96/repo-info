## `redmine:latest`

```console
$ docker pull redmine@sha256:aea19db212df9076053d0412dc4b45d05461254088555045f9e7d74623941896
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

### `redmine:latest` - linux; amd64

```console
$ docker pull redmine@sha256:b30c4e74f74710f53f33c21f6846faaa152da2fd8d6d823363fde33dc97ae89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255011573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559cc1cfd5f6045c065299290338c014c09bd68d19bdbe4d72c16de6560522fa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 22:16:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
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
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84491629166a60586ab96171f3d8f7e8e5b2c892a87d50cf86ba73ce94121540`  
		Last Modified: Tue, 08 Apr 2025 01:51:46 GMT  
		Size: 3.5 MB (3499283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0c99c21f6865a554c62a53020e39b9dbdc5ae2908921bd491ee82c54966eb8`  
		Last Modified: Tue, 08 Apr 2025 01:51:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4053f2691250b2004b6c744b9418a34a51f7dead4a8cc8eea38bcd7ba20916`  
		Last Modified: Tue, 08 Apr 2025 01:51:47 GMT  
		Size: 37.7 MB (37712279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda45b35ae08cfc6c32ef357ee61c9c548366c769686fec6860f94bbc8f3bd50`  
		Last Modified: Tue, 08 Apr 2025 01:51:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4e6b9b933bf22ab6ebd3a23079f4b72f90b74212c67f0b4a829ebdf7863f4d`  
		Last Modified: Tue, 08 Apr 2025 02:23:40 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ad58a58da80f79b85055bcf618deae2541395473d8d738aba767aa9f54e10c`  
		Last Modified: Tue, 08 Apr 2025 02:23:43 GMT  
		Size: 123.1 MB (123121882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa21c5ff9dad3548f6a00e9b695162a5beedf534abf1183aa8a6644e6943cd7`  
		Last Modified: Tue, 08 Apr 2025 02:23:40 GMT  
		Size: 1.1 MB (1143525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2d08204fba5542a8f5d39ce6bc8dcad3d1d6c658286686a0e6c3ee8cf95fbc`  
		Last Modified: Tue, 08 Apr 2025 02:23:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ea0c246d20893e8b4b0ae1327e116c7497527a6db8406e45b003c216e4c4f0`  
		Last Modified: Tue, 08 Apr 2025 02:23:41 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf3cbb22135dd77287e0f8968600755a6ac1d885f6ee42ad1787fb9f418fc49`  
		Last Modified: Tue, 08 Apr 2025 02:23:42 GMT  
		Size: 4.1 MB (4056917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1010e63242bce42791581a36d95822550ac196196f9614f73c1f5c2db976202`  
		Last Modified: Tue, 08 Apr 2025 02:23:43 GMT  
		Size: 57.2 MB (57246420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af77e582966cb0f4ddd2acc71030c33bda29b8dd295df0114510de4f2cea86de`  
		Last Modified: Tue, 08 Apr 2025 02:23:42 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:0c26180544c9910bb2d735302d7f04da41884ca84003df6538a406844e12401d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68587991a33e754582a0520168d7073dd1d0645b40eb34ee5a98c62bd903ec29`

```dockerfile
```

-	Layers:
	-	`sha256:e06dbe8e144ffbeed6fea79c2ba01e87fcb67a7b1bfa48a9c4edaf72eb8dfea8`  
		Last Modified: Tue, 08 Apr 2025 02:23:40 GMT  
		Size: 41.3 KB (41252 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:91c46e480539c7c6809907f5afc3eab92646c21cafdf5280d38fbbf3eddaf164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239428346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169b5031ce317405b96678aa5e9bcd48867ace6de4526573ef9dde29f357cef6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 22:16:24 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
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
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da0305b2b23f80b1908c2ce6cdaee30c7f0a90503be88e1a607ebd5d8c65f1`  
		Last Modified: Tue, 08 Apr 2025 01:15:14 GMT  
		Size: 3.1 MB (3073460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e679718b4a0a268971ab010660cfd8581d60c05d2e1f1f4dc104ef75227825`  
		Last Modified: Tue, 08 Apr 2025 07:55:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f375cf4b53fbb47725637251c9ce6175d6c3c25a934a9d015cfc2ac75d8527`  
		Last Modified: Tue, 08 Apr 2025 07:58:11 GMT  
		Size: 34.3 MB (34251932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af2a647aff90572c4790fbe05a6a77c327c736696d724fc2e40c381a923b7c`  
		Last Modified: Tue, 08 Apr 2025 07:58:09 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b480cd75f89ecebc8e466fdd2032e2a25699ecb4ffb37f4f1a52c97ec1fe64`  
		Last Modified: Tue, 08 Apr 2025 10:32:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6173e71d15905243b6a3a2e3c06f8f8eca4ef7f2abe1e79a15452a7d4e150862`  
		Last Modified: Tue, 08 Apr 2025 10:32:15 GMT  
		Size: 116.8 MB (116761652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebeac76cbfde514ceaa82b1731fed8919884ce29c4e153d032b676f99bf88996`  
		Last Modified: Tue, 08 Apr 2025 10:32:12 GMT  
		Size: 1.1 MB (1120759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d24ac1f0d4026b661d99744e57cf3283656248572339b9e2445d089175ca06`  
		Last Modified: Tue, 08 Apr 2025 10:32:11 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9dbf64bf5f2ffef89f0bce8e767fdc5f34c4fd839bac5a628bd4f76cfe74ec`  
		Last Modified: Tue, 08 Apr 2025 10:32:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cd565e61ffbd90ce7607badc501108f71d16daa6f7b5f0f1e04dcf4160e65a`  
		Last Modified: Tue, 08 Apr 2025 10:32:13 GMT  
		Size: 4.1 MB (4056921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc94576188ffb6b5035a0c4721af72d2fc051ad4b306fdd46d001e6daa2af73`  
		Last Modified: Tue, 08 Apr 2025 10:32:15 GMT  
		Size: 54.4 MB (54401790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5689f9979ea3a94f01a934dfdd84221288888d729c5ef97f7e6eb30d799d72`  
		Last Modified: Tue, 08 Apr 2025 10:32:13 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:ab9d3a88cdfa12bac5104356bb651c9e7550e4217e80318c40b442849597da92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f2b0854dd3e5168f99fa82cc6e36718e48dd9f3446268aa35620c19feb4cd0`

```dockerfile
```

-	Layers:
	-	`sha256:a956f69ef084e6749f01410ff2e6a1a7bc3ef1d5d2706c0c382d493c3797ce3a`  
		Last Modified: Tue, 08 Apr 2025 10:32:11 GMT  
		Size: 41.4 KB (41425 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0a56ab16a063533bd7cb135befc57d33a643da24d5a8bf2b1cc280ee71ec8e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232532384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e1be9c983dab463d2370c6a51905eacb250bebf18e33d06bc0eda5c1f555c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 22:16:24 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
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
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b9af88c849258200dfe951d2ab46f39e95311b0593488e6b7736531419708`  
		Last Modified: Tue, 08 Apr 2025 01:16:30 GMT  
		Size: 2.9 MB (2907779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1edb05d5531be9965f495a717a0b763b159ea3dde1cf0369a8d4ddfe247767d`  
		Last Modified: Tue, 08 Apr 2025 16:23:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc9f24d0120921823e4d02f5f6ddc1b7b360f3f5b5d431aaf6a859f439d9b7c`  
		Last Modified: Tue, 08 Apr 2025 16:32:56 GMT  
		Size: 34.1 MB (34126649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03707ecced234d137f976b644506cbb6304d79d8019b9d13333919d62e8a712e`  
		Last Modified: Tue, 08 Apr 2025 16:32:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeb7a8460de846fd98513c56c65a2d30f9112a8018f146031d101aefeec4cef`  
		Last Modified: Tue, 08 Apr 2025 21:22:49 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5caece0ca9151a3322958e97025ebb7b219869c56a7367987cbcb2091810067`  
		Last Modified: Tue, 08 Apr 2025 21:22:53 GMT  
		Size: 112.1 MB (112140448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe0b527456a3253fb6f97f2fa8f865aad6a73fadd69f0bac785e116ca2e13c`  
		Last Modified: Tue, 08 Apr 2025 21:22:50 GMT  
		Size: 1.1 MB (1110098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29b8ccdc1621c6168e71fbe9edf7a4913b2c451e60fcbad8b1649d2637df118`  
		Last Modified: Tue, 08 Apr 2025 21:22:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0393946a9029830f2c7b992b01cc77391eabb16acb1e1106f6b70c08743daab`  
		Last Modified: Tue, 08 Apr 2025 21:22:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631b27cef56c96b3acb4f74ac353ba48dbe697144d9b7da42f36011dc34d9fa`  
		Last Modified: Tue, 08 Apr 2025 21:22:51 GMT  
		Size: 4.1 MB (4056913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251df160f412a5de1173810525168cb2822027c7be6b101ca0bc9f7d9476800`  
		Last Modified: Tue, 08 Apr 2025 21:22:52 GMT  
		Size: 54.2 MB (54248622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3190ddd940c18185c7895a7150c7457ddb0c855cda6c0fc5dec0433472f86574`  
		Last Modified: Tue, 08 Apr 2025 21:22:51 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:700dd8a22aff749706eb84a301b1a664a4c208a9c62e4d3cb6676a10f54e5ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d709b899284ec5c1ea9e77100e57d0e3e9fff0f9f537e2e3308b60d2d2c372c`

```dockerfile
```

-	Layers:
	-	`sha256:692ba7af96220c08e08de00eb6983fc9e3e9a32448bd10f019b4713abaf35473`  
		Last Modified: Tue, 08 Apr 2025 21:22:49 GMT  
		Size: 41.4 KB (41425 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:d0d6f27f176c087e299656b510baf78de80c1d5262c97734aac082845628b142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251242781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb745f99e38bbae6f362eee889f7087b9a80826069938ce59de8570db163e2cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 22:16:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
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
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa2de5f47784eeac44d104145d3ce6fb0c0af731d1f98c56441ce3ffeed401d`  
		Last Modified: Tue, 08 Apr 2025 01:17:12 GMT  
		Size: 3.3 MB (3322887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fae63766ccb69dffa8068bda9cb7df860809ee1cdd67996784e28875b1ec0c`  
		Last Modified: Tue, 08 Apr 2025 10:33:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfe51dc869df5aad796c3ae06fdba321f557b2c6f07b8b8b3e98e9ee95f418`  
		Last Modified: Tue, 08 Apr 2025 10:39:06 GMT  
		Size: 37.7 MB (37689466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc22bbf78422e9db07a2cd7f8daf44e6c7690e64987a9e8d2494ab04958169`  
		Last Modified: Tue, 08 Apr 2025 10:39:05 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a320b063604e60e94d5e2bb889c9818fe731b742c4de7c007df1e1207c5f0f77`  
		Last Modified: Tue, 08 Apr 2025 15:46:25 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ffbd3c0537ee938903206c92f55a85da748f67d8eafe7bd1dee248ef27dc49`  
		Last Modified: Tue, 08 Apr 2025 15:46:28 GMT  
		Size: 120.4 MB (120407457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bee94135342a5901aae85d20f10504a03aeab01ab84df498768d9d1c045914f`  
		Last Modified: Tue, 08 Apr 2025 15:46:25 GMT  
		Size: 1.1 MB (1076188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903377b03eeeaee2e57c4e48bf370b4b1b09a8a710388a9ee9cc14aadb03e405`  
		Last Modified: Tue, 08 Apr 2025 15:46:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1ec62dc414b9396f60ac274f43a868a21be5f69dcedf4295cd8c48ddcad6bc`  
		Last Modified: Tue, 08 Apr 2025 15:46:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccfa295b25e1ba38393ff69149d98e3e1172da5a257c2d161d3251ad1f656d9`  
		Last Modified: Tue, 08 Apr 2025 15:46:26 GMT  
		Size: 4.1 MB (4056917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d981403815e949448d1a336818eb1dc33c66ee02f6edae4ca126de0cf91d8d82`  
		Last Modified: Tue, 08 Apr 2025 15:46:28 GMT  
		Size: 56.6 MB (56619537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9407d125a235b3aacea4660b2ffeec7796738d6f811ab27afc18b1e1ca831c24`  
		Last Modified: Tue, 08 Apr 2025 15:46:27 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:b93fc5b82819b873f338a5b577ce095f8d7ff582eb86ac47bc9f6eeb87f1eda6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 KB (41479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1eb04d3a4938c04b09a5eb1ab6fc64f8266b38c7eccf3ba6ec5615ac38da0e`

```dockerfile
```

-	Layers:
	-	`sha256:d6b08564de423026161d113cbc99fa1ae8ed58f8359448b91330af2cd858446c`  
		Last Modified: Tue, 08 Apr 2025 15:46:24 GMT  
		Size: 41.5 KB (41479 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:8f4e381b38f650dab31b999ba756e4ef05a2b3f3bfd38fc1cb2dac215ed9aa96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253475093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b28357468b3a123f5c87963d29ccede8d57ac595a3fa8b231cf06fd72db4709`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 22:16:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
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
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1466e9c96bbf9867a623db20b35b9cbd63a3951fd518d3c8813612d19a37f`  
		Last Modified: Tue, 08 Apr 2025 01:31:02 GMT  
		Size: 3.5 MB (3503446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd642ce7d66cf94ae11a255f25b885eaebc2a09c69a67e8a5798cb0a50b2ae0`  
		Last Modified: Tue, 08 Apr 2025 01:31:02 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7d681c74da1dcb9a108d3487b4de0d87d370127b6f437e66d14306c710e331`  
		Last Modified: Tue, 08 Apr 2025 01:31:04 GMT  
		Size: 34.1 MB (34057826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f30f09804fecdbd3b8947d41c2022a4fcc61c69cb9a0fe97e4ca6c98e087868`  
		Last Modified: Tue, 08 Apr 2025 01:31:02 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e472f155fa1322e5b7f98821394215c00807b4e40b1d94e00d7dc4564fa855`  
		Last Modified: Tue, 08 Apr 2025 02:23:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179a550f30ae81915ac1071544d3149df73f795f25d206a8b8e4af2bc80cb6cb`  
		Last Modified: Tue, 08 Apr 2025 02:23:25 GMT  
		Size: 125.0 MB (124991100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111391fd5055a49ae7906c6ae8f6f62295d685b9f9d0b790efaaa88595872c70`  
		Last Modified: Tue, 08 Apr 2025 02:23:22 GMT  
		Size: 1.1 MB (1119110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b49c35459f6c79992e82ed1381d19d09bc9496804eb722b5fdb9052ef32611b`  
		Last Modified: Tue, 08 Apr 2025 02:23:22 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8c9a83568ea055cf74bf90d62c4f377a28d3c95a36df87f07e917571601f3`  
		Last Modified: Tue, 08 Apr 2025 02:23:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bb782e64e7cb9cb6ef0ddf8df2ab5f5015b3c83f4817ae17dda473afaa97d5`  
		Last Modified: Tue, 08 Apr 2025 02:23:23 GMT  
		Size: 4.1 MB (4056917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cc360aabeabc13ab3be7d1ba51161bbd86835f1f97eeda845808676aa66006`  
		Last Modified: Tue, 08 Apr 2025 02:23:25 GMT  
		Size: 56.5 MB (56531960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c713bc1c7f667b5a89bc831760f79699d5b8d5aa66c1afcafa414d9e99d41`  
		Last Modified: Tue, 08 Apr 2025 02:23:24 GMT  
		Size: 2.3 KB (2303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:f5d6b137fcc4142c23f6e35842ca412d46068e39dc90adebb116334a1bfea1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 KB (41189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc8c04c37e335caf1419c686c5317a84a800bac3f1c8beeb87e63721c1bbe46`

```dockerfile
```

-	Layers:
	-	`sha256:e3019f06bd2244efb491b1c07b667d468a41107d102c9e0c1165018848ec8b35`  
		Last Modified: Tue, 08 Apr 2025 02:23:22 GMT  
		Size: 41.2 KB (41189 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; mips64le

```console
$ docker pull redmine@sha256:b13376f39b3b78632a524ef56ea161961a0137da35dbe891c177d36bd078178d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259241832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac913cca9fcd42552f7ae4c8799fb8f467ed9af8e05784cf6adf1bd9e4e0ccc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 22:16:24 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
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
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6949d2412d1813d925526134f33bbbd4b60e21f566ca57a9d89acc7ac2b8b0d6`  
		Last Modified: Tue, 08 Apr 2025 01:29:32 GMT  
		Size: 2.9 MB (2895366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8077a442f0164a66c43732a39701fd27fd0c4d6bf24dabe3ada98b5c8a06bb`  
		Last Modified: Tue, 08 Apr 2025 21:54:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda90a90db4482604573fbb46f109ec939afef44f49b250731f7497eb6d8351`  
		Last Modified: Tue, 08 Apr 2025 22:10:31 GMT  
		Size: 35.4 MB (35424364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf0495edee7954ab00a35d2f3bb3ae81040f1f88a8b036140fd7564ddc3fdf1`  
		Last Modified: Tue, 08 Apr 2025 22:10:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0c06045f03abb1c4a651ce70c9c163af1a31664382725dd027f0f8d96fb029`  
		Last Modified: Wed, 09 Apr 2025 08:39:48 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f3d3919b29cf4b3714550f6d4f54a8eea7f3dd3eb12c85d284678adc9c87b2`  
		Last Modified: Wed, 09 Apr 2025 08:40:00 GMT  
		Size: 118.6 MB (118606688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc619d712e6fec716f4309bee8491eaa00a4bd879099686a183789fd786119ad`  
		Last Modified: Wed, 09 Apr 2025 08:39:49 GMT  
		Size: 1.0 MB (1030996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930ffafc5f1095278a7e6de3f7380fcae9684d8abd993ab990e39aedcba7a766`  
		Last Modified: Wed, 09 Apr 2025 08:39:49 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5e1d4ac2233ad1d6b52a59bfe54c6bc8662b6e6ca1bfb0f0aae270414a00d5`  
		Last Modified: Wed, 09 Apr 2025 08:39:49 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9b6b7b73ed0f5fa42a93bfbcc99a557e642fa82a1a2eeee8927db93407fd35`  
		Last Modified: Wed, 09 Apr 2025 08:39:50 GMT  
		Size: 4.1 MB (4056918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be67b2b2e0e59ceacd7707e8c1fa150c53ffd518c085688a6e1e2e89308ea6e9`  
		Last Modified: Wed, 09 Apr 2025 08:39:57 GMT  
		Size: 68.7 MB (68709535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd04b24a16614f8f53751c31b42a40fce602bb741ad06ce62b75ae533651079`  
		Last Modified: Wed, 09 Apr 2025 08:39:50 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:c199bd94d2833db9030adce5c06be98912dd44cc662eafadc38223dfc872e19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 KB (41368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e77eeaea2cb0d76797c7c836d9038494349a8bad8a97f99cf7ce981edb9bd27`

```dockerfile
```

-	Layers:
	-	`sha256:39d83f8ae5868ccbc2b03234c66020bb7d80dea17cc04d1248050b8871c6982e`  
		Last Modified: Wed, 09 Apr 2025 08:39:48 GMT  
		Size: 41.4 KB (41368 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:aa2fbeedc23894e3e02db996fb4680e43d6fc627894eaf839881b1e1df185f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276365093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab40b20b89516d77d2874db6ffcdf005bddd0076b56ec832b6bb430ee37106d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 22:16:24 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
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
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42468877a74e57c50c11233c777cffdbaa83d62017691c314be00ed02fbee779`  
		Last Modified: Tue, 08 Apr 2025 01:19:17 GMT  
		Size: 3.7 MB (3702920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5065fa57efae8ad889eb0ec7942e994d0544c22f59c33ef5cda5fc47622545`  
		Last Modified: Tue, 08 Apr 2025 07:19:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a45c66aa8b574ff77deb9ffd83981bc0a1f84fb79ce38a695025c30e1771a1`  
		Last Modified: Tue, 08 Apr 2025 07:23:45 GMT  
		Size: 35.8 MB (35799842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76babbb792ecaa474b624a1d2685cd5f3529fea83fdb79c49ff749ca599d3d8b`  
		Last Modified: Tue, 08 Apr 2025 07:23:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cd64a9e5e042dd5265c6895abd8fee079fde1daf7df44bf2cab835920359b7`  
		Last Modified: Tue, 08 Apr 2025 16:03:53 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ef0742695ed2c5119232ef174fb89487002ee143950e18caf2a0afe4ab7296`  
		Last Modified: Tue, 08 Apr 2025 16:03:57 GMT  
		Size: 130.1 MB (130108237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041468b329ef58dfe0cd140ca579e747980347e999adbac16fd38bdf914e4dde`  
		Last Modified: Tue, 08 Apr 2025 16:03:53 GMT  
		Size: 1.1 MB (1066303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f742461513ab3ce8854934759381c8fe1d073ac8d366e227b62fd43fa2457ce0`  
		Last Modified: Tue, 08 Apr 2025 16:03:53 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaa6419db04aefdc1caa2cc787d79a5488620202de18f125cbb978c700d2b0b`  
		Last Modified: Tue, 08 Apr 2025 16:03:55 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3d2b45e978ea780572a967dc265478ae0b08e131f7e73fea303a32509847d8`  
		Last Modified: Tue, 08 Apr 2025 16:03:55 GMT  
		Size: 4.1 MB (4056919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf5ac28244919d584a15389b97c0a18e59dd4e9c6bc945f7e564bed5510b4fa`  
		Last Modified: Tue, 08 Apr 2025 16:03:57 GMT  
		Size: 69.6 MB (69558633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c66a18dcb7cbc1cd925ba0386647fe7701bcc6f458a329f6f5b116fad99082`  
		Last Modified: Tue, 08 Apr 2025 16:03:56 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:a348fae861ef0aa5bc8837f566d2054b36a3a5b15e74a2e118d806b68311c1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3565d80148e7786ec420c0636456e3b326df064dc4c82c775b20890d6e57f2b5`

```dockerfile
```

-	Layers:
	-	`sha256:d517f9b8e4b361d829896545efeeddb69eae5a293c2ca5ea51ed494ab34c5e0c`  
		Last Modified: Tue, 08 Apr 2025 16:03:53 GMT  
		Size: 41.3 KB (41330 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:d4e57ccf7120e0cc374e9651a7e5617c7fc89e51c16e8673e865c727e0e02b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256638409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5581e792dabf784fdac753450621643c93bf3a05508d1bb6e744ed64d687928`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Fri, 14 Feb 2025 22:16:24 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_VERSION=3.3.7
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.7.tar.xz
# Fri, 14 Feb 2025 22:16:24 GMT
ENV RUBY_DOWNLOAD_SHA256=5dbcbc605e0ed4b09c52703241577eb7edc3a2dc747e184c72b5285719b6ad72
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 14 Feb 2025 22:16:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 22:16:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 14 Feb 2025 22:16:24 GMT
CMD ["irb"]
# Tue, 11 Mar 2025 02:53:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		ca-certificates 		ghostscript 		git 		gsfonts 		imagemagick 		mercurial 		openssh-client 		subversion 		tini 		wget 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 02:53:30 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Mar 2025 02:53:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
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
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		pkgconf 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle config build.nokogiri --use-system-libraries; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5390cf33ec28c798a2df11ec64efd7f989ab7db3d4d33d56e88209a2178b13`  
		Last Modified: Tue, 08 Apr 2025 01:15:45 GMT  
		Size: 3.2 MB (3163368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee68bcbce1342748889cb05bd536d8c1873092b88e16957dce203a7d188202c6`  
		Last Modified: Tue, 08 Apr 2025 06:12:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2c16010d95c603ae72a36bcde9eb569c90dbd558caf4e9f4605ec5c4809c2d`  
		Last Modified: Tue, 08 Apr 2025 06:15:22 GMT  
		Size: 35.0 MB (35042365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e32e05f23304748fa6faf235e14289bff38f534cfc8f82e4ceccc8d45f2919`  
		Last Modified: Tue, 08 Apr 2025 06:15:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada86fa330ae25fb2803f18f23dc8cef727c03a032e7e648cf41fa793bcff9f3`  
		Last Modified: Tue, 08 Apr 2025 10:25:22 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7757d71a9e26ea3efa4fc11c235a54626e672fa8d8efcd2f7a953023925399e`  
		Last Modified: Tue, 08 Apr 2025 10:25:25 GMT  
		Size: 118.8 MB (118779533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de17617a20c452f3689985e752a23cfc6f82964efe452271a6101b891652cf7`  
		Last Modified: Tue, 08 Apr 2025 10:25:23 GMT  
		Size: 1.1 MB (1108758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfd3e6640788457546a2b26cfe6c1610d3df023b796bf06880f92c2431d02b`  
		Last Modified: Tue, 08 Apr 2025 10:25:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ab161090387156b028ef5604f12a27ef10be1e83b40eb9aa4d25bde1adca47`  
		Last Modified: Tue, 08 Apr 2025 10:25:23 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26e1c5c1a1fe8a17529464ee87d9a64dc403cbbcdba80d5dd80cfe147e898d8`  
		Last Modified: Tue, 08 Apr 2025 10:25:24 GMT  
		Size: 4.1 MB (4056920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa11f7ffd182f6bcc5a0e1422abcb74e2f55d7406a62fd46dcee8293989f1fe`  
		Last Modified: Tue, 08 Apr 2025 10:25:26 GMT  
		Size: 67.6 MB (67598850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089a83ffc26e626cf1601805f2d115bddd6dceecb4ad06407e0d9ca844e46924`  
		Last Modified: Tue, 08 Apr 2025 10:25:24 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:latest` - unknown; unknown

```console
$ docker pull redmine@sha256:b37bf521a2c3528dd941df4ef2482977c4c6a8162f995bf6b1d5c52736f709e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da918cd3a3083104ba074afc6cebd46b0e5fdb04b1b7eadf9676a35d92bb322e`

```dockerfile
```

-	Layers:
	-	`sha256:5e2c42b0bac811c60ee99ecc4f941e354db268d7de479f2cc21907b7c58c9ede`  
		Last Modified: Tue, 08 Apr 2025 10:25:22 GMT  
		Size: 41.3 KB (41252 bytes)  
		MIME: application/vnd.in-toto+json
