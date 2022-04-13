## `ruby:slim-bullseye`

```console
$ docker pull ruby@sha256:7ef9a9490d99dff73bc72ab9f96707f432de8cdc9ac84347b527d5129ffb59b4
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

### `ruby:slim-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:8a2e611b6b5779ce06d58867bbe67b5e37ae1da23f74acca2d491739af065dd2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73805431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46930b6a37bed03ab35b5fc869011070012edfbd0be92d062f77f8ef853d36fe`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 10:28:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 10:28:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 10:28:51 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 10:28:51 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:22:38 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:22:38 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:24:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:24:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:24:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:24:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:25:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:25:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a196c62ee705bf37cfab91ea1d171f7b636ffd65269877b758f726189872e`  
		Last Modified: Tue, 29 Mar 2022 11:19:01 GMT  
		Size: 10.0 MB (9990916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365bbf24384cc62b2e96112071ead0fb9d34bb8f42158306d2b628b641fc0068`  
		Last Modified: Tue, 29 Mar 2022 11:18:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8784bbb4c7ec0168d6c466e23dac93bd30b1448a26aed635fd4049e2ad800bac`  
		Last Modified: Tue, 12 Apr 2022 19:14:08 GMT  
		Size: 32.4 MB (32435682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4692036d56896f8c38296e16c51dd6b2032285fc66bb8e8ef2a8600c5ce315`  
		Last Modified: Tue, 12 Apr 2022 19:14:05 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:7945a7aca8bdd38124366b7219425341786df2290692bdad0fbb73b53a6b152c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68538934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f955d0008684f1c5d8d26d141870d3ddc6da2adc5a2f1252c50bc98e0d20e2`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:50:37 GMT
ADD file:6b9a30e6ef50a46e87cf9d7f5a491c7951fdb6dd6fab3c9d4a9c3c40f92b8db4 in / 
# Tue, 29 Mar 2022 00:50:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 23:44:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:44:22 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 23:44:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 23:44:22 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:54:49 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:54:49 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:59:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:59:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:59:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:59:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:59:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:59:57 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9a41aba0a099ec129c20f41f6370b97daa4c3d4d3edc76ea1863bc5f76f9e5e5`  
		Last Modified: Tue, 29 Mar 2022 01:05:21 GMT  
		Size: 28.9 MB (28920513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf44c7251b2b648f973f028009b225f6c08537764f423748cb086f75716c797`  
		Last Modified: Wed, 30 Mar 2022 01:01:08 GMT  
		Size: 8.6 MB (8633465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab9a3a54418b6eafc72c90d31b5f425c60b3b5f13be1f1407c1c9f1619eb964`  
		Last Modified: Wed, 30 Mar 2022 01:01:01 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffb9d891fbbd22cd1d7f19de88f954a71664ac41bce30416b43419d3aff6af4`  
		Last Modified: Tue, 12 Apr 2022 20:12:24 GMT  
		Size: 31.0 MB (30984584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee775b9a0dd14b98853568291f23d025801ab9d14024978e9399d0526237cbb`  
		Last Modified: Tue, 12 Apr 2022 20:12:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:821558c49f4a1299268daf78bb7358a944407a6cd27989630dab1c1e5053d6a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65567986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5ecec3b282a10ce5a46ab46a34bcb0de61a6c6a119abda12360a46c9b2f689`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 02:18:34 GMT
ADD file:e1835d1a0c70a0335757f211893e5d12ddf797e489e10434c0982bdf9b234f67 in / 
# Tue, 29 Mar 2022 02:18:36 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 15:07:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 15:07:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 30 Mar 2022 15:07:38 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 15:07:38 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 19:04:43 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 19:04:44 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 19:09:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 19:09:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 19:09:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 19:09:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 19:09:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 19:09:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f98812e1a494a683a5b3dea593dd2ef305f5f732193044c147f22e44b00164bc`  
		Last Modified: Tue, 29 Mar 2022 02:34:13 GMT  
		Size: 26.6 MB (26575370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f688115dbd56a1fea4d640c931a8c2458750d03deb3a447bc7117990adf76eb5`  
		Last Modified: Wed, 30 Mar 2022 16:27:08 GMT  
		Size: 8.1 MB (8143596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c61f3a636f525c0fd50a0f7a8613b3d9ab7e850dcd61dfe7b3ff478e64d614`  
		Last Modified: Wed, 30 Mar 2022 16:27:01 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897ad87a8787f8399fb423553c4ffc0b40332ebe1a1f4ddd18a7dca9dd329a83`  
		Last Modified: Tue, 12 Apr 2022 20:56:44 GMT  
		Size: 30.8 MB (30848645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10e548458742aa9b9210af2effd3013ea1d64b790c5df31c7a408e02ab5a1e0`  
		Last Modified: Tue, 12 Apr 2022 20:56:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:07b55558936dcc5dac77ef71cc91e6e12c48d745300c7ff24591bca2bdf3a4a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70689026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33ca89737841e7b7376b973d4ac430cfb55959f3d536897d9c39fb749d423d2`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 01:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 01:04:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 30 Mar 2022 01:04:40 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 01:04:41 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:43:27 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:43:28 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:45:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:45:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:45:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:45:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:45:43 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:45:44 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6f29ca162065ee9762bc3cc495618ef13e2942009a5b8aef07e4da875edb31`  
		Last Modified: Wed, 30 Mar 2022 02:04:44 GMT  
		Size: 9.0 MB (9035255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9987e0079ca5ec9f2ced5c365ab9fb5b01fac470fb359dee0903acbeca51dd16`  
		Last Modified: Wed, 30 Mar 2022 02:04:42 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48196e433ad9b3a1e904929f0f9daa120f843a3eab5baf46d167e78676331e2`  
		Last Modified: Tue, 12 Apr 2022 19:38:16 GMT  
		Size: 31.6 MB (31589118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27b69cce8ce2ad547e2a433ab3fa14a46d8f28acc3535d1fb6f361ba7892f73`  
		Last Modified: Tue, 12 Apr 2022 19:38:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:2d2857c332da604e07ec29aa00b35d2bc86cf8bb4163bc53f0cb8166fde16d61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74966144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddab87e531a9d307206478b164ba46b013891622c6dc6587d8ffd500ca08668`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:01 GMT
ADD file:d093057c080a13cc4370d0e786857751004b8cd3c93368742512abbee4f1de83 in / 
# Tue, 29 Mar 2022 00:42:01 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 09:57:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 09:57:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 09:57:26 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 09:57:27 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:41:46 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:41:47 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:44:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:44:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:44:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:44:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:44:05 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:44:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:fec59da75229f638ca2878278d3859a1a8b73a20d5c0c043354eb37129ebb8bf`  
		Last Modified: Tue, 29 Mar 2022 00:49:10 GMT  
		Size: 32.4 MB (32389518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97056a7b1dd6e578c21e2af25f613c64cfd3f6709ea95ef1a5f57b3582aa3a2d`  
		Last Modified: Tue, 29 Mar 2022 10:38:06 GMT  
		Size: 11.8 MB (11788492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69a680da3ca1ea5bb12eb18b3ec7db1c4d6bc215a757ea067a4325dd39766a8`  
		Last Modified: Tue, 29 Mar 2022 10:38:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da219e907bb936e188388b3c9f546ad95595e9a4982aaac4fe207140865c946c`  
		Last Modified: Tue, 12 Apr 2022 19:35:56 GMT  
		Size: 30.8 MB (30787794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9864a2e7c8a2bc4d371746851b3f7ad54010b29f11a4b755f52186fc4d028046`  
		Last Modified: Tue, 12 Apr 2022 19:35:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:7d2853e68ff55a441a96164ed110d12c74e2eea7268224b4359e80c377248375
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71361901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff74a19cacc626bf1dc2993a13ad236a7ef87f53b1b68f50c245ff831fe7273`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 07:42:27 GMT
ADD file:32aa9fd7ee5c64e4bd49459e801e3e5dc50138590bbfca671e336a197aa7fa92 in / 
# Tue, 29 Mar 2022 07:42:31 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 22:55:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 22:55:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 30 Mar 2022 22:55:48 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 22:55:51 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 19:20:01 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 19:20:04 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 19:33:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 19:33:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 19:33:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 19:33:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 19:33:22 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 19:33:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5c2a8045f9de06328ab3d0ff505d990892219b7faee393bc9ac342347fc83d04`  
		Last Modified: Tue, 29 Mar 2022 07:52:59 GMT  
		Size: 29.6 MB (29641474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e515fbd7ef30fc5572e4b46c918bc345341150fa86849a004400bbc0baf3949c`  
		Last Modified: Thu, 31 Mar 2022 01:40:05 GMT  
		Size: 9.6 MB (9628974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99422d3257f2492a1c72895858658495bd23ded3637025d7007247513d77301`  
		Last Modified: Thu, 31 Mar 2022 01:39:56 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07c58d5658d46f9bd3cc358242fd09b816f778f7a00bfa298b2eb38e08c9f8`  
		Last Modified: Tue, 12 Apr 2022 22:04:19 GMT  
		Size: 32.1 MB (32091112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1085f6ad8f1eecff76bf0589393fe227b71680d2d4538eefe7513c9246541fa`  
		Last Modified: Tue, 12 Apr 2022 22:04:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:d07014723013a550af99afc4052d39984b2513c40cafcb0355afcfb83be2b73a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78361178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f233f57c0d516936703b9fddd5b1454bb727a322366f6e3dcd0c875ab909bb46`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:08 GMT
ADD file:e7ae113c10f322a9cffc46b62ba12820e270caaadaee3c5b907c801a37e1632c in / 
# Tue, 29 Mar 2022 00:22:11 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 20:15:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 20:15:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 20:15:42 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 20:15:45 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:29:54 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:30:00 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:54:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:54:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:54:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:54:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:54:36 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:54:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ecc74bb8af5a048e1123af0e17d88ef3da1d10951ada79e8e1cc9c0a694245d3`  
		Last Modified: Tue, 29 Mar 2022 00:32:57 GMT  
		Size: 35.3 MB (35282506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562a86188fb99fc4a0a625ba1095e72199d3ed24a320c53438ff2f86ff81d5`  
		Last Modified: Tue, 29 Mar 2022 21:50:59 GMT  
		Size: 10.5 MB (10476023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33bf06fdc797244697941f6f490e54db503199df283939fa0e50eba6c623bdc`  
		Last Modified: Tue, 29 Mar 2022 21:50:56 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecb30da86cdaf7b2a5c9d16a57524caee368b94755cdc5c1201261664dfea23`  
		Last Modified: Tue, 12 Apr 2022 21:15:42 GMT  
		Size: 32.6 MB (32602274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e803ba57bf1d774ed71a6680a063570101979406c8c0c18472417c84d24cb926`  
		Last Modified: Tue, 12 Apr 2022 21:15:28 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:018439975ce258e4fb589ae05ffbf051c3e7a77cd67cfc335f67248a2b76d319
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70765441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddc2a0718ca1e1abf15edae03de8295e6c984186241a19d52fa10b63a04f5dc`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:57 GMT
ADD file:39c5e0d7a686abd19448ab3e6237d50955ae2187fc2b64289a08c2549352b8f1 in / 
# Tue, 29 Mar 2022 00:51:58 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 23:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:31:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 23:31:15 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 23:31:16 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:45:32 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:45:33 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:48:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:48:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:48:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:48:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:48:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:48:07 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ffb22bcde95509bb75f6dd2d69f3fdb5c7471727e4d720b31d92cd297582865c`  
		Last Modified: Tue, 29 Mar 2022 01:04:43 GMT  
		Size: 29.7 MB (29655426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2caa2d369e39e8f176bf162dfa7070d65d69e293ec77edecf1bb425470ed7a`  
		Last Modified: Wed, 30 Mar 2022 00:08:54 GMT  
		Size: 8.9 MB (8859363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1f3b5dab660c0503abcae2c3dd4baf626ff13d1e698d4bcb82adfe3981b67c`  
		Last Modified: Wed, 30 Mar 2022 00:08:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb0b41c7454034e3866ce37178b2f85a3508344189d97f9845100bcd3942f5c`  
		Last Modified: Tue, 12 Apr 2022 20:00:34 GMT  
		Size: 32.3 MB (32250278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ecfe0436e15f3b6a3146f65ac3f50803e4567ddd3e331e1d5c30c92508d31c`  
		Last Modified: Tue, 12 Apr 2022 20:00:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
