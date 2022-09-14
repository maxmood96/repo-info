## `ruby:3-slim-buster`

```console
$ docker pull ruby@sha256:301b10da2b8a94187e690e16e9c0aac1dfd7ad4d0fde9c0a1394516fb3de9214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `ruby:3-slim-buster` - linux; amd64

```console
$ docker pull ruby@sha256:084d85fa52705a51083baee6feb987d6343a42a9370a4af30ab3987dd986eccc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71873687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9108341de6577f6f469b85910a2ae6aa70dc476c68878052e194f4fbb9298f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:10:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:10:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Sep 2022 03:10:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 03:15:04 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Sep 2022 03:15:04 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 13 Sep 2022 03:15:04 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 13 Sep 2022 03:17:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 13 Sep 2022 03:17:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Sep 2022 03:17:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Sep 2022 03:17:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 03:17:22 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 13 Sep 2022 03:17:22 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4cb661b516b0ad739cbf3d36fc7631a481167d9b1f303ad0a7e11219609495`  
		Last Modified: Tue, 13 Sep 2022 03:28:16 GMT  
		Size: 12.6 MB (12631850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662090a6a1767b24d7e2fbb75ec98f703ea2e7f360ab2b62fce5f8ad57f6de60`  
		Last Modified: Tue, 13 Sep 2022 03:28:14 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88c860c68cbaa3914c61b149fa427ed00ad36e3cb17fbc12629f0afba7a580d`  
		Last Modified: Tue, 13 Sep 2022 03:29:04 GMT  
		Size: 32.1 MB (32110911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439b2f7e1b5bc6f7a4b6e1531537d37450de3024ddc892cdb9bfbe7d27817bd`  
		Last Modified: Tue, 13 Sep 2022 03:29:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:45ae264707bc3d4d5d876c5488a6b01e4cfcad4887f80d8ae74d0c1ddf0faefb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63285585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90d9a497b684fd241ef4b882b0fc848568a6dc74681429bde637f69bef73048`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 03:43:14 GMT
ADD file:0a80cba5196c5f463d85aeb456ee0f5778155ac5b1d3ce93a2023f1141aac44a in / 
# Tue, 13 Sep 2022 03:43:14 GMT
CMD ["bash"]
# Wed, 14 Sep 2022 08:17:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Sep 2022 08:17:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 14 Sep 2022 08:17:59 GMT
ENV LANG=C.UTF-8
# Wed, 14 Sep 2022 08:33:23 GMT
ENV RUBY_MAJOR=3.1
# Wed, 14 Sep 2022 08:33:23 GMT
ENV RUBY_VERSION=3.1.2
# Wed, 14 Sep 2022 08:33:23 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Wed, 14 Sep 2022 08:36:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Sep 2022 08:36:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Sep 2022 08:36:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Sep 2022 08:36:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Sep 2022 08:37:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 14 Sep 2022 08:37:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:04df89f99dde583959eeb3f2964381f6e5a3199fa335ea1b9862aab596638515`  
		Last Modified: Tue, 13 Sep 2022 03:50:50 GMT  
		Size: 22.7 MB (22740495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537ed80b226d4c844e500780a91a060f85148b85dc010a48bf7aa20570df240a`  
		Last Modified: Wed, 14 Sep 2022 09:07:19 GMT  
		Size: 9.9 MB (9926528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fe49d089127096177882fc1ed92bc5543d333b45dab19c356a247d2c492e5d`  
		Last Modified: Wed, 14 Sep 2022 09:07:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d66e823cd2aaa576675c1bdc857d3477b6d8e055d4d09735b2f775b3f4d480`  
		Last Modified: Wed, 14 Sep 2022 09:09:15 GMT  
		Size: 30.6 MB (30618186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c5707c6b6fff6f4f54502a89c984d67b2babde36a0945d70073aa472f2cebd`  
		Last Modified: Wed, 14 Sep 2022 09:09:11 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:6b78b570fd81498c2c5d605bbae90610a9d02908bc3563e2ca8dba80ee4bd450
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68593267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8824c11a4133a4c64003bfef85a5844da164943f88b2bbb53963a40d539f1d4b`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 04:19:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 04:19:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Sep 2022 04:19:32 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 04:24:38 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Sep 2022 04:24:39 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 13 Sep 2022 04:24:40 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 13 Sep 2022 04:26:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 13 Sep 2022 04:26:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Sep 2022 04:26:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Sep 2022 04:26:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 04:26:47 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 13 Sep 2022 04:26:48 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037d9aec918ce7b1d7ff3ae6a1fb5559fdbef1613aecb675a7038dcb60166246`  
		Last Modified: Tue, 13 Sep 2022 04:39:45 GMT  
		Size: 11.3 MB (11329564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b8b928ed77d86516195f815c6e824839fc3aaaa7e8a1b90e535649ac8e640b`  
		Last Modified: Tue, 13 Sep 2022 04:39:43 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cd8c187244c3c7c8b0f402ef6b1358d877a64b25e3aa999a6b1465e255bc07`  
		Last Modified: Tue, 13 Sep 2022 04:40:46 GMT  
		Size: 31.4 MB (31359209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8345a93d74f0bc4477bb38f69134f0e4569b71501766c4d64e6671bc51b27ea7`  
		Last Modified: Tue, 13 Sep 2022 04:40:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-slim-buster` - linux; 386

```console
$ docker pull ruby@sha256:1ad7fb07d2f365f90a3e1c42738191e260e33cb5b35406ee897107fc51489bd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75828185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7d84639fe12fc8731fa8efad59777c32aa9033feaf84a2db59b211f2f554e6`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Sep 2022 01:40:12 GMT
ADD file:da95249e10828562612e8b0a3595f3cbf6a5cb5dbfb47302a4d42a4a8c5025b1 in / 
# Tue, 13 Sep 2022 01:40:12 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 04:12:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 04:12:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Sep 2022 04:12:27 GMT
ENV LANG=C.UTF-8
# Tue, 13 Sep 2022 04:17:49 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Sep 2022 04:17:50 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 13 Sep 2022 04:17:51 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 13 Sep 2022 04:20:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 13 Sep 2022 04:20:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Sep 2022 04:20:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Sep 2022 04:20:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 04:20:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 13 Sep 2022 04:20:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7db2238a0cb6ea85529a33cb395b0243796e76066f31656ba5e08232e2fb0308`  
		Last Modified: Tue, 13 Sep 2022 01:46:12 GMT  
		Size: 27.8 MB (27790952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ee409eb25d5a286b2d237e9cfea1f0cacefd469b51f2f367faa400de04aaac`  
		Last Modified: Tue, 13 Sep 2022 04:33:40 GMT  
		Size: 17.3 MB (17292505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c710b97518b1300db542e8c58a47aa0d3ae2bd9b8bf97ec9933b44ab1b93575`  
		Last Modified: Tue, 13 Sep 2022 04:33:37 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a710148dc0f8088aafe1b561dc9a18b85f08a33fe8b617fdced151f22b81af`  
		Last Modified: Tue, 13 Sep 2022 04:34:41 GMT  
		Size: 30.7 MB (30744387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eaf9b844be8577fe2f74af5d49d39e2f32d501ef866c0916269a9f446d98723`  
		Last Modified: Tue, 13 Sep 2022 04:34:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
