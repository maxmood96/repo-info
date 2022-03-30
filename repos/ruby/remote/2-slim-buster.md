## `ruby:2-slim-buster`

```console
$ docker pull ruby@sha256:0f04551980ef0b1299a3800f761f8d321c38fefd98676bdea66a57cd274bc592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `ruby:2-slim-buster` - linux; amd64

```console
$ docker pull ruby@sha256:8d6f346f6fb839997366bae884a92e881dcd9e2d754d5f00351376547e905785
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54275419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00854303a06d906b1c51496164f3dc22b2b278c4638c99603981efe330e9454`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 10:32:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 10:32:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 10:32:17 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 10:58:49 GMT
ENV RUBY_MAJOR=2.7
# Tue, 29 Mar 2022 10:58:49 GMT
ENV RUBY_VERSION=2.7.5
# Tue, 29 Mar 2022 10:58:50 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Tue, 29 Mar 2022 11:01:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 29 Mar 2022 11:01:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 29 Mar 2022 11:01:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 29 Mar 2022 11:01:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 11:01:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 29 Mar 2022 11:01:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f50025d0672279ac92c03f9450d7acd8865318daf73a2ac10dcc574ce8597b`  
		Last Modified: Tue, 29 Mar 2022 11:19:28 GMT  
		Size: 12.6 MB (12581277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5812fdc56bb069b5ee346cc2335a2233b171cbec31ff56d4c2fb7fd7727b4d9`  
		Last Modified: Tue, 29 Mar 2022 11:19:26 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99095d5716240a4154b983df352f3ca93fda3704e9ba67887441a9fcf9bd8322`  
		Last Modified: Tue, 29 Mar 2022 11:21:52 GMT  
		Size: 14.5 MB (14541799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad132bf1f88da8cccad4490ab58a047d40174583c192e9d7cc8ecbf488611865`  
		Last Modified: Tue, 29 Mar 2022 11:21:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; arm variant v5

```console
$ docker pull ruby@sha256:b423d6011571b044b93ae7e49c376dde5709f14f6d2c53677095ac40ef6c186c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49133771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fd8b079b84a9630cdff32c40a23476612c43037b4768cec9b35ad5eee833ec`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 05:20:46 GMT
ADD file:4b7bce60b3e3455ba9b14c881ffa61187b9e56365fe4f275ee871e7c7e930fb9 in / 
# Thu, 17 Mar 2022 05:20:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:18:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 18:18:28 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 18:41:06 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Mar 2022 18:41:06 GMT
ENV RUBY_VERSION=2.7.5
# Thu, 17 Mar 2022 18:41:07 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Thu, 17 Mar 2022 18:45:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 18:46:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 18:46:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 18:46:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 18:46:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 18:46:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f193682138b0c37054cb843ef2155a75706f248a369d454bf6444833f120aefc`  
		Last Modified: Thu, 17 Mar 2022 05:36:29 GMT  
		Size: 24.9 MB (24886195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96710cd49a7971b2d375ed6a4e2b9b3c346ddd6eccddcf626a6a5952d4761371`  
		Last Modified: Thu, 17 Mar 2022 19:03:43 GMT  
		Size: 10.3 MB (10348954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea873326987bb8e6add742f0b299995920760d1a154732afb6605f8277c9268b`  
		Last Modified: Thu, 17 Mar 2022 19:03:37 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9008ac1a07d889200cbbc22b80ff13379adf5f7210ca0fbb9731e0a07d97293`  
		Last Modified: Thu, 17 Mar 2022 19:06:01 GMT  
		Size: 13.9 MB (13898250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f141bf45c65e7301b4b0a8d528df8bdb764b2aa4d2fe8fc13db95aca90a1ca`  
		Last Modified: Thu, 17 Mar 2022 19:05:57 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:741483d2cb130e8cda0468d991093e74a901606db6a49041f8df969511d4ce09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46420485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644ed2a9a6622ed56612a4aa433acbf365a85ef515c0a9dce1eade3d99aa7379`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 09:32:07 GMT
ADD file:ca7a6b7c138de7fd85996719398396d0ed0f059d2e12b7f401cd460b64924e25 in / 
# Thu, 17 Mar 2022 09:32:08 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 12:41:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 12:41:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 18 Mar 2022 12:41:14 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 13:18:50 GMT
ENV RUBY_MAJOR=2.7
# Fri, 18 Mar 2022 13:18:50 GMT
ENV RUBY_VERSION=2.7.5
# Fri, 18 Mar 2022 13:18:50 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Fri, 18 Mar 2022 13:22:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 18 Mar 2022 13:22:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 18 Mar 2022 13:22:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 18 Mar 2022 13:22:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 13:22:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 18 Mar 2022 13:22:56 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0b8f06901fc5e8a29999e260b4ada4ee1cc4415e5c1a16fb7bb21cc2ac995f72`  
		Last Modified: Thu, 17 Mar 2022 09:48:01 GMT  
		Size: 22.8 MB (22754389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e124b65386fabaa7971619254cd2a043e78822adbf73cfa2c62da8c24234c5`  
		Last Modified: Fri, 18 Mar 2022 13:55:07 GMT  
		Size: 9.9 MB (9872973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f8cac5fcdd0784685b4345eab21f5c830506856ea662bf8350910342a9879`  
		Last Modified: Fri, 18 Mar 2022 13:55:00 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af67b70c089cb7b7f410790e5d712de35dd000ac9c96c3664462df766fa59989`  
		Last Modified: Fri, 18 Mar 2022 13:59:36 GMT  
		Size: 13.8 MB (13792749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c5602231984219e82767715794ee2a91163cb7b40d64bd4e12fee12f618570`  
		Last Modified: Fri, 18 Mar 2022 13:59:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:e35ed9247fe9aeebf6b25e878949ae3a56944f237a1ed6f5bc9487b44e622111
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51358436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f6dad7eb4a0caa28a2b551c0ee78bc814fbb79d1279a642d716ea53fa5f75c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 20:14:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 20:14:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 20:14:06 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 20:33:25 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Mar 2022 20:33:26 GMT
ENV RUBY_VERSION=2.7.5
# Thu, 17 Mar 2022 20:33:27 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Thu, 17 Mar 2022 20:35:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 20:35:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 20:35:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 20:35:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 20:35:11 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 20:35:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba00919e9bc7af9af691a92dbfeef3ca40c29e924ff156b705f3d8168caf7f28`  
		Last Modified: Thu, 17 Mar 2022 20:51:59 GMT  
		Size: 11.3 MB (11261791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026504a0d60799aae9f35f23d7dbcaadfe16543f13e4f4ed3a811e62444a5151`  
		Last Modified: Thu, 17 Mar 2022 20:51:57 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27885d521e38a6629bba4350d4d1c020cd4f9549b6a1633494cb1d27953f9b12`  
		Last Modified: Thu, 17 Mar 2022 20:54:59 GMT  
		Size: 14.2 MB (14173071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc33469bffbfc152cffb11e92066b5767913f3e4b73813e1e016105fec04ba7e`  
		Last Modified: Thu, 17 Mar 2022 20:54:57 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; 386

```console
$ docker pull ruby@sha256:847a34a1bf6362c872cee50a832fa8aadf1674427fd51947638c26fbf3458d1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58839939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1807de95123c6c15a3f3ab40cfbcca9f230f3b3d8bbaa7b4cd26ca39ea226232`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:26 GMT
ADD file:bcf3d504dc285de8b639c7f4017c41a4593a6c2aa6f046c9be79e587d05b5120 in / 
# Tue, 29 Mar 2022 00:42:27 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 10:00:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 10:00:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 10:00:17 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 10:20:05 GMT
ENV RUBY_MAJOR=2.7
# Tue, 29 Mar 2022 10:20:05 GMT
ENV RUBY_VERSION=2.7.5
# Tue, 29 Mar 2022 10:20:06 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Tue, 29 Mar 2022 10:21:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 29 Mar 2022 10:21:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 29 Mar 2022 10:21:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 29 Mar 2022 10:21:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 10:21:49 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 29 Mar 2022 10:21:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:65b92490caa5e2c0588fab60d39315a2a8c09aa8ea0fe208d23f6984a47ecc03`  
		Last Modified: Tue, 29 Mar 2022 00:50:02 GMT  
		Size: 27.8 MB (27801252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a237049b615c6378412074b43b9be2a006a39ce2774924350cb13cf964196eb`  
		Last Modified: Tue, 29 Mar 2022 10:38:43 GMT  
		Size: 17.2 MB (17235396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b347ed75fb0e86c7dc48ba6f435bc768d9dab571bbb43ab3c59fcf217720b0`  
		Last Modified: Tue, 29 Mar 2022 10:38:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e928db8efda3767ba3c0adde21d519b7aecc792097856391832aa623e474e1e8`  
		Last Modified: Tue, 29 Mar 2022 10:41:45 GMT  
		Size: 13.8 MB (13802952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512aaa5b6844fa876fde6771d951c7916741b5e197f79c0cefba1279835d20de`  
		Last Modified: Tue, 29 Mar 2022 10:41:42 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; mips64le

```console
$ docker pull ruby@sha256:1e01ab7682ae7094316d37d7be4ef20e96a496f6d773abeaf5b72801dcfd8497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51902203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1966ebfc993fa30597e4537cbcc7a717466af53d1a58fb6bbbe25b729ed313f0`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 08:54:09 GMT
ADD file:47b03990ddc290dac99c4fb2fb851724325624d58fc57f6c9902ba2a98a54bea in / 
# Thu, 17 Mar 2022 08:54:13 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 19:00:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 19:00:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 18 Mar 2022 19:00:26 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 20:26:54 GMT
ENV RUBY_MAJOR=2.7
# Fri, 18 Mar 2022 20:26:57 GMT
ENV RUBY_VERSION=2.7.5
# Fri, 18 Mar 2022 20:27:00 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Fri, 18 Mar 2022 20:36:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 18 Mar 2022 20:36:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 18 Mar 2022 20:36:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 18 Mar 2022 20:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 20:36:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 18 Mar 2022 20:36:43 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4563fe17a75d3d628ff1f7de39c0d8aa8e256bebfcca83591111dc19e4b15795`  
		Last Modified: Thu, 17 Mar 2022 10:44:40 GMT  
		Size: 25.8 MB (25820197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aedb250cc8b00e1d0f3a5869c795be746c5cac8f9faf91e6401948509cf94bf`  
		Last Modified: Fri, 18 Mar 2022 21:19:46 GMT  
		Size: 11.6 MB (11630240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638ccb9be331173fbdbcd80ed55ec468ae5c9c2aae417cc064ce94d6fa66765d`  
		Last Modified: Fri, 18 Mar 2022 21:19:36 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97e43cd0c31e76237baebb7562e776169cfe8b04ca9eced5a8afe4ccb16b39e`  
		Last Modified: Fri, 18 Mar 2022 21:23:08 GMT  
		Size: 14.5 MB (14451422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef849d799acdd65002f2ab3b1084d8b79e1029cf9a286ee7f8648851068e965e`  
		Last Modified: Fri, 18 Mar 2022 21:23:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; ppc64le

```console
$ docker pull ruby@sha256:a30f05a88f9a222b949363c2b96addb35933bafe10c23e71b8566a51d9eaad7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58317270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6008d8ce5586a8156ee6edb2df1240eb327acba516c1224f39a3ed7c574d5f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:59 GMT
ADD file:7271d778d432a07f57fedf8d50d83699ef545acc9db9346f6fe75b0054af4cd1 in / 
# Tue, 29 Mar 2022 00:23:00 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 20:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 20:23:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 20:23:19 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 21:04:45 GMT
ENV RUBY_MAJOR=2.7
# Tue, 29 Mar 2022 21:04:48 GMT
ENV RUBY_VERSION=2.7.5
# Tue, 29 Mar 2022 21:04:51 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Tue, 29 Mar 2022 21:10:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 29 Mar 2022 21:10:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 29 Mar 2022 21:10:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 29 Mar 2022 21:10:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 21:11:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 29 Mar 2022 21:11:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7db831386ce67ac1cf2b4f1513fe3746c9ea2b8d4c82efca75be638eaf533614`  
		Last Modified: Tue, 29 Mar 2022 00:34:41 GMT  
		Size: 30.6 MB (30560163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308b496e1e95a5feaf264a7cc31e6b3c3374fe5e96c73fe9189627bc50dc558`  
		Last Modified: Tue, 29 Mar 2022 21:51:39 GMT  
		Size: 12.7 MB (12724933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2deab05a4a7c0b5c756150a843ec69322aa059b31c6b469fae6c15e5e74aaa25`  
		Last Modified: Tue, 29 Mar 2022 21:51:36 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1303d883ae3fe073690ef95e100d3c1f482eeb8044d752902251372faac88372`  
		Last Modified: Tue, 29 Mar 2022 21:54:55 GMT  
		Size: 15.0 MB (15031801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27349e215e16f7180699a867cf8128ed18faa9b53a6d0a6b64cbcf305ab82f2e`  
		Last Modified: Tue, 29 Mar 2022 21:54:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-slim-buster` - linux; s390x

```console
$ docker pull ruby@sha256:1b091f4bca21b0e5ba3a084dfe502e42df435ccb99fd00e73f330ceab02266f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51316277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abf5fb42d92d7c25c48c2c6f9de5ffab2efbfba8335816e2553ce4253f032a0`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 03:07:30 GMT
ADD file:4342e1d9db757e91953273ac7120c9d6004d38281f9cea830898b4f35ca43517 in / 
# Thu, 17 Mar 2022 03:07:32 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 15:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 15:49:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 15:49:57 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 16:07:03 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Mar 2022 16:07:03 GMT
ENV RUBY_VERSION=2.7.5
# Thu, 17 Mar 2022 16:07:04 GMT
ENV RUBY_DOWNLOAD_SHA256=d216d95190eaacf3bf165303747b02ff13f10b6cfab67a9031b502a49512b516
# Thu, 17 Mar 2022 16:08:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 16:08:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 16:08:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 16:08:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 16:08:24 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 16:08:24 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6f8a08956872b0f67802da3a67e007322eb963a60e0dadd736077f3ece414e1f`  
		Last Modified: Thu, 17 Mar 2022 03:13:18 GMT  
		Size: 25.8 MB (25769076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9cef5c82f53c076a6b79c5df66e5aa85afd14eb4dfee12b48f9f24590f5787`  
		Last Modified: Thu, 17 Mar 2022 16:23:24 GMT  
		Size: 10.8 MB (10815376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d0a7487845abb7f24bbfa9fbfa7aa7ba2db74064de78c2e76a6d43cfa13400`  
		Last Modified: Thu, 17 Mar 2022 16:23:22 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dbb255fade604c5e6d73dc46a983386b07e4a755500132f48d8e13bd9a6e0f`  
		Last Modified: Thu, 17 Mar 2022 16:26:26 GMT  
		Size: 14.7 MB (14731450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5eff1821a1cec41d67097b8a3d453e923ede40793dd74fcba938bfbe41ee10`  
		Last Modified: Thu, 17 Mar 2022 16:26:25 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
