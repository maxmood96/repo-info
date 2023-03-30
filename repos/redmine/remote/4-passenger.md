## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:3d962b94ef55ce9bcf3945047734219d1da60f3c26151ccfbcfc9d90a8e17ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:a1f413e082f5b17a5f1bf3e1ed339db201718a776386edc91648197c2c7cab3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233945737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86072df17aff7c5f2dc4b4758d14f799e4a8bfe88f8a4d3dfac44815ca14663`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 16:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 16:05:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 23 Mar 2023 16:05:39 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 16:33:30 GMT
ENV RUBY_MAJOR=2.7
# Thu, 30 Mar 2023 20:03:14 GMT
ENV RUBY_VERSION=2.7.8
# Thu, 30 Mar 2023 20:03:14 GMT
ENV RUBY_DOWNLOAD_SHA256=f22f662da504d49ce2080e446e4bea7008cee11d5ec4858fc69000d0e5b1d7fb
# Thu, 30 Mar 2023 20:05:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 30 Mar 2023 20:05:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 Mar 2023 20:05:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 Mar 2023 20:05:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Mar 2023 20:05:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 30 Mar 2023 20:05:01 GMT
CMD ["irb"]
# Thu, 30 Mar 2023 20:35:47 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Thu, 30 Mar 2023 20:36:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 Mar 2023 20:36:10 GMT
ENV RAILS_ENV=production
# Thu, 30 Mar 2023 20:36:10 GMT
WORKDIR /usr/src/redmine
# Thu, 30 Mar 2023 20:36:10 GMT
ENV HOME=/home/redmine
# Thu, 30 Mar 2023 20:36:11 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Thu, 30 Mar 2023 20:36:11 GMT
ENV REDMINE_VERSION=4.2.10
# Thu, 30 Mar 2023 20:36:11 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.10.tar.gz
# Thu, 30 Mar 2023 20:36:11 GMT
ENV REDMINE_DOWNLOAD_SHA256=6f26388c23892962552ca491d5efedabd42dac88861dd9d80bc33458f65be1e9
# Thu, 30 Mar 2023 20:36:14 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Thu, 30 Mar 2023 20:36:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 30 Mar 2023 20:36:56 GMT
VOLUME [/usr/src/redmine/files]
# Thu, 30 Mar 2023 20:36:56 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Thu, 30 Mar 2023 20:36:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Mar 2023 20:36:56 GMT
EXPOSE 3000
# Thu, 30 Mar 2023 20:36:56 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Thu, 30 Mar 2023 20:37:09 GMT
ENV PASSENGER_VERSION=6.0.17
# Thu, 30 Mar 2023 20:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 30 Mar 2023 20:37:27 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Thu, 30 Mar 2023 20:37:27 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Thu, 30 Mar 2023 20:37:27 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b6c5e514e1b14fbdb31cb290dc9e714aab2152526b6807ebca5713c53cfa19`  
		Last Modified: Thu, 23 Mar 2023 16:39:55 GMT  
		Size: 10.0 MB (10023421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77fe2302da079bdc4425a38a2e8615bb9a8a19e32bd72f7d7b0b63e1831e069`  
		Last Modified: Thu, 23 Mar 2023 16:39:53 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff7ec1d7d50f958f29d658a8d50193f41d9ec88226060f32a0de57898307a8f`  
		Last Modified: Thu, 30 Mar 2023 20:15:57 GMT  
		Size: 14.6 MB (14582745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b726c02bc91a65acd215d0083c9d95f65c052e3c333539a41ed28372940f8f2`  
		Last Modified: Thu, 30 Mar 2023 20:15:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fca822c8a4a072dbf1be47a2d7327e392f6dcb57b15bcad6bc7ce5e8d24c62`  
		Last Modified: Thu, 30 Mar 2023 20:41:22 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1754bd9104d9657e70efb737dd5aa5b9cf66f28341e2e8d1fb9dfcf11acd8657`  
		Last Modified: Thu, 30 Mar 2023 20:41:36 GMT  
		Size: 101.9 MB (101904652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad1042b1aac948fd246d4e35226b2fb72f45bdd64534d26df543433a04a70c7`  
		Last Modified: Thu, 30 Mar 2023 20:41:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8c12568812438a94eb11ff02a79d102ff6ff613a6b95e8a0266e6725049c14`  
		Last Modified: Thu, 30 Mar 2023 20:41:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cd31a8ef5ecfdac9354c03ad558c033effa05a85941031494903aa036eb5d4`  
		Last Modified: Thu, 30 Mar 2023 20:41:21 GMT  
		Size: 3.1 MB (3068912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a56f07555a1bfad03fea91064363b69bf69b4671cd5997821aff680d2712560`  
		Last Modified: Thu, 30 Mar 2023 20:41:25 GMT  
		Size: 45.1 MB (45087888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e866ea731273f3a972eae90eb2f5bc315c9a07d59c0b277f9c19943cd441848b`  
		Last Modified: Thu, 30 Mar 2023 20:41:20 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3cba4c11e904414bb2015175fb67fe66cb4e75c459a81168795940cf1cc04b`  
		Last Modified: Thu, 30 Mar 2023 20:41:56 GMT  
		Size: 22.2 MB (22245362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac52a3cf1699f8c79961f300585bcdbc20c6923a01eff04225aade35fafa99c`  
		Last Modified: Thu, 30 Mar 2023 20:41:54 GMT  
		Size: 5.6 MB (5616891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
