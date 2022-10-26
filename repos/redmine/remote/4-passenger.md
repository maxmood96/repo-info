## `redmine:4-passenger`

```console
$ docker pull redmine@sha256:aa184dd16307b96f12447e15eac3d23c98c382e3deb89f9623122a8e09a70eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `redmine:4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:26a0a094f5270794a972a2dd5e428e097320a5b9efd43cfd95154e5b546b484d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233942071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c7ee3b23bbc4fd746ffa01edffe1cfb498b6066b3d8220e7f429819d9775d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:08:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:08:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 25 Oct 2022 08:08:32 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 08:24:54 GMT
ENV RUBY_MAJOR=2.7
# Tue, 25 Oct 2022 08:24:54 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 25 Oct 2022 08:24:54 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 25 Oct 2022 08:26:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 25 Oct 2022 08:26:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 25 Oct 2022 08:26:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 25 Oct 2022 08:26:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 08:26:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 25 Oct 2022 08:26:46 GMT
CMD ["irb"]
# Tue, 25 Oct 2022 20:29:30 GMT
RUN groupadd -r -g 999 redmine && useradd -r -g redmine -u 999 redmine
# Tue, 25 Oct 2022 20:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 				bzr 		git 		mercurial 		openssh-client 		subversion 				ghostscript 		gsfonts 		imagemagick 		gosu 		tini 	; 	sed -ri 's/(rights)="none" (pattern="PDF")/\1="read" \2/' /etc/ImageMagick-6/policy.xml; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:29:57 GMT
ENV RAILS_ENV=production
# Tue, 25 Oct 2022 20:29:57 GMT
WORKDIR /usr/src/redmine
# Tue, 25 Oct 2022 20:29:57 GMT
ENV HOME=/home/redmine
# Tue, 25 Oct 2022 20:29:58 GMT
RUN set -eux; 	[ ! -d "$HOME" ]; 	mkdir -p "$HOME"; 	chown redmine:redmine "$HOME"; 	chmod 1777 "$HOME"
# Tue, 25 Oct 2022 20:29:58 GMT
ENV REDMINE_VERSION=4.2.8
# Tue, 25 Oct 2022 20:29:58 GMT
ENV REDMINE_DOWNLOAD_URL=https://www.redmine.org/releases/redmine-4.2.8.tar.gz
# Tue, 25 Oct 2022 20:29:58 GMT
ENV REDMINE_DOWNLOAD_SHA256=0b431c052d8fd36b93201dafaf3615cdb8d03460efcf2400e7d32662b2ab6272
# Tue, 25 Oct 2022 20:30:01 GMT
RUN set -eux; 	curl -fL -o redmine.tar.gz "$REDMINE_DOWNLOAD_URL"; 	echo "$REDMINE_DOWNLOAD_SHA256 *redmine.tar.gz" | sha256sum -c -; 	tar -xf redmine.tar.gz --strip-components=1; 	rm redmine.tar.gz files/delete.me log/delete.me; 	mkdir -p log public/plugin_assets sqlite tmp/pdf tmp/pids; 	chown -R redmine:redmine ./; 	echo 'config.logger = Logger.new(STDOUT)' > config/additional_environment.rb; 	chmod -R ugo=rwX config db sqlite; 	find log tmp -type d -exec chmod 1777 '{}' +
# Tue, 25 Oct 2022 20:30:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		default-libmysqlclient-dev 		freetds-dev 		gcc 		libpq-dev 		libsqlite3-dev 		make 		patch 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		gosu redmine bundle config --local without 'development test'; 	puma="$(grep -E "^[[:space:]]*gem [:'\"]puma['\",[:space:]].*\$" Gemfile)"; 	{ echo; echo "$puma"; } | sed -re 's/^[[:space:]]+//' >> Gemfile; 	echo '# the following entries only exist to force `bundle install` to pre-install all database adapter dependencies -- they can be safely removed/ignored' > ./config/database.yml; 	for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$adapter:" >> ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 	done; 	gosu redmine bundle install --jobs "$(nproc)"; 	rm ./config/database.yml; 	chmod -R ugo=rwX Gemfile.lock "$GEM_HOME"; 	rm -rf ~redmine/.bundle; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -v '^/usr/local/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Oct 2022 20:30:46 GMT
VOLUME [/usr/src/redmine/files]
# Tue, 25 Oct 2022 20:30:46 GMT
COPY file:f61e8718e722eba56748d9a7e58011159861fb49784b1ad721746c1fc5735b6d in / 
# Tue, 25 Oct 2022 20:30:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Oct 2022 20:30:46 GMT
EXPOSE 3000
# Tue, 25 Oct 2022 20:30:47 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Tue, 25 Oct 2022 20:30:53 GMT
ENV PASSENGER_VERSION=6.0.15
# Tue, 25 Oct 2022 20:31:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gcc 		make 	; 	rm -rf /var/lib/apt/lists/*; 		gem install passenger --version "$PASSENGER_VERSION"; 	passenger-config build-native-support; 	if [ -n "$(passenger-config build-native-support 2>&1)" ]; then cat /tmp/passenger_native_support-*.log; false; fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Oct 2022 20:31:11 GMT
RUN set -eux; 	passenger-config install-agent; 	passenger-config download-nginx-engine
# Tue, 25 Oct 2022 20:31:11 GMT
ENV PASSENGER_PID_FILE=tmp/pids/server.pid
# Tue, 25 Oct 2022 20:31:11 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009a5b08accbeaf60176b2dbabecbb95bcc60b2705679b6956856848fef05e78`  
		Last Modified: Tue, 25 Oct 2022 08:30:41 GMT  
		Size: 10.0 MB (10020386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886fce225b5fdd6139310267139044feaa2ceead04880fcc20ad6c299c016661`  
		Last Modified: Tue, 25 Oct 2022 08:30:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c656fb77bbec99e918bb8e55f1b318851f66ac21c902e929812e4c8e26fcd6d5`  
		Last Modified: Tue, 25 Oct 2022 08:32:42 GMT  
		Size: 14.6 MB (14583037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee93fc08be7d9ef0ef167af57324538fc818a4b8b2d105a521870c5da7e43bd`  
		Last Modified: Tue, 25 Oct 2022 08:32:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af604ba71bbf6db61dbac1fc4880131f46a99740bdc0487b77dd2497764fc68`  
		Last Modified: Tue, 25 Oct 2022 20:32:40 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3697c5023d89e972419b818944cb712ac0b6e3fa7434e0ef77e509a229d9bd`  
		Last Modified: Tue, 25 Oct 2022 20:32:56 GMT  
		Size: 102.0 MB (101993381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21087ecfaff96dcb4500574f23d1eba2ed505a4e2023d261adbd18b0b6ce596a`  
		Last Modified: Tue, 25 Oct 2022 20:32:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d29410ce45cb4385db772e8756236b351f4f0cc0c94c56d7f6d3ef66322ca16`  
		Last Modified: Tue, 25 Oct 2022 20:32:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b355d6f25141de646f62e9cd1adc640a78ea4a0b62752d16f20facb7432af2`  
		Last Modified: Tue, 25 Oct 2022 20:32:39 GMT  
		Size: 3.1 MB (3066581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5540e05a5d598f62b5eba13d47f509d58b811b74d3077e556aeb8dc5fd856b2d`  
		Last Modified: Tue, 25 Oct 2022 20:32:47 GMT  
		Size: 45.2 MB (45190634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3867860b319583f91790c3f40dcef2417b5e1d0fd66c5f2e08f0bc0da0f5f89e`  
		Last Modified: Tue, 25 Oct 2022 20:32:38 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de784c1019a6686afaa4246d4ac15f6ebe152921c6e6764ab132f386aa22de11`  
		Last Modified: Tue, 25 Oct 2022 20:33:21 GMT  
		Size: 22.1 MB (22116597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d2af4c1836b503b41127e91000af28b1737f11ebcaaa25583a2723401cff75`  
		Last Modified: Tue, 25 Oct 2022 20:33:18 GMT  
		Size: 5.5 MB (5546961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
