## `ruby:rc-slim-buster`

```console
$ docker pull ruby@sha256:1d312fae73247890f9d1560cca2474e34a8af2b7413425f34a92779fec21c94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ruby:rc-slim-buster` - linux; amd64

```console
$ docker pull ruby@sha256:5c17d966eceeccb0c2636abaca7139d566e756040e9767f5eae64d27c915c5ef
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62453625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42a75e52f3b40a74ad90073ec80b3b31baa6c92714fc30b62db24b054eaec3c`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 12:48:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 12:48:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 23 Nov 2019 12:48:57 GMT
ENV RUBY_MAJOR=2.7-rc
# Wed, 27 Nov 2019 02:25:07 GMT
ENV RUBY_VERSION=2.7.0-preview3
# Wed, 27 Nov 2019 02:25:07 GMT
ENV RUBY_DOWNLOAD_SHA256=ad9d61e55ac224e3447a762e001965839846f9658f87a0e792840887cfe61b8c
# Wed, 27 Nov 2019 02:28:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 27 Nov 2019 02:28:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 27 Nov 2019 02:28:19 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 27 Nov 2019 02:28:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/bundle/gems/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2019 02:28:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 27 Nov 2019 02:28:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb775c9947bd15329b240cace20af8c8a27f2a0307b3a70afa4fc4d1fc48bca8`  
		Last Modified: Sat, 23 Nov 2019 13:53:45 GMT  
		Size: 12.5 MB (12539717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4023dfa48cbbce1634b98375fc7fd67949fb44a3364f32d3b5c26f67ac6f62`  
		Last Modified: Sat, 23 Nov 2019 13:53:41 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d59f22cf0d35cb8e84ac2bfdb3d45a0c366ab76feb6f9a7d1e4403aa8a6794`  
		Last Modified: Wed, 27 Nov 2019 02:33:32 GMT  
		Size: 22.8 MB (22820911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5211224ebabddeca1337196512f409852edc8547fd810a37f5189b0cbc421dff`  
		Last Modified: Wed, 27 Nov 2019 02:33:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim-buster` - linux; arm variant v5

```console
$ docker pull ruby@sha256:91fc34120a4c5f61c11ea941ce4bbbb4c25e812d0ddcf091c59d7863c5a72f1a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57230423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb22a9d347f4e67fcf227b6304038d32826f9a3d5872207bfa9cd12feb2e056`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 22 Nov 2019 12:13:54 GMT
ADD file:94ed554e445cf749e10644dfa0d836103c120a6ea388bf6dc9f18f7c6b2f095a in / 
# Fri, 22 Nov 2019 12:13:56 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 21:05:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 21:05:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 22 Nov 2019 21:05:40 GMT
ENV RUBY_MAJOR=2.7-rc
# Thu, 19 Dec 2019 01:32:41 GMT
ENV RUBY_VERSION=2.7.0-rc1
# Thu, 19 Dec 2019 01:32:45 GMT
ENV RUBY_DOWNLOAD_SHA256=7528db87df7a8cbfdcbd053073839f5a00b2a38f807771e3e45000e72fc86732
# Thu, 19 Dec 2019 01:37:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 19 Dec 2019 01:37:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 Dec 2019 01:37:52 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 Dec 2019 01:37:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/bundle/gems/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 01:37:55 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 19 Dec 2019 01:37:56 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:45ae7e8aa5bfd9e1b0db11d7fa5a56a8af11b69fc56707d763f89aa2c61b7e8f`  
		Last Modified: Fri, 22 Nov 2019 12:22:20 GMT  
		Size: 24.8 MB (24829480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2befe122bee8236017ffe93f128e20d77cb5946a5f00f13b742340f3a83bc6c0`  
		Last Modified: Fri, 22 Nov 2019 22:13:11 GMT  
		Size: 10.3 MB (10326045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468085ff5a63d0dff4c6810a05c346c9f588c93c6d4a04c5a95d97c9b853642c`  
		Last Modified: Fri, 22 Nov 2019 22:13:06 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b350c7f87eccf2b6d19e94e4b0c3b443bb4c816b0a8bf558f287b8e87ee6f2`  
		Last Modified: Thu, 19 Dec 2019 01:40:15 GMT  
		Size: 22.1 MB (22074524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f73dbe48efffeb77079e359581f4215b7e2c453961ec709ce77404eeda494c5`  
		Last Modified: Thu, 19 Dec 2019 01:40:10 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim-buster` - linux; arm variant v7

```console
$ docker pull ruby@sha256:5515a4ed5af88592254c6c5d0dc00b01d76f42c376299bda5f1c9b9d7ed3b8fa
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54508881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54098694c1272605105950e9f4bb48f217f77255fb2b65f3a803d1566a536f5`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:45 GMT
ADD file:85cf6081b7d1948b250d1b3749a65e2561cddafb7cd748db6b7b7420a376a48f in / 
# Fri, 22 Nov 2019 13:22:46 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 04:33:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 04:34:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 23 Nov 2019 04:34:26 GMT
ENV RUBY_MAJOR=2.7-rc
# Thu, 19 Dec 2019 02:21:47 GMT
ENV RUBY_VERSION=2.7.0-rc1
# Thu, 19 Dec 2019 02:21:50 GMT
ENV RUBY_DOWNLOAD_SHA256=7528db87df7a8cbfdcbd053073839f5a00b2a38f807771e3e45000e72fc86732
# Thu, 19 Dec 2019 02:26:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 19 Dec 2019 02:26:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 Dec 2019 02:26:13 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 Dec 2019 02:26:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/bundle/gems/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 02:26:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 19 Dec 2019 02:26:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3cf3d03fb414460b7542c20e72fe29a83f08d22fd2c7a8cab1834eec2976e4b2`  
		Last Modified: Fri, 22 Nov 2019 13:33:25 GMT  
		Size: 22.7 MB (22699053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5cd440452730be312ed9f6ff2063f4953c4ae8fb1859943c285839847657b8`  
		Last Modified: Sat, 23 Nov 2019 08:51:36 GMT  
		Size: 9.8 MB (9847641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580b62fa74a174b783ae61dc031d2ee1ad2a3a1abec926f4799eb8ce96221f4e`  
		Last Modified: Sat, 23 Nov 2019 08:51:32 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd0f2d1b6cbbdad7fb4d1c742df7bf6100a631094cbf02e67d4bb421e8179d8`  
		Last Modified: Thu, 19 Dec 2019 02:36:43 GMT  
		Size: 22.0 MB (21961811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2fcd895d2bbfbd31d482a30b404e0e6e1fc73fc53a391ad420bc1e01710a9a`  
		Last Modified: Thu, 19 Dec 2019 02:36:38 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim-buster` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:43864961007ebae36b43d7c813d37d3918d2f641c69962fb1216c8ca7dd89bc9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59765383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46930ec29fb5e078f2bad692879121384ace3a20287580e6ebe249a7f522b05b`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:59 GMT
ADD file:69e0891ef62c74ec5e9bae38f8d2770ab2f0d7ea0d3cf1dc85875763be0b10b7 in / 
# Fri, 22 Nov 2019 13:42:02 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 15:19:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 15:19:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 23 Nov 2019 15:19:59 GMT
ENV RUBY_MAJOR=2.7-rc
# Thu, 19 Dec 2019 03:11:36 GMT
ENV RUBY_VERSION=2.7.0-rc1
# Thu, 19 Dec 2019 03:11:37 GMT
ENV RUBY_DOWNLOAD_SHA256=7528db87df7a8cbfdcbd053073839f5a00b2a38f807771e3e45000e72fc86732
# Thu, 19 Dec 2019 03:16:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 19 Dec 2019 03:16:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 Dec 2019 03:16:34 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 Dec 2019 03:16:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/bundle/gems/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 03:16:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 19 Dec 2019 03:16:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a4f3dd4087f9309af4187e5dda90741441f057da59c2270598e16aa8019b0ca2`  
		Last Modified: Fri, 22 Nov 2019 13:49:50 GMT  
		Size: 25.9 MB (25850802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad002cc66de1024f4b545e0b251cecc37fb100c7c1496de41db6c36fa4a3c5e`  
		Last Modified: Sat, 23 Nov 2019 16:46:01 GMT  
		Size: 11.2 MB (11244462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136066132e4f7535bf1ff675b52ade73553f9816505cb941f687b6d46969304e`  
		Last Modified: Sat, 23 Nov 2019 16:45:57 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885ce45725f5ba91411f55e7eae1aa983267864b842be2e82a19fa1623cad835`  
		Last Modified: Thu, 19 Dec 2019 03:23:48 GMT  
		Size: 22.7 MB (22669743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393a5870b7f1f3548ec46d89bac27d4de5a0d10c7725c1cdc51663c5c7b57e47`  
		Last Modified: Thu, 19 Dec 2019 03:23:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim-buster` - linux; 386

```console
$ docker pull ruby@sha256:5cbe96d589f09b63f86f55b35ecc3decaf7c8b3900548c05a2df8705eee8b34c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67146975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac13376f37c26f647a23ae51e73898d23b6660b8ebda4895944ab57993ae5f6b`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 22 Nov 2019 16:50:19 GMT
ADD file:68f0911eb53ffc655e6a641b4acfb0670c2fd84c7dc34b0128735f0478532a6b in / 
# Fri, 22 Nov 2019 16:50:19 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 07:45:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 07:45:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 23 Nov 2019 07:45:54 GMT
ENV RUBY_MAJOR=2.7-rc
# Sat, 23 Nov 2019 07:45:54 GMT
ENV RUBY_VERSION=2.7.0-preview2
# Sat, 23 Nov 2019 07:45:54 GMT
ENV RUBY_DOWNLOAD_SHA256=fa39f088331f6d505154aa9d025aab177fdffedfbbabccd900b8c02e745bc077
# Sat, 23 Nov 2019 07:49:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sat, 23 Nov 2019 07:49:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 23 Nov 2019 07:49:53 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 23 Nov 2019 07:49:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/bundle/gems/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 07:49:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sat, 23 Nov 2019 07:49:54 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ce9b44038a207698571bb0cc0b950ee2a3608cb09b2b20712b353a54ae619111`  
		Last Modified: Fri, 22 Nov 2019 16:58:27 GMT  
		Size: 27.7 MB (27746760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca425a65f337091b48012d7fad57f0138c7dd28f20b773d830378d32fcdfa3c`  
		Last Modified: Sat, 23 Nov 2019 08:45:22 GMT  
		Size: 17.2 MB (17205652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33875468e1424f786b12bdc428b6ead9901f207196d04f4a34b47dc6eae2828d`  
		Last Modified: Sat, 23 Nov 2019 08:45:11 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cc9de6eeebbc6ccb7bd367f0e6893291f2d9804f1d0fdd231658e5fecd6236`  
		Last Modified: Sat, 23 Nov 2019 08:45:21 GMT  
		Size: 22.2 MB (22194220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690fcd515d5705b02260b6e3be6d354126c4b62082247e95ad02b2730b98e8cc`  
		Last Modified: Sat, 23 Nov 2019 08:45:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim-buster` - linux; ppc64le

```console
$ docker pull ruby@sha256:f40b6b75147e7d5b9fad2ba12fe41341ba88f987724d9212cfa292a6a62fadeb
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66563032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ef0d2c1a57dcb40425d7434cc61a447f1be29c4d628b2e7164ecac96e969f5`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:33 GMT
ADD file:56ee7f5cc8715d22f4efb9ec5b1c24fac7fdf8f6dc9c07c45625c4f89bdccac3 in / 
# Fri, 22 Nov 2019 14:55:37 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 02:01:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 02:01:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sat, 23 Nov 2019 02:01:58 GMT
ENV RUBY_MAJOR=2.7-rc
# Thu, 19 Dec 2019 03:43:12 GMT
ENV RUBY_VERSION=2.7.0-rc1
# Thu, 19 Dec 2019 03:43:15 GMT
ENV RUBY_DOWNLOAD_SHA256=7528db87df7a8cbfdcbd053073839f5a00b2a38f807771e3e45000e72fc86732
# Thu, 19 Dec 2019 03:47:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 19 Dec 2019 03:47:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 Dec 2019 03:48:01 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 Dec 2019 03:48:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/bundle/gems/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 03:48:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 19 Dec 2019 03:48:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e190211f5678d77388755410611e5e6a755e195e7a1096473c675edc074a2389`  
		Last Modified: Fri, 22 Nov 2019 15:04:10 GMT  
		Size: 30.5 MB (30517327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290d113506ef96fca5a922efc930a485e7381c4c1ea88219469796833d801259`  
		Last Modified: Sat, 23 Nov 2019 03:20:10 GMT  
		Size: 12.7 MB (12688875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da50836d8571492bde7f2465659bcfac604d80bf79277cd789d127464a0fc94`  
		Last Modified: Sat, 23 Nov 2019 03:20:06 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3ac4c9567582cf841d9448145d337ce1ce3e2ca64c51c2fa218896ff965d6e`  
		Last Modified: Thu, 19 Dec 2019 03:55:34 GMT  
		Size: 23.4 MB (23356454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0c984356bef492edb836cf3c8a4aa5f48a229d10f25f8d9923c6c8be751e39`  
		Last Modified: Thu, 19 Dec 2019 03:55:30 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:rc-slim-buster` - linux; s390x

```console
$ docker pull ruby@sha256:6d9ec1dcd0d2bdcb0b058e6680734eb2dc4ad582ffe2d53f0fa783588e73d79e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59513692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85078ce5d9a1d7277e93725ca7c1a442f8bf67cb3a9e18832fcba93716be3fbf`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 22 Nov 2019 10:40:33 GMT
ADD file:92d7fb80869eafe72ec0a814553e85cc6f6ace54374e03063dbcff07a4415447 in / 
# Fri, 22 Nov 2019 10:40:33 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 17:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 17:32:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 22 Nov 2019 17:32:48 GMT
ENV RUBY_MAJOR=2.7-rc
# Thu, 19 Dec 2019 01:06:11 GMT
ENV RUBY_VERSION=2.7.0-rc1
# Thu, 19 Dec 2019 01:06:12 GMT
ENV RUBY_DOWNLOAD_SHA256=7528db87df7a8cbfdcbd053073839f5a00b2a38f807771e3e45000e72fc86732
# Thu, 19 Dec 2019 01:08:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 19 Dec 2019 01:08:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 19 Dec 2019 01:08:02 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 19 Dec 2019 01:08:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/bundle/gems/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 01:08:03 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 19 Dec 2019 01:08:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2434d96be4ae20e5e4e1b50d6b3ff644c541815000df6f7c12efa5b652d79000`  
		Last Modified: Fri, 22 Nov 2019 10:44:48 GMT  
		Size: 25.7 MB (25705174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fc87c9e439ba935edbb0e5c8739c3f0daf524447412cd4f5627bf6f066bdff`  
		Last Modified: Fri, 22 Nov 2019 18:04:04 GMT  
		Size: 10.8 MB (10794235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7954ca3f72782fad1b439b4725b098cca9e62d7f6d29c6f49cf8b8a2abd0554c`  
		Last Modified: Fri, 22 Nov 2019 18:04:02 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb5654b1eb89a119220829f0c15ffa0e47a7bca42a28b8a486b3e54d0af4140`  
		Last Modified: Thu, 19 Dec 2019 01:12:58 GMT  
		Size: 23.0 MB (23013938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de78176666774fe9862b2dd0934557b5ba38cd5cf20253f0568b646ca96bc8ae`  
		Last Modified: Thu, 19 Dec 2019 01:12:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
