## `redmine:5-bullseye`

```console
$ docker pull redmine@sha256:f502c6e35082eec2c51f297877aae121741e941843c6b801cee81f83ae86005a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:5-bullseye` - linux; amd64

```console
$ docker pull redmine@sha256:543d88dddd4677fa4efeb35efc8d60e9b4f671424e89768a13b3cf389aaab1c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240459155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e1bbde27d1808fca10a4ff2bd73b3bdf116b6dd64bf0dcf7a225d99ca4ca35`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 19:08:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 03 May 2023 19:08:49 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 19:19:16 GMT
ENV RUBY_MAJOR=3.1
# Wed, 03 May 2023 19:19:17 GMT
ENV RUBY_VERSION=3.1.4
# Wed, 03 May 2023 19:19:17 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 03 May 2023 19:21:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 03 May 2023 19:21:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 03 May 2023 19:21:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 03 May 2023 19:21:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 19:21:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 03 May 2023 19:21:35 GMT
CMD ["irb"]
# Thu, 04 May 2023 08:52:23 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 04 May 2023 08:52:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 08:52:59 GMT
ENV RAILS_ENV=production
# Thu, 04 May 2023 08:52:59 GMT
WORKDIR /usr/src/redmine
# Thu, 04 May 2023 08:52:59 GMT
ENV HOME=/home/redmine
# Thu, 04 May 2023 08:53:00 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 04 May 2023 08:53:00 GMT
ENV REDMINE_VERSION=5.0.5
# Thu, 04 May 2023 08:53:00 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Thu, 04 May 2023 08:53:00 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Thu, 04 May 2023 08:53:03 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 04 May 2023 08:53:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 May 2023 08:53:34 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 04 May 2023 08:53:34 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 04 May 2023 08:53:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 04 May 2023 08:53:34 GMT
EXPOSE 3000
# Thu, 04 May 2023 08:53:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ffa30101754210c7fbca23d2147904756a96e7f8d9754f6db4bc31580083c`  
		Last Modified: Wed, 03 May 2023 19:42:49 GMT  
		Size: 10.0 MB (10023164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaf5502212fbe68d4ac640762fb12d59af0868a4cd48fb88fd3e7612d79c165`  
		Last Modified: Wed, 03 May 2023 19:42:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5989aaa467739f805f59f49c0a3760fb8ce5823811aafed2047cd795702e85b`  
		Last Modified: Wed, 03 May 2023 19:44:01 GMT  
		Size: 32.6 MB (32626126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9217ac23b4ffb1f4c4f88d8e6ecf75f075baddf3d460235576adacd563695f`  
		Last Modified: Wed, 03 May 2023 19:43:59 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfff5d2555333adcf30d9ac46f9b53f66068d38493b07e0f22c96ae1454f91cd`  
		Last Modified: Thu, 04 May 2023 08:55:47 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d891fae24e2268b1d51f5f6f98541fb2ad0de0fa1500d1119e50095e5e6e86d`  
		Last Modified: Thu, 04 May 2023 08:56:01 GMT  
		Size: 102.0 MB (101950855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5088d0bb4d616b66757ce59f26a16d77ef5b3fd5cfd00c6cfb60b400ffdb7a`  
		Last Modified: Thu, 04 May 2023 08:55:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90fea341e9bed0799d84c9c55f33825c2dc1a70a0949af70e774290a8a37729`  
		Last Modified: Thu, 04 May 2023 08:55:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ad114b837f98f3ba0a20553d16fc74a59d17c394c2a2f9a812742d04c09b28`  
		Last Modified: Thu, 04 May 2023 08:55:45 GMT  
		Size: 3.1 MB (3144728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329f47a6fb15a7eb6ddd2e9bb4c98eb4e9f1e6bd5ea2cee018d044183fbd8bf7`  
		Last Modified: Thu, 04 May 2023 08:55:51 GMT  
		Size: 61.3 MB (61306310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634b5bfed32de3a1afc002603da871c0444b29cbbdb75d977c9e7462d48234f4`  
		Last Modified: Thu, 04 May 2023 08:55:45 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; arm variant v5

```console
$ docker pull redmine@sha256:50dbef0bf3c09bde14f091ae8a2cab4bf5b9addaf576867c027b28d584e82db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239272609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f32c31da1c378f99ef5aae011fa3ee5a080368a187ed64af1ad96583dcf8f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 May 2023 00:48:41 GMT
ADD file:868f634f5ddb80ed9e9c719ccaf5d564d96fe819f0b000ecc734311baf5da99b in / 
# Tue, 23 May 2023 00:48:42 GMT
CMD ["bash"]
# Tue, 23 May 2023 07:43:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:43:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 23 May 2023 07:43:58 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 07:53:32 GMT
ENV RUBY_MAJOR=3.1
# Tue, 23 May 2023 07:53:32 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 23 May 2023 07:53:32 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 23 May 2023 07:56:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 23 May 2023 07:56:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 May 2023 07:56:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 May 2023 07:56:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:56:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Tue, 23 May 2023 07:56:01 GMT
CMD ["irb"]
# Tue, 23 May 2023 14:10:23 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 23 May 2023 14:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 14:11:14 GMT
ENV RAILS_ENV=production
# Tue, 23 May 2023 14:11:15 GMT
WORKDIR /usr/src/redmine
# Tue, 23 May 2023 14:11:15 GMT
ENV HOME=/home/redmine
# Tue, 23 May 2023 14:11:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 23 May 2023 14:11:15 GMT
ENV REDMINE_VERSION=5.0.5
# Tue, 23 May 2023 14:11:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Tue, 23 May 2023 14:11:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Tue, 23 May 2023 14:11:19 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 23 May 2023 14:12:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 14:13:00 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 May 2023 14:13:00 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 23 May 2023 14:13:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 May 2023 14:13:00 GMT
EXPOSE 3000
# Tue, 23 May 2023 14:13:00 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:812967ccba449e7a96044b2d48ffc62816b22eb17641844c4dfffbe3b3ec6f21`  
		Last Modified: Tue, 23 May 2023 00:51:19 GMT  
		Size: 28.9 MB (28903411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be04097d1ded9335b3db9447099711ba6b7e06110590c1dce452f7bfbde88a6b`  
		Last Modified: Tue, 23 May 2023 08:01:48 GMT  
		Size: 8.6 MB (8634451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22a934b77fc215fc18ccde8e1d1820798abb4b25ed01191b3bb3c4815f31168`  
		Last Modified: Tue, 23 May 2023 08:01:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e558fe7b0b7f0c483952f729a9b4538079f921461ee708c55b103cf7712078c2`  
		Last Modified: Tue, 23 May 2023 08:03:08 GMT  
		Size: 31.2 MB (31165902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09bd2353f05cb293e4149ffe41c6f17410af979ed625452c1d65ea76df4a388`  
		Last Modified: Tue, 23 May 2023 08:03:05 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1681b6f77f5349baf9df52875f55ffa9f56ce152cfb790aef20b7fac64702291`  
		Last Modified: Tue, 23 May 2023 14:13:25 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33ce5197ddeea0a5db93b1952ea946e256221827558584f8a1508f339fc42b4`  
		Last Modified: Tue, 23 May 2023 14:13:41 GMT  
		Size: 96.9 MB (96937620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99a7183b87b4479908484a64728c038e680d23bc2d9b587f2af99be0589c084`  
		Last Modified: Tue, 23 May 2023 14:13:23 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9379413a0f9982ab8bbd00003c886dc4762ba5d5c2713fd0d91acd330ac4349`  
		Last Modified: Tue, 23 May 2023 14:13:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded41c8d3d717a77525f1dca14700ae1bc39cf151f507fc276b9adf2ae4a79fa`  
		Last Modified: Tue, 23 May 2023 14:13:24 GMT  
		Size: 3.1 MB (3144727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ba0240e2cc3cc2985b991b82cc02755b3e4f22f3abc632436a128bcfec530b`  
		Last Modified: Tue, 23 May 2023 14:13:40 GMT  
		Size: 70.5 MB (70482037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5ed9b88903c3b22e128eb00e175a1d2e1b119579bf3d2176afd3e62a17e8c8`  
		Last Modified: Tue, 23 May 2023 14:13:23 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; arm variant v7

```console
$ docker pull redmine@sha256:ff951caa094f4c7d102ba22cbc70648ada7486ce91a6669c15d2330cc39c7b82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232179494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c493b999326e01bf0d7ee09eb80911e4f3ca2916ad19fa8ceb7189d6ad5cbf26`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 May 2023 00:57:55 GMT
ADD file:dbb95e676c7a9806b1883ebcf4259345159caf22ff7194ba7556ea0b1f78099a in / 
# Tue, 23 May 2023 00:57:56 GMT
CMD ["bash"]
# Tue, 23 May 2023 05:30:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 05:30:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 23 May 2023 05:30:28 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 05:40:42 GMT
ENV RUBY_MAJOR=3.1
# Tue, 23 May 2023 05:40:42 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 23 May 2023 05:40:42 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 23 May 2023 05:42:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 23 May 2023 05:42:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 May 2023 05:42:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 May 2023 05:42:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 05:42:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Tue, 23 May 2023 05:42:46 GMT
CMD ["irb"]
# Tue, 23 May 2023 11:17:53 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 23 May 2023 11:18:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 11:18:36 GMT
ENV RAILS_ENV=production
# Tue, 23 May 2023 11:18:36 GMT
WORKDIR /usr/src/redmine
# Tue, 23 May 2023 11:18:36 GMT
ENV HOME=/home/redmine
# Tue, 23 May 2023 11:18:37 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 23 May 2023 11:18:37 GMT
ENV REDMINE_VERSION=5.0.5
# Tue, 23 May 2023 11:18:37 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Tue, 23 May 2023 11:18:37 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Tue, 23 May 2023 11:18:41 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 23 May 2023 11:20:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 11:20:17 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 May 2023 11:20:17 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 23 May 2023 11:20:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 May 2023 11:20:17 GMT
EXPOSE 3000
# Tue, 23 May 2023 11:20:17 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a27027e97f260d9b7aac9bae941b44639374700dc4c32cc2e378b189a4ffda88`  
		Last Modified: Tue, 23 May 2023 01:01:46 GMT  
		Size: 26.6 MB (26564635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb6a09bcc5c0984ecb3a04b714caca1098f621d70de5fb59d22fc016d46ffae`  
		Last Modified: Tue, 23 May 2023 05:50:53 GMT  
		Size: 8.1 MB (8143926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2368c379d00172553a3637b0c56b1cdb714a97b92bb40f910b023e9ac82c3`  
		Last Modified: Tue, 23 May 2023 05:50:51 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78962edc36f5ff06f5957f41aec3bc1dafd3618cb6e13c99ec2b9d672ce2d46`  
		Last Modified: Tue, 23 May 2023 05:52:01 GMT  
		Size: 31.0 MB (31035229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5cd2c80a56fed84af20ba9be79ed5dac3e9a1b6e1836258be0c336c9a5d6c2`  
		Last Modified: Tue, 23 May 2023 05:51:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea862d8a626da36c10966cc92c3d1d1b665f35912597084ce0f29e07919fd460`  
		Last Modified: Tue, 23 May 2023 11:20:58 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b31e9f24d6835f56d24faf30d2975bcdc170bd14c94a42784db34d02de7bfe`  
		Last Modified: Tue, 23 May 2023 11:21:19 GMT  
		Size: 93.1 MB (93088723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b031e982ee3121799cb93e955dfa65d76bb816ce5f5d9a517dfeafd9df32be7`  
		Last Modified: Tue, 23 May 2023 11:20:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ea408fee9d5b75836e0b562f8b6a05a49f149cb73a4c88c9a912ca2c58b643`  
		Last Modified: Tue, 23 May 2023 11:20:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9743a7c9ddd3977b534a9ab701def5dfc9efe7c5a1a3cfe1e6af73bb05371d2a`  
		Last Modified: Tue, 23 May 2023 11:20:57 GMT  
		Size: 3.1 MB (3144717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48f99217e4e14ab2c16d3528eb9ea68f3a5024b6a7e6a8ff3cd7f67df66624b`  
		Last Modified: Tue, 23 May 2023 11:21:09 GMT  
		Size: 70.2 MB (70197808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69488c04c63d72af28feb05643fd9eb0e45efd0cfb755976de81a278cb7021f3`  
		Last Modified: Tue, 23 May 2023 11:20:56 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b7b00a2feef45f9ec427ec6a618d27afaf46536327354b02e38889c9dce020fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234944341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a434b7d9895ad17cc2182b8851f93889968bccf14bc2dbdac84f2cc285fd9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 06:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 06:17:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 23 May 2023 06:17:13 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 06:33:27 GMT
ENV RUBY_MAJOR=3.1
# Tue, 23 May 2023 06:33:27 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 23 May 2023 06:33:27 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 23 May 2023 06:35:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 23 May 2023 06:35:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 May 2023 06:35:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 May 2023 06:35:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 06:35:17 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Tue, 23 May 2023 06:35:17 GMT
CMD ["irb"]
# Tue, 23 May 2023 19:41:54 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 23 May 2023 19:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 19:42:32 GMT
ENV RAILS_ENV=production
# Tue, 23 May 2023 19:42:32 GMT
WORKDIR /usr/src/redmine
# Tue, 23 May 2023 19:42:33 GMT
ENV HOME=/home/redmine
# Tue, 23 May 2023 19:42:33 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 23 May 2023 19:42:33 GMT
ENV REDMINE_VERSION=5.0.5
# Tue, 23 May 2023 19:42:33 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Tue, 23 May 2023 19:42:33 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Tue, 23 May 2023 19:42:36 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 23 May 2023 19:43:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 19:43:03 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 May 2023 19:43:03 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 23 May 2023 19:43:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 May 2023 19:43:03 GMT
EXPOSE 3000
# Tue, 23 May 2023 19:43:03 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c44207aeb95c5c97b69601e7ecf6205b0018dc481f58c8d1c35c7e9f1ce3d6e`  
		Last Modified: Tue, 23 May 2023 06:46:42 GMT  
		Size: 9.2 MB (9243477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68b42fcab4b6e0ed16656636285da203ba16863eff8f005def15c873988b921`  
		Last Modified: Tue, 23 May 2023 06:46:41 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f6677e34939ef3d61f952f03eb1fd89bde1a1894e28bddeaa6bab4abcd7015`  
		Last Modified: Tue, 23 May 2023 06:48:53 GMT  
		Size: 32.0 MB (31987287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d18bebe0e6b2814ed86e3b712f39ca4b5fc012cb4753e109949603be9cfe78b`  
		Last Modified: Tue, 23 May 2023 06:48:51 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e74d9b84c95140f4673683c35724c0c5d551b44647ac3b82e5bfc7c1088a79`  
		Last Modified: Tue, 23 May 2023 19:43:33 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65881028873a1db810b5c3026a9752aa3c0c4ae86d9898a6e47c96e1d562368e`  
		Last Modified: Tue, 23 May 2023 19:43:44 GMT  
		Size: 99.7 MB (99728975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e78b2ca102b4be3aa996bcf652e4e3c80eeafac8bc441a4d867735686bea43`  
		Last Modified: Tue, 23 May 2023 19:43:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999969cc00673f986f3de461058f2540abf696d132398ada10b72def0a026440`  
		Last Modified: Tue, 23 May 2023 19:43:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c2f44a5ef0240e897d383d3f62d4f32d43bc75c2618dd5d231556e70f39cf5`  
		Last Modified: Tue, 23 May 2023 19:43:32 GMT  
		Size: 3.1 MB (3144722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09351dafb4d00c2452eed8ef73da9247d29a3c7c8db5b6483604fd1b96b18ff`  
		Last Modified: Tue, 23 May 2023 19:43:36 GMT  
		Size: 60.8 MB (60782667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b3015e8387f4b48910c7963bdaae5ca97cfe7f0443d8535dbdc7e1f5063816`  
		Last Modified: Tue, 23 May 2023 19:43:31 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; 386

```console
$ docker pull redmine@sha256:b6502a4e5844e5f761aac69f1343c4071b337bee04d63d6349d20d2d18e47f67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242614255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9e59fc2d27361dede193e580d656a55437b099895cdbfd7ac3ceda216e79e6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 May 2023 00:39:30 GMT
ADD file:8319fc1c1a3c0f2a6bb03636fe1fd0eb7fa52c58505d279e4366627452ea2104 in / 
# Tue, 23 May 2023 00:39:30 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:12:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 23 May 2023 01:12:04 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 01:28:03 GMT
ENV RUBY_MAJOR=3.1
# Tue, 23 May 2023 01:28:03 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 23 May 2023 01:28:03 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 23 May 2023 01:31:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 23 May 2023 01:31:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 May 2023 01:31:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 May 2023 01:31:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 01:31:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Tue, 23 May 2023 01:31:40 GMT
CMD ["irb"]
# Tue, 23 May 2023 20:07:12 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 23 May 2023 20:08:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 20:08:03 GMT
ENV RAILS_ENV=production
# Tue, 23 May 2023 20:08:03 GMT
WORKDIR /usr/src/redmine
# Tue, 23 May 2023 20:08:03 GMT
ENV HOME=/home/redmine
# Tue, 23 May 2023 20:08:04 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 23 May 2023 20:08:04 GMT
ENV REDMINE_VERSION=5.0.5
# Tue, 23 May 2023 20:08:04 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Tue, 23 May 2023 20:08:04 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Tue, 23 May 2023 20:08:08 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 23 May 2023 20:08:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 20:08:57 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 May 2023 20:08:57 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 23 May 2023 20:08:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 May 2023 20:08:57 GMT
EXPOSE 3000
# Tue, 23 May 2023 20:08:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0f5d158483bd0ffef0c106b68514aece2ca0500d2990c830844277cbca7fe0bc`  
		Last Modified: Tue, 23 May 2023 00:44:28 GMT  
		Size: 32.4 MB (32388165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e573e66fa2cd19b7052169187d24733be9d6d250dc8898046d0fea6cd049d`  
		Last Modified: Tue, 23 May 2023 01:43:19 GMT  
		Size: 12.0 MB (11997370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35afa18cbcba46f8516124b77bcc5ade8c55162dc60d023b4302c72e9cb40e08`  
		Last Modified: Tue, 23 May 2023 01:43:15 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35da886c11b3e44726a8d010f5314900641263fd2ee12d332bd3587940af7bb`  
		Last Modified: Tue, 23 May 2023 01:44:35 GMT  
		Size: 31.2 MB (31181783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8906d58f8e100a1cc314b06760b6084baa703ad4692de9f4421a955bca26d235`  
		Last Modified: Tue, 23 May 2023 01:44:31 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0085dc86d98d2cce17f44f20af765c68feae60a57db48602e9e58bf0b3480619`  
		Last Modified: Tue, 23 May 2023 20:09:23 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d20f60e7243a9fb6d86471fcdab6379ec43394ee8b124058d8ae1b8188d61b4`  
		Last Modified: Tue, 23 May 2023 20:09:46 GMT  
		Size: 103.3 MB (103280307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f88577d7761fc164721c1374ff603290408a1089b6e2c8b6cc874166a232f`  
		Last Modified: Tue, 23 May 2023 20:09:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d6b18e3160d9a71f29ad1e301b52e90fb281779ac15eed5d363898a84a43f1`  
		Last Modified: Tue, 23 May 2023 20:09:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf0c1b1e250a42c9c591801bc7ed83f608656f8120767a2720c975deb797bd5`  
		Last Modified: Tue, 23 May 2023 20:09:22 GMT  
		Size: 3.1 MB (3144706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d2132a28569fcceb1d52266277c464731f4d2add5dba9a07096c568da4fdf2`  
		Last Modified: Tue, 23 May 2023 20:09:32 GMT  
		Size: 60.6 MB (60617470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f37b13ff9c01722a7dc3c8ac9135a011aaf42314ac8ae54c44d301add1ca9d6`  
		Last Modified: Tue, 23 May 2023 20:09:21 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; ppc64le

```console
$ docker pull redmine@sha256:265fc5cb8715d85df8f5b85544484f25a1814290611abed919d388e2d5b8ec50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262602616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b545af270f841702bbef70c27ce71bb202248e98c70fc297d0590769aded071b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 May 2023 01:17:35 GMT
ADD file:719aea085739ec41c255f35070ca652d4e356c5ee62c8237f8ebc7389feb8e38 in / 
# Tue, 23 May 2023 01:17:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:23:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:23:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 23 May 2023 02:23:32 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:40:17 GMT
ENV RUBY_MAJOR=3.1
# Tue, 23 May 2023 02:40:18 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 23 May 2023 02:40:18 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 23 May 2023 02:44:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 23 May 2023 02:44:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 May 2023 02:44:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 May 2023 02:44:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:44:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Tue, 23 May 2023 02:44:22 GMT
CMD ["irb"]
# Tue, 23 May 2023 18:16:09 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 23 May 2023 18:17:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 18:17:23 GMT
ENV RAILS_ENV=production
# Tue, 23 May 2023 18:17:23 GMT
WORKDIR /usr/src/redmine
# Tue, 23 May 2023 18:17:24 GMT
ENV HOME=/home/redmine
# Tue, 23 May 2023 18:17:25 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 23 May 2023 18:17:25 GMT
ENV REDMINE_VERSION=5.0.5
# Tue, 23 May 2023 18:17:26 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Tue, 23 May 2023 18:17:26 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Tue, 23 May 2023 18:17:30 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 23 May 2023 18:20:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 18:20:38 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 May 2023 18:20:38 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 23 May 2023 18:20:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 May 2023 18:20:39 GMT
EXPOSE 3000
# Tue, 23 May 2023 18:20:39 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b6c83d2f160e7e38990586d26caa105ff577368a887fd754ae4634cdbfec83ff`  
		Last Modified: Tue, 23 May 2023 01:22:03 GMT  
		Size: 35.3 MB (35280911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d38ba339ef6043fdfe3ddd5359c69fcf0314d3e805835066f25f5bdec81cbaa`  
		Last Modified: Tue, 23 May 2023 02:52:45 GMT  
		Size: 10.5 MB (10481258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6686de7ce20c5bf6829105ad713ada3bd60313789b594e248ffe5250dc1b159f`  
		Last Modified: Tue, 23 May 2023 02:52:42 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4951bfecfe434f2065bfa58d65d30fcd4683531c9458244fa962c03cc48cd61e`  
		Last Modified: Tue, 23 May 2023 02:54:21 GMT  
		Size: 32.8 MB (32791406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6822a4153fffa9635a3af305ce435ccee23f1029d7a694a724a74fd392835a95`  
		Last Modified: Tue, 23 May 2023 02:54:16 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d010422a0250f16a373f3597c5ff8ad1fc52f61099da6f3072b8ebc2222ebf`  
		Last Modified: Tue, 23 May 2023 18:21:10 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a977b46e219bead533e3a8a515378d18d6cfc2686a5e4dc9e6f30f58879501f`  
		Last Modified: Tue, 23 May 2023 18:21:39 GMT  
		Size: 107.4 MB (107443877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efeaf7f19d0e8d71d60e5bf40ee16aaf9f6e6e2f2c6f0a879872309f6ac334a`  
		Last Modified: Tue, 23 May 2023 18:21:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea5baa1b39474112103625e97ae36a7f5e83a76ddf5932164ee870adcd9fa34`  
		Last Modified: Tue, 23 May 2023 18:21:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e898ff5b6079039bed766daf98fa3b1d19080116f5e49720a78c54a26f6c8c`  
		Last Modified: Tue, 23 May 2023 18:21:10 GMT  
		Size: 3.1 MB (3144728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bec1766d9c0c5db50c697d59a1259f4c4a12c771c95cff12c12556aa59494d`  
		Last Modified: Tue, 23 May 2023 18:21:21 GMT  
		Size: 73.5 MB (73455970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310d196dec1478203b98e845304fb3a5b24b7edfa37caa5354225cfd515c9cfd`  
		Last Modified: Tue, 23 May 2023 18:21:08 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:5-bullseye` - linux; s390x

```console
$ docker pull redmine@sha256:18236c272ce92ebec06b4b013e5436488dd3402f6c27169bbb13e454ea41a60f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246275752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf569631fbadd1e473c5ee1099a537c6b333e906a2296c7680caf94e3e57e20`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Tue, 23 May 2023 00:42:52 GMT
ADD file:23b1e12559302529556a94a1d4098dbdb454e263265258b940c2b2d23a97c121 in / 
# Tue, 23 May 2023 00:42:54 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:16:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:16:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 23 May 2023 02:16:13 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:20:52 GMT
ENV RUBY_MAJOR=3.1
# Tue, 23 May 2023 02:20:52 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 23 May 2023 02:20:52 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Tue, 23 May 2023 02:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 23 May 2023 02:22:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 May 2023 02:22:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 May 2023 02:22:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:22:51 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Tue, 23 May 2023 02:22:51 GMT
CMD ["irb"]
# Tue, 23 May 2023 07:30:19 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 23 May 2023 07:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:31:07 GMT
ENV RAILS_ENV=production
# Tue, 23 May 2023 07:31:08 GMT
WORKDIR /usr/src/redmine
# Tue, 23 May 2023 07:31:08 GMT
ENV HOME=/home/redmine
# Tue, 23 May 2023 07:31:08 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 23 May 2023 07:31:08 GMT
ENV REDMINE_VERSION=5.0.5
# Tue, 23 May 2023 07:31:08 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.5.tar.gz
# Tue, 23 May 2023 07:31:09 GMT
ENV REDMINE_DOWNLOAD_SHA256=a89ad1c4bb9bf025e6527c77ab18c8faf7749c94a975caf2cfdbba00eb12a481
# Tue, 23 May 2023 07:31:12 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 23 May 2023 07:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 May 2023 07:32:39 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 23 May 2023 07:32:39 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 23 May 2023 07:32:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:32:40 GMT
EXPOSE 3000
# Tue, 23 May 2023 07:32:40 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9c24ec455bdb6a9ad0d033c7cce8e71dd5bdbbe53a86d5feeb8d4cb7804fb8e5`  
		Last Modified: Tue, 23 May 2023 00:45:47 GMT  
		Size: 29.6 MB (29642170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389e5acb5f585dd7876222f795a0f8adb45bbb36dfee1707ad06ef3c32abe06a`  
		Last Modified: Tue, 23 May 2023 02:25:49 GMT  
		Size: 8.9 MB (8864321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f41881192359d6eae65c1dea80a1676401b472e6565797e2c8a05658dbfc19`  
		Last Modified: Tue, 23 May 2023 02:25:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024533d1e28fb42ceec653648bb53ba0eec8a926cca2b4c37f7b9b789b7af370`  
		Last Modified: Tue, 23 May 2023 02:26:18 GMT  
		Size: 32.4 MB (32444939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b5d84dde0b278d9f070f6f6be97cb4cd0dd9049cae6b5db6e105f3c27889b4`  
		Last Modified: Tue, 23 May 2023 02:26:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e124e3b7008c7cc2e28a51aa7d2a4d7799cc31412bd73e1977dbefce7f106f`  
		Last Modified: Tue, 23 May 2023 07:33:23 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5da631b4b4c7127198e48f86bf58b8faf488ef102faab591fcfcf25d9b04c6`  
		Last Modified: Tue, 23 May 2023 07:33:40 GMT  
		Size: 99.1 MB (99100022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8194e9b168568a9374eb0c7d7b975522db3580b5925d9c8fbabdda7e5e737e17`  
		Last Modified: Tue, 23 May 2023 07:33:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30f3e6e11e4514ccc6404483280e3630549835793dff5b03361dbe9c29d547d`  
		Last Modified: Tue, 23 May 2023 07:33:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2caf823e61a2e7d70afc4d2d259076a7bc395aa17754d3ed013ab5045800091`  
		Last Modified: Tue, 23 May 2023 07:33:22 GMT  
		Size: 3.1 MB (3144736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a796f7a39654617ecd8921840d5250fb82d7ae4ec20522b6f04ea4b2e69827d`  
		Last Modified: Tue, 23 May 2023 07:33:28 GMT  
		Size: 73.1 MB (73075099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7620f92f662463a03d08b4f50297a1a6294fd6fb5372fc89156fbdc05b85dd`  
		Last Modified: Tue, 23 May 2023 07:33:21 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
