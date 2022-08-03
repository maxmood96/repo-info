## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:a315eb0c85c3f48a12881df18fef9bb704684f728e931d380931e272bf401124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:a524c0d6fe191d2f66035cc1ec7495d243df38eb9a256b3f526585ecc0ca3cd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233668837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07bf276bdf94e9179ee763d23bd1945d994f5fd68d2764698615e1879788449`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 14:12:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 14:12:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 02 Aug 2022 14:12:57 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 14:41:38 GMT
ENV RUBY_MAJOR=2.7
# Tue, 02 Aug 2022 14:41:38 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 02 Aug 2022 14:41:38 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 02 Aug 2022 14:43:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 02 Aug 2022 14:43:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 02 Aug 2022 14:43:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 02 Aug 2022 14:43:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 14:43:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 02 Aug 2022 14:43:29 GMT
CMD ["irb"]
# Wed, 03 Aug 2022 11:54:04 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Wed, 03 Aug 2022 11:54:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 11:54:30 GMT
ENV RAILS_ENV=production
# Wed, 03 Aug 2022 11:54:30 GMT
WORKDIR /usr/src/redmine
# Wed, 03 Aug 2022 11:54:31 GMT
ENV HOME=/home/redmine
# Wed, 03 Aug 2022 11:54:31 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Wed, 03 Aug 2022 11:54:31 GMT
ENV REDMINE_VERSION=4.2.7
# Wed, 03 Aug 2022 11:54:31 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.7.tar.gz
# Wed, 03 Aug 2022 11:54:31 GMT
ENV REDMINE_DOWNLOAD_SHA256=ed4be03b5ab63c2641a87db8978739dd997c0f646bfa1010ac9e5210c343724e
# Wed, 03 Aug 2022 11:54:35 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Wed, 03 Aug 2022 11:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Aug 2022 11:55:18 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 03 Aug 2022 11:55:18 GMT
COPY file:5ad924c6f87c91325ac6781766e5ad56444f0bea5780e13e8bed5000ee3cfc38 in / 
# Wed, 03 Aug 2022 11:55:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:55:19 GMT
EXPOSE 3000
# Wed, 03 Aug 2022 11:55:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Wed, 03 Aug 2022 11:55:27 GMT
ENV PASSENGER_VERSION=6.0.14
# Wed, 03 Aug 2022 11:55:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Aug 2022 11:55:45 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Wed, 03 Aug 2022 11:55:45 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Wed, 03 Aug 2022 11:55:46 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bb0f44ae93459375f6748f7e0da260969856f977e505f1e69f788aed567024`  
		Last Modified: Tue, 02 Aug 2022 14:49:22 GMT  
		Size: 10.0 MB (9991988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a772400c0cb95deeb07842407e5e9c47b819275298c7c61aaa823ac39690e9`  
		Last Modified: Tue, 02 Aug 2022 14:49:20 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7518cd34e0768a362b2f0369b5c4d0d4cbefc85a0bb99abca28632eeb2f5cf6`  
		Last Modified: Tue, 02 Aug 2022 14:53:07 GMT  
		Size: 14.6 MB (14582333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe3a491a3bd821351544fde48757d96ab4749e764dc28befd42e3618067195`  
		Last Modified: Tue, 02 Aug 2022 14:53:05 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414f1730bfbe113703f767568e7bfdc4c05e77f0a0137f9434f8e299b437f306`  
		Last Modified: Wed, 03 Aug 2022 11:57:18 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b0964a59f3fcf1253f1e5b6fda6161d210093aecbfb80a4da395ea8837c0e3`  
		Last Modified: Wed, 03 Aug 2022 11:57:34 GMT  
		Size: 102.0 MB (101991336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eaa8dea3fe0210431bbad4d37318c948ab22bd3e4b32e9d8280f8a8fcd485a1`  
		Last Modified: Wed, 03 Aug 2022 11:57:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6a0eeb02b1e33ec6c91906c65adea204244cb18782d415015ec8702ba431d5`  
		Last Modified: Wed, 03 Aug 2022 11:57:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a2beeed31f86f1636b0700dc676854712ee862f6cda679a18dfd022e896872`  
		Last Modified: Wed, 03 Aug 2022 11:57:17 GMT  
		Size: 3.1 MB (3066349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8372afbbc58a28df18027a317c036bacebbdaaafaa2608464c25e60792344b31`  
		Last Modified: Wed, 03 Aug 2022 11:57:21 GMT  
		Size: 45.3 MB (45321151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa8a3734a86e0625196d123e7989a2d404bc3d3ff2678a42cda7f7b33a0bf05`  
		Last Modified: Wed, 03 Aug 2022 11:57:16 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9872faec321f4edc4c22b2aea16701fe2015bef3c46a7d9a8a27bd8c86339860`  
		Last Modified: Wed, 03 Aug 2022 11:57:58 GMT  
		Size: 21.8 MB (21800199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c7f98df135aa1141c8c8e567a7180388b0e34ae75026896a614266742b6d51`  
		Last Modified: Wed, 03 Aug 2022 11:57:56 GMT  
		Size: 5.5 MB (5544417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
