## `redmine:bookworm`

```console
$ docker pull redmine@sha256:3dbed9c94b142170575108b5a59f8bc5e2cae7421ec47b02440cb2385c8bed14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 9
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; s390x

### `redmine:bookworm` - linux; amd64

```console
$ docker pull redmine@sha256:17a3fa3cc804bdede55a1d906056a9cf9a57abf6b69e36bd3d0b1328d6509b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264153304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a089d3c65bcd170b4399367aea49643d983ead3feb2dcd633c98c45bc350ee8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 30 Sep 2023 08:26:15 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Sat, 30 Sep 2023 08:26:15 GMT
CMD ["bash"]
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 30 Sep 2023 08:26:15 GMT
ENV LANG=C.UTF-8
# Sat, 30 Sep 2023 08:26:15 GMT
ENV RUBY_MAJOR=3.1
# Sat, 30 Sep 2023 08:26:15 GMT
ENV RUBY_VERSION=3.1.4
# Sat, 30 Sep 2023 08:26:15 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 30 Sep 2023 08:26:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 30 Sep 2023 08:26:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 30 Sep 2023 08:26:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Sep 2023 08:26:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Sat, 30 Sep 2023 08:26:15 GMT
CMD ["irb"]
# Sat, 30 Sep 2023 08:26:15 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
ENV RAILS_ENV=production
# Sat, 30 Sep 2023 08:26:15 GMT
WORKDIR /usr/src/redmine
# Sat, 30 Sep 2023 08:26:15 GMT
ENV HOME=/home/redmine
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
ENV REDMINE_VERSION=5.0.6
# Sat, 30 Sep 2023 08:26:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.6.tar.gz
# Sat, 30 Sep 2023 08:26:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=488fe08f37a8eb1011415922a8ea743b7f38d8a7a5f8822950a34a375dcf08ee
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 30 Sep 2023 08:26:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Sep 2023 08:26:15 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 30 Sep 2023 08:26:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32882a047637d1e356aac96e3485e5c4f16490e83ac72bf0f69340bc69b73b3`  
		Last Modified: Wed, 11 Oct 2023 21:02:39 GMT  
		Size: 13.9 MB (13853087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb17d33ba4abee39ce1feb59f447a85aa6e1a10686552ec9c2b36c4de74acb9f`  
		Last Modified: Wed, 11 Oct 2023 21:02:37 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abc5610912a216bef86f31252003165227b6a4a4c3b75ea34757f8ec55f1225`  
		Last Modified: Wed, 11 Oct 2023 21:04:00 GMT  
		Size: 32.9 MB (32923982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aade4254051370d665168ebd1057b5f0f4706ba5747709f0704490a81a0fa6`  
		Last Modified: Wed, 11 Oct 2023 21:03:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08f9fcdac599558d64355b8f54fb24eb3d33becd5107dc53612b70addf2d062`  
		Last Modified: Fri, 20 Oct 2023 16:04:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac238a0b4e4c6e19fb0faf694e6ea2a344ba719ce48d84557ace0cecced376a`  
		Last Modified: Fri, 20 Oct 2023 16:04:25 GMT  
		Size: 123.1 MB (123111358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbb1283b2174a80985434b590fb4a3201e3bec334331b2fae0b9d12b93028f4`  
		Last Modified: Fri, 20 Oct 2023 16:04:19 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6e85af125f5c484a64342b4342c57f57dfe65a9ee4ef612c503fc12cf5e3a2`  
		Last Modified: Fri, 20 Oct 2023 16:04:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9506678f98ba29fa06c2422895271532b444d08bdef2861f6f4c9ac191235e22`  
		Last Modified: Fri, 20 Oct 2023 16:04:21 GMT  
		Size: 3.1 MB (3146234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c6d62a208e81284b666c099df4acf6af4267b9b49ae25466460443c3e42bb3`  
		Last Modified: Fri, 20 Oct 2023 16:04:23 GMT  
		Size: 62.0 MB (61965011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e670e8442751d6e27cf72685412ef2cc1f54b3f389a6663eb4601952d71a5d`  
		Last Modified: Fri, 20 Oct 2023 16:04:20 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:eb50b73b6dd69efe6c3ee1dc6a7a5bb04cd1b58f1324ecd2dd73e5e9cac403b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7586556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1434af4cc68cd18650e0558ce95d9a9d66652ee885bda77084a089cfbf8c69b8`

```dockerfile
```

-	Layers:
	-	`sha256:ce5a3db66637a56ba943da2df28e6ffd930425022a337846b76b0aa8d0adadcd`  
		Last Modified: Fri, 20 Oct 2023 16:04:19 GMT  
		Size: 7.6 MB (7550989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a351b42ea85e5f9df71a70293dcbc5ce17df6108c99bf1b46e1c19302e98a80`  
		Last Modified: Fri, 20 Oct 2023 16:04:17 GMT  
		Size: 35.6 KB (35567 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; arm variant v5

```console
$ docker pull redmine@sha256:0f83a4fa14bbb397822e6c05179ba92943d0b6b83e9cc78b3f46705e745ce8ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250031847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e153b673f4f66affa667b230e89b82b14d5a4fe2b7db1e5e332606aa905519`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 11 Oct 2023 17:37:43 GMT
ADD file:8c43adb3245fc6f2b10aa5a86c850db5dcf3515eaf7e46630922fe21f806bd2a in / 
# Wed, 11 Oct 2023 17:37:43 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:39:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 Oct 2023 03:39:41 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 04:05:28 GMT
ENV RUBY_MAJOR=3.1
# Thu, 12 Oct 2023 04:05:28 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 12 Oct 2023 04:05:29 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 12 Oct 2023 04:07:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 Oct 2023 04:07:43 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 Oct 2023 04:07:43 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 Oct 2023 04:07:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 04:07:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 12 Oct 2023 04:07:44 GMT
CMD ["irb"]
# Thu, 12 Oct 2023 11:00:01 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 12 Oct 2023 11:00:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:00:48 GMT
ENV RAILS_ENV=production
# Thu, 12 Oct 2023 11:00:48 GMT
WORKDIR /usr/src/redmine
# Thu, 12 Oct 2023 11:00:48 GMT
ENV HOME=/home/redmine
# Thu, 12 Oct 2023 11:00:49 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 12 Oct 2023 11:00:49 GMT
ENV REDMINE_VERSION=5.0.6
# Thu, 12 Oct 2023 11:00:49 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.6.tar.gz
# Thu, 12 Oct 2023 11:00:49 GMT
ENV REDMINE_DOWNLOAD_SHA256=488fe08f37a8eb1011415922a8ea743b7f38d8a7a5f8822950a34a375dcf08ee
# Thu, 12 Oct 2023 11:00:53 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 12 Oct 2023 11:01:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 12 Oct 2023 11:01:32 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 12 Oct 2023 11:01:32 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 12 Oct 2023 11:01:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Oct 2023 11:01:33 GMT
EXPOSE 3000
# Thu, 12 Oct 2023 11:01:33 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:904e6393ef1ee28b37171369eb4f7cb04714631c711799819fccb83886bd212b`  
		Last Modified: Wed, 11 Oct 2023 17:40:47 GMT  
		Size: 26.9 MB (26922150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20203ec6d19ec737e6baed920a74929f0fa4cad2efb189917b3916b5f24edce`  
		Last Modified: Thu, 12 Oct 2023 04:17:33 GMT  
		Size: 11.6 MB (11610568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cdc753315de00d83e4f10414d08e2a555790c803dfa6e177c6f6ecad5102a4`  
		Last Modified: Thu, 12 Oct 2023 04:17:30 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb32b68c91f39aa4481bc6a1049bd847d66c026ceaaac282d8446d23f0fd3649`  
		Last Modified: Thu, 12 Oct 2023 04:19:56 GMT  
		Size: 31.7 MB (31717592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3545bd8b48286239e1687d181553184440e623fdc9ae68718f7eb9677faf57`  
		Last Modified: Thu, 12 Oct 2023 04:19:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7d337cb78774e24f401385b76b02b9c74ae63c9068bcecdbe98261cea40a5e`  
		Last Modified: Thu, 12 Oct 2023 11:01:48 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4d5656d8e616281842b885db4c19576010cc493f84f1f6912905ea08f8da5c`  
		Last Modified: Thu, 12 Oct 2023 11:02:07 GMT  
		Size: 116.6 MB (116646127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2627fb0b5a42e52b57ce6a1887e147e31e68d1f9836b6754a4adc84599db0a`  
		Last Modified: Thu, 12 Oct 2023 11:01:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95189bdba466264a636366613a23621e3283db2b30914715c257816ffa67261`  
		Last Modified: Thu, 12 Oct 2023 11:01:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c117581a8184f047d4e1952183148ca47b7d925e6db69769c206a558558cb8`  
		Last Modified: Thu, 12 Oct 2023 11:01:47 GMT  
		Size: 3.1 MB (3146834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411529fe380b70fe65cd0c67bf520f91b7675e11dda05ccdf3cae45e94836908`  
		Last Modified: Thu, 12 Oct 2023 11:01:53 GMT  
		Size: 60.0 MB (59984735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0bf54d05f35400d77f54ca6817e2e1dccb0bcce3f024996a1a02228c46958d`  
		Last Modified: Thu, 12 Oct 2023 11:01:46 GMT  
		Size: 2.0 KB (2012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:bookworm` - linux; arm variant v7

```console
$ docker pull redmine@sha256:e3f5cf65c4af230b818e827a504a8f33c3dd03a8d23e7f916968a4c74ab4bf95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242293522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d261164ea868181944c817ef47d037b3a300978c3b8207b91bc107b6efe4e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:56:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 02:56:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 Oct 2023 02:56:49 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 03:11:36 GMT
ENV RUBY_MAJOR=3.1
# Thu, 12 Oct 2023 03:11:36 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 12 Oct 2023 03:11:36 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 12 Oct 2023 03:14:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 Oct 2023 03:14:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 Oct 2023 03:14:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 Oct 2023 03:14:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 03:14:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 12 Oct 2023 03:14:01 GMT
CMD ["irb"]
# Thu, 12 Oct 2023 08:27:16 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 12 Oct 2023 08:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 08:28:01 GMT
ENV RAILS_ENV=production
# Thu, 12 Oct 2023 08:28:01 GMT
WORKDIR /usr/src/redmine
# Thu, 12 Oct 2023 08:28:01 GMT
ENV HOME=/home/redmine
# Thu, 12 Oct 2023 08:28:01 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 12 Oct 2023 08:28:01 GMT
ENV REDMINE_VERSION=5.0.6
# Thu, 12 Oct 2023 08:28:01 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.6.tar.gz
# Thu, 12 Oct 2023 08:28:01 GMT
ENV REDMINE_DOWNLOAD_SHA256=488fe08f37a8eb1011415922a8ea743b7f38d8a7a5f8822950a34a375dcf08ee
# Thu, 12 Oct 2023 08:28:05 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 12 Oct 2023 08:28:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 12 Oct 2023 08:28:40 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 12 Oct 2023 08:28:40 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 12 Oct 2023 08:28:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Oct 2023 08:28:41 GMT
EXPOSE 3000
# Thu, 12 Oct 2023 08:28:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32f9959ff346b3c201d6df91a71361277ea210195a1ea4e46d76d8c17caa17b`  
		Last Modified: Thu, 12 Oct 2023 03:22:37 GMT  
		Size: 10.9 MB (10946920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f422dd6a4f2ddb51a2f22b3a8169acba8a5514a182769d761c616038ff0c55b`  
		Last Modified: Thu, 12 Oct 2023 03:22:35 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7854b092aea279cfe6c984ef69a06756de693a7c85052791a9d212d4c9c560d4`  
		Last Modified: Thu, 12 Oct 2023 03:23:59 GMT  
		Size: 31.6 MB (31559908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740be2b65f1c53bc62cbf6cdbd683083be225ba7b90a753bd0edad58542ce21f`  
		Last Modified: Thu, 12 Oct 2023 03:23:56 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b604b3f54499ba4c1c7c8e532ff3f3c8ce6cbc10ac05386f42d2f26f332bb8`  
		Last Modified: Thu, 12 Oct 2023 08:29:09 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18169b03a9842b67e131c7e7b5052d31c37f8bf830d1b49da7460b1799009846`  
		Last Modified: Thu, 12 Oct 2023 08:29:26 GMT  
		Size: 112.1 MB (112146973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95802aa3d40b33b2921fa2da34996801c5e9f498ffcfbce152b154690d1e55c`  
		Last Modified: Thu, 12 Oct 2023 08:29:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad69ab014ee59f6592095267139e2f35957d061758e5d03f30d78a475fa7a3e7`  
		Last Modified: Thu, 12 Oct 2023 08:29:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cd91e3db4c10d8725ccd2ae5945c18539f6fec8525020bc9e81892ff66f1d9`  
		Last Modified: Thu, 12 Oct 2023 08:29:08 GMT  
		Size: 3.1 MB (3146828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e82210e1420cf89aab3f49f7903ac28df9a3b63a4037f9b103514bf8d28b1b`  
		Last Modified: Thu, 12 Oct 2023 08:29:14 GMT  
		Size: 59.7 MB (59740120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f988cc9cad0f0d861b14e829b12a31bf191a90b098c0b122786dacde195cff3`  
		Last Modified: Thu, 12 Oct 2023 08:29:07 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:bookworm` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:2e35066fdb514c3b98dd4b587c7b314b8240270712996043e39a9b4cdcc825d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259635131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c155391e068df4a41b38eada07287863d23ce3c51d8ffccaea2b031078f168`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 04:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 04:02:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 Oct 2023 04:02:24 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 04:25:55 GMT
ENV RUBY_MAJOR=3.1
# Thu, 12 Oct 2023 04:25:55 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 12 Oct 2023 04:25:55 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 12 Oct 2023 04:27:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 Oct 2023 04:27:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 Oct 2023 04:27:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 Oct 2023 04:27:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 04:27:48 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 12 Oct 2023 04:27:48 GMT
CMD ["irb"]
# Thu, 12 Oct 2023 16:52:49 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 12 Oct 2023 16:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 16:53:27 GMT
ENV RAILS_ENV=production
# Thu, 12 Oct 2023 16:53:27 GMT
WORKDIR /usr/src/redmine
# Thu, 12 Oct 2023 16:53:28 GMT
ENV HOME=/home/redmine
# Thu, 12 Oct 2023 16:53:28 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 12 Oct 2023 16:53:28 GMT
ENV REDMINE_VERSION=5.0.6
# Thu, 12 Oct 2023 16:53:28 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.6.tar.gz
# Thu, 12 Oct 2023 16:53:28 GMT
ENV REDMINE_DOWNLOAD_SHA256=488fe08f37a8eb1011415922a8ea743b7f38d8a7a5f8822950a34a375dcf08ee
# Thu, 12 Oct 2023 16:53:31 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 12 Oct 2023 16:54:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 12 Oct 2023 16:54:03 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 12 Oct 2023 16:54:03 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 12 Oct 2023 16:54:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Oct 2023 16:54:03 GMT
EXPOSE 3000
# Thu, 12 Oct 2023 16:54:03 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4740ddbf4a7cc298c91dc6b147b759d6bd3964a1c63d008ea5483c4d1889e50`  
		Last Modified: Thu, 12 Oct 2023 04:39:42 GMT  
		Size: 12.7 MB (12695198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475324cbcdaeec2833906ae4ed7e772221d8079df1a4bd36a032e5ceb9beebea`  
		Last Modified: Thu, 12 Oct 2023 04:39:40 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8a0e3f83d73f8d1341754ae01a0ab50c71fa697b6011a607ff039eb1a1e213`  
		Last Modified: Thu, 12 Oct 2023 04:42:04 GMT  
		Size: 32.4 MB (32361652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58afbb767717699fe13a2d2052f7abd1f5effbc871cc778b0c3b9a10a362ae7`  
		Last Modified: Thu, 12 Oct 2023 04:42:02 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5adc1afaeb861f606c4b3cd1ce74bdf9363aafb3627b69b955988390c9beef`  
		Last Modified: Thu, 12 Oct 2023 16:54:24 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a1c9eb7d61718b1aea4549d8a76f3a92f57e27300b8821ca5f3c71d9636b1c`  
		Last Modified: Thu, 12 Oct 2023 16:54:37 GMT  
		Size: 120.3 MB (120255531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca11e79db83c6c351d819eabf328b6cf594cfd77a2f7b186aa4fc284da601138`  
		Last Modified: Thu, 12 Oct 2023 16:54:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2789c9ff1064a4f2bd0693914de8e0c9d0fa35440bdae43067a6a802dec9e8e`  
		Last Modified: Thu, 12 Oct 2023 16:54:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fa38d38bfea10cd0bdb4a6ae6e42ac075a656361cb8c55b38701bfaa9a10f4`  
		Last Modified: Thu, 12 Oct 2023 16:54:23 GMT  
		Size: 3.1 MB (3146826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064a26c5e5672e82bd5680427278768e46fa109804495d9c619ef1058d6f1935`  
		Last Modified: Thu, 12 Oct 2023 16:54:28 GMT  
		Size: 62.0 MB (61992793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea2fd5ecc33c7381aa5e3e7207ddc4ecc4cbdc2ef236e21a3f5b2723cdb501e`  
		Last Modified: Thu, 12 Oct 2023 16:54:23 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:bookworm` - linux; 386

```console
$ docker pull redmine@sha256:1d71e6bcbdebc951fa303529da3642f158d6428fc19a1bb3201d0e4cb420f411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264667106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921faff00731ad5dea52a19171699e43c7de79d17b783484a28fb477e1ddbbee`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Sat, 30 Sep 2023 08:26:15 GMT
ADD file:31318c1b1f05d559cce42f5b12eef97d916932217e0b987fb07c0fc11bf0a14a in / 
# Sat, 30 Sep 2023 08:26:15 GMT
CMD ["bash"]
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 30 Sep 2023 08:26:15 GMT
ENV LANG=C.UTF-8
# Sat, 30 Sep 2023 08:26:15 GMT
ENV RUBY_MAJOR=3.1
# Sat, 30 Sep 2023 08:26:15 GMT
ENV RUBY_VERSION=3.1.4
# Sat, 30 Sep 2023 08:26:15 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 30 Sep 2023 08:26:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 30 Sep 2023 08:26:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 30 Sep 2023 08:26:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Sep 2023 08:26:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Sat, 30 Sep 2023 08:26:15 GMT
CMD ["irb"]
# Sat, 30 Sep 2023 08:26:15 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
ENV RAILS_ENV=production
# Sat, 30 Sep 2023 08:26:15 GMT
WORKDIR /usr/src/redmine
# Sat, 30 Sep 2023 08:26:15 GMT
ENV HOME=/home/redmine
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME" # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
ENV REDMINE_VERSION=5.0.6
# Sat, 30 Sep 2023 08:26:15 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.6.tar.gz
# Sat, 30 Sep 2023 08:26:15 GMT
ENV REDMINE_DOWNLOAD_SHA256=488fe08f37a8eb1011415922a8ea743b7f38d8a7a5f8822950a34a375dcf08ee
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' + # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
VOLUME [/usr/src/redmine/files]
# Sat, 30 Sep 2023 08:26:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 30 Sep 2023 08:26:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 30 Sep 2023 08:26:15 GMT
EXPOSE map[3000/tcp:{}]
# Sat, 30 Sep 2023 08:26:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b27d0f1369837277a82877763487cdd2535037988fc27e16f11cf74e103ae4cd`  
		Last Modified: Wed, 11 Oct 2023 17:45:31 GMT  
		Size: 30.2 MB (30164118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638854a46d4fd1cda640b11806c707575e28f75a19ae6f73f95ecdff69a54fe2`  
		Last Modified: Thu, 12 Oct 2023 14:48:17 GMT  
		Size: 13.4 MB (13401495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e8019553deac77de65b32cfd6acfa40bce3958e3a89c71e831491b28c452ef`  
		Last Modified: Thu, 12 Oct 2023 14:48:13 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6b004c15d461960d09f57a0b2ae9f89f15462e5536546a22391e70f5aa6347`  
		Last Modified: Thu, 12 Oct 2023 14:50:59 GMT  
		Size: 31.6 MB (31626417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b78d002b24b82e322cae77b2ab8313070cf7bbbfc1c7ad8c10f8df79682b45`  
		Last Modified: Thu, 12 Oct 2023 14:50:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba3d83ea47bf88559e0f6ef81a1bfcd25b15e673a97eedc3b658bed0698acc`  
		Last Modified: Fri, 20 Oct 2023 16:05:47 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23376cb74ee1063ed3f0af0cc40e8fc960b4c8feadc2567e851f91042aee7127`  
		Last Modified: Fri, 20 Oct 2023 16:05:56 GMT  
		Size: 124.9 MB (124941396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19af4186ca51b1320a68a50282a1fa68ea8a1cffac8bc14954aa9be144ea699`  
		Last Modified: Fri, 20 Oct 2023 16:05:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ac5cbcbeb3d4dab50bbb7ccf69aef1f434ceb1ebceaecea0f4b15004ec47ad`  
		Last Modified: Fri, 20 Oct 2023 16:05:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399c77bcc04cf053d84a0ce153993958f4e82ddb45d88d1c1c07c774944c4de`  
		Last Modified: Fri, 20 Oct 2023 16:05:50 GMT  
		Size: 3.1 MB (3146232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035bf288ebb9770cd07104054b78a3685a005597a3cbc8b2f59c3c6ada4c1a3e`  
		Last Modified: Fri, 20 Oct 2023 16:05:54 GMT  
		Size: 61.4 MB (61383683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284852247443acf4b40d0367e2b9b69d79338b7bb7f689cb9dda5227cd42672`  
		Last Modified: Fri, 20 Oct 2023 16:05:50 GMT  
		Size: 2.0 KB (2015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redmine:bookworm` - unknown; unknown

```console
$ docker pull redmine@sha256:44254a45e2a08b132e3070e4b864829424a05f41d600cbeaa3496983951455d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 KB (35296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a6044cd9e52fd427b262b5cacb37a1a8f81a0b7b527988d1cb596f54ff27eb`

```dockerfile
```

-	Layers:
	-	`sha256:fd2f667c8cfbb8243e6bab767b834faf0ad90ff11efc40fb90be12b8920ad497`  
		Last Modified: Fri, 20 Oct 2023 16:05:46 GMT  
		Size: 35.3 KB (35296 bytes)  
		MIME: application/vnd.in-toto+json

### `redmine:bookworm` - linux; ppc64le

```console
$ docker pull redmine@sha256:53ae37dc4a45437faf1956b5baaba3cd2b24fafbedadce9d7c491f1afadd5f54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290127573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac3aa893c6c04f1321beaeddc45b9317ef0e5d68b058d9de78c010c76a70c41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:19 GMT
ADD file:53c83bdd58e7c4003ae769596cc2f8e6b72c0bbb854dbe7f006a39f273848b1b in / 
# Wed, 11 Oct 2023 17:44:21 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 05:50:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 05:50:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 Oct 2023 05:50:24 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 06:41:05 GMT
ENV RUBY_MAJOR=3.1
# Thu, 12 Oct 2023 06:41:05 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 12 Oct 2023 06:41:06 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 12 Oct 2023 06:46:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 Oct 2023 06:46:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 Oct 2023 06:46:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 Oct 2023 06:46:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 06:46:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 12 Oct 2023 06:46:27 GMT
CMD ["irb"]
# Fri, 13 Oct 2023 00:32:46 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 13 Oct 2023 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 00:34:38 GMT
ENV RAILS_ENV=production
# Fri, 13 Oct 2023 00:34:39 GMT
WORKDIR /usr/src/redmine
# Fri, 13 Oct 2023 00:34:40 GMT
ENV HOME=/home/redmine
# Fri, 13 Oct 2023 00:34:41 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 13 Oct 2023 00:34:41 GMT
ENV REDMINE_VERSION=5.0.6
# Fri, 13 Oct 2023 00:34:42 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.6.tar.gz
# Fri, 13 Oct 2023 00:34:42 GMT
ENV REDMINE_DOWNLOAD_SHA256=488fe08f37a8eb1011415922a8ea743b7f38d8a7a5f8822950a34a375dcf08ee
# Fri, 13 Oct 2023 00:34:48 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 13 Oct 2023 00:37:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 13 Oct 2023 00:37:39 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 13 Oct 2023 00:37:40 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Fri, 13 Oct 2023 00:37:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 00:37:40 GMT
EXPOSE 3000
# Fri, 13 Oct 2023 00:37:41 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:54813908ce8a5d8a81f2db88ad0366eb5266484c7c402e5e93ef26e764f7a0e2`  
		Last Modified: Wed, 11 Oct 2023 17:49:58 GMT  
		Size: 33.1 MB (33141653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbee63d9345729ab4b0dc112a2c786811261a1d6d98c54e78874dd8f3afa73`  
		Last Modified: Thu, 12 Oct 2023 07:05:27 GMT  
		Size: 14.6 MB (14574846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e661119bc16f9cb71e1eaba8592ff901f4caf2b74d87bd9cd48f5f10d5b27c`  
		Last Modified: Thu, 12 Oct 2023 07:05:22 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6eac7d82bc424b5ff04f0d69f25aadb7c0227661774a519f6a3a9c520ec57e5`  
		Last Modified: Thu, 12 Oct 2023 07:08:15 GMT  
		Size: 33.3 MB (33286004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b36c097ca364e442561e152a8f52add18ef22a9439bd78a3842f7609685692c`  
		Last Modified: Thu, 12 Oct 2023 07:08:09 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec34256ab541408fec3cc8ac1690d30d0fd833e7dc2a58a6ff8f405273be970`  
		Last Modified: Fri, 13 Oct 2023 00:38:06 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4247e0981934313013303f65c2225339acbe368ada8dd604dc91db0732aec93e`  
		Last Modified: Fri, 13 Oct 2023 00:38:25 GMT  
		Size: 129.9 MB (129885088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14210e41db8a251a98950d790ab4578ba7ff9597154581984daf76571e806303`  
		Last Modified: Fri, 13 Oct 2023 00:38:04 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ae1ecabdf0c0dbc35eac4d83becc5ace7c4c88693befc4b1626800375bbe85`  
		Last Modified: Fri, 13 Oct 2023 00:38:04 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb382831b2489e6ecb1a76cc0931f96a0f6c2a7d37d90d3aadb0f28e34bc9feb`  
		Last Modified: Fri, 13 Oct 2023 00:38:04 GMT  
		Size: 3.1 MB (3146834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a855adcb50d8d92845ea279e73fb4725300b98e3a3f33fb798bac8b479d0fa31`  
		Last Modified: Fri, 13 Oct 2023 00:38:12 GMT  
		Size: 76.1 MB (76089298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a8172abbc0f7f249de9d227ff92b762dd6bbc4f5790cb64e7b15999a0b090b`  
		Last Modified: Fri, 13 Oct 2023 00:38:03 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:bookworm` - linux; s390x

```console
$ docker pull redmine@sha256:17a8c80fd2e50c48af572d2bf1e0de01aa1cb6de6f444992204154c98a07f136
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269069368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9d2a79ee01c2bf8632f2b4e203ffdd0e3a2b950ad8f13ee725c6ff9e8bc532`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:28 GMT
ADD file:b85ed0ed01200dd3626d66cf5205d989fc48e61b3dd3498f777ee72d91e64870 in / 
# Wed, 11 Oct 2023 17:50:30 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 11:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:45:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 12 Oct 2023 11:45:19 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 12:09:58 GMT
ENV RUBY_MAJOR=3.1
# Thu, 12 Oct 2023 12:09:58 GMT
ENV RUBY_VERSION=3.1.4
# Thu, 12 Oct 2023 12:09:58 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 12 Oct 2023 12:12:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 12 Oct 2023 12:12:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 12 Oct 2023 12:12:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 12 Oct 2023 12:12:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 12:12:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 12 Oct 2023 12:12:28 GMT
CMD ["irb"]
# Fri, 13 Oct 2023 05:18:51 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Fri, 13 Oct 2023 05:19:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 05:19:57 GMT
ENV RAILS_ENV=production
# Fri, 13 Oct 2023 05:19:57 GMT
WORKDIR /usr/src/redmine
# Fri, 13 Oct 2023 05:19:57 GMT
ENV HOME=/home/redmine
# Fri, 13 Oct 2023 05:19:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Fri, 13 Oct 2023 05:19:58 GMT
ENV REDMINE_VERSION=5.0.6
# Fri, 13 Oct 2023 05:19:59 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-5.0.6.tar.gz
# Fri, 13 Oct 2023 05:19:59 GMT
ENV REDMINE_DOWNLOAD_SHA256=488fe08f37a8eb1011415922a8ea743b7f38d8a7a5f8822950a34a375dcf08ee
# Fri, 13 Oct 2023 05:20:03 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Fri, 13 Oct 2023 05:21:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 13 Oct 2023 05:21:50 GMT
VOLUME [/usr/src/redmine/files]
# Fri, 13 Oct 2023 05:21:50 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Fri, 13 Oct 2023 05:21:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 05:21:51 GMT
EXPOSE 3000
# Fri, 13 Oct 2023 05:21:51 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f270c1bb05fa46b165ce3680225dc9fa5bbfe4d69420a467350e80f692c78eb2`  
		Last Modified: Wed, 11 Oct 2023 17:56:03 GMT  
		Size: 27.5 MB (27512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e877f3c81bf9a50810bf096d00872903283fe09d73ff90425ae4548053d11291`  
		Last Modified: Thu, 12 Oct 2023 12:23:30 GMT  
		Size: 12.0 MB (12026488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885ef75b8a470e680c4dd3fcbe2f55924154f5a9bffefea8551c18f1de9f2a5d`  
		Last Modified: Thu, 12 Oct 2023 12:23:28 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dff19f4f6c18b490cc68f269663fca46e5482cb9cd4929fa69afe06ed899bd`  
		Last Modified: Thu, 12 Oct 2023 12:30:12 GMT  
		Size: 32.5 MB (32541780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a34cc442788cb9fe612b5b72a0842581f32af86f7682bf829c64d317129712`  
		Last Modified: Thu, 12 Oct 2023 12:30:08 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687028e2fd6c1de6fa1d4667b6283a70b384ce6bb4a2c145cf844060168bf0c3`  
		Last Modified: Fri, 13 Oct 2023 05:22:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e32208c300ce0bf6df9fc43bbb9a7b72012b27146deea15c35450f9ef5f7ca`  
		Last Modified: Fri, 13 Oct 2023 05:22:34 GMT  
		Size: 118.7 MB (118678146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c584b9d8867ff7c6b7e73d6042c61209fe0dbf723d4f6ae1ff3971c52d22a09`  
		Last Modified: Fri, 13 Oct 2023 05:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c6a23bf9ee10bf1d7fdea8e90962e09510868f32a3e872f3b8cee2ed16669c`  
		Last Modified: Fri, 13 Oct 2023 05:22:17 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09b6b6c88e1a0c9e052ba0c1293c35244ece8d9c61f87aaedfebb9f08ec36cd`  
		Last Modified: Fri, 13 Oct 2023 05:22:17 GMT  
		Size: 3.1 MB (3146834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9509f0d857ed118789a4c031a16f145c3e18be1dd2e839ec159d92e694c61552`  
		Last Modified: Fri, 13 Oct 2023 05:22:24 GMT  
		Size: 75.2 MB (75159421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2780a990d6f591bf725f6096a7acb06ae5cc8d3a0d002ad7b43cba621b63ff`  
		Last Modified: Fri, 13 Oct 2023 05:22:17 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
